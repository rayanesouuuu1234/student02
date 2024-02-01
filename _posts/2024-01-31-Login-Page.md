## Signup

<form id="signupForm">
    <label for="username">Username (UID):</label>
    <input type="text" id="username" name="username" required>
    <br>
    <label for="password">Password:</label>
    <input type="password" id="password" name="password" required>
    <br>
    <button type="submit">Create Account</button>
</form>

## Login Form

<form id="loginForm">
    <label for="loginUsername">Username:</label>
    <input type="text" id="loginUsername" name="loginUsername" value="toby" required>
    <br>
    <label for="loginPassword">Password:</label>
    <input type="password" id="loginPassword" name="loginPassword" value="123toby" required>
    <br>
    <button type="submit">Log In</button>
</form>

<script>
// Handle the signup form submission
document.getElementById('signupForm').addEventListener('submit', function(e) {
    e.preventDefault(); // Prevent default form submission

    const signupData = {
        uid: document.getElementById('username').value,
        password: document.getElementById('password').value,
        // dob: document.getElementById('dob').value, // Uncomment and add a dob input if needed
    };

    fetch('http://127.0.0.1:8086/api/users', { // Adjust the endpoint if necessary
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
        },
        body: JSON.stringify(signupData),
    })
    .then(response => {
        if (!response.ok) {
            throw new Error('Network response was not ok ' + response.statusText);
        }
        return response.text();
    })
    .then(data => {
        console.log(data);
        alert('Account created successfully!');
    })
    .catch(error => {
        console.error('There was a problem with your fetch operation:', error);
        alert('Error creating account: ' + error.message);
    });
});

// Handle the login form submission
document.getElementById('loginForm').addEventListener('submit', function(e) {
    e.preventDefault(); // Prevent default form submission

    const loginData = {
        uid: document.getElementById('loginUsername').value,
        password: document.getElementById('loginPassword').value,
    };

    fetch('http://127.0.0.1:8086/api/users/authenticate', { // Adjust the endpoint if necessary
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
        },
        body: JSON.stringify(loginData),
    })
    .then(response => {
        if (!response.ok) {
            throw new Error('Login failed: ' + response.statusText);
        }
        return response.text();
    })
    .then(data => {
        console.log(data);
        alert('Login successful!');
    })
    .catch(error => {
        console.error('There was a problem with the login operation:', error);
        alert('Error logging in: ' + error.message);
    });
});
</script>
