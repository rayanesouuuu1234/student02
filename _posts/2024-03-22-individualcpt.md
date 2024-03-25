
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Used Car Price Predictor</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Used Car Price Predictor</h1>
    </header>
    <main>
        <form id="price-prediction-form">
            <label for="year">Year:</label>
            <input type="number" id="year" name="year" min="1990" max="2022" required>

            <label for="km_driven">Kilometers Driven:</label>
            <input type="number" id="km_driven" name="km_driven" required>

            <label for="fuel">Fuel Type:</label>
            <select id="fuel" name="fuel" required>
                <option value="Petrol">Petrol</option>
                <option value="Diesel">Diesel</option>
                <option value="CNG">CNG</option>
                <option value="LPG">LPG</option>
                <option value="Electric">Electric</option>
            </select>

            <label for="transmission">Transmission:</label>
            <select id="transmission" name="transmission" required>
                <option value="Manual">Manual</option>
                <option value="Automatic">Automatic</option>
            </select>

            <label for="owner">Owner:</label>
            <select id="owner" name="owner" required>
                <option value="First Owner">First Owner</option>
                <option value="Second Owner">Second Owner</option>
                <option value="Third Owner">Third Owner</option>
                <option value="Fourth Owner">Fourth Owner</option>
                <option value="Above Fourth Owner">Above Fourth Owner</option>
            </select>

            <button type="submit">Predict Price</button>
        </form>
        <div id="prediction-result">
            <h2>Estimated Price:</h2>
            <p id="predicted-price"></p>
        </div>
    </main>
    <footer>
        <p>&copy; 2024 Used Car Price Predictor</p>
    </footer>
    <script src="app.js"></script>
</body>
</html>

<style>
/* Reset default browser styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
/* Reset default browser styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    transition: background-color 0.3s, color 0.3s;
}

body, html {
    height: 100%;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #121212;
    color: #ffffff;
}

header {
    background-color: #1F1F1F;
    padding: 20px 0;
    text-align: center;
    width: 100%;
    box-shadow: 0 2px 10px 0 rgba(255, 255, 255, 0.1);
}

h1 {
    margin: 0;
    font-size: 2.5rem;
    color: #0d6efd;
    text-transform: uppercase;
    letter-spacing: 1px;
}

main {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: calc(100% - 60px);
    padding: 40px 0;
}

form {
    margin: 30px 0;
    padding: 20px;
    border-radius: 10px;
    background-color: #252525;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
}

input, select, button {
    width: 300px;
    padding: 15px;
    margin: 10px 0;
    border: none;
    border-radius: 5px;
}

input[type='number'], select {
    background-color: #333;
    color: #ddd;
}

input[type='number']:focus, select:focus {
    outline: none;
    border: 2px solid #0d6efd;
}

button {
    background-color: #0d6efd;
    color: #fff;
    font-size: 1rem;
    letter-spacing: 1px;
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
}

button:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 20px rgba(13, 110, 253, 0.5);
}

button:active {
    transform: translateY(-1px);
}

#prediction-result {
    margin-top: 20px;
    padding: 20px;
    background-color: #333;
    border-radius: 10px;
    box-shadow: inset 0 0 10px 0 rgba(255, 255, 255, 0.1);
}

#predicted-price {
    font-size: 1.5rem;
    font-weight: bold;
    color: #4CAF50;
}

footer {
    background-color: #1F1F1F;
    color: #8c8c8c;
    text-align: center;
    padding: 10px 0;
    position: absolute;
    bottom: 0;
    width: 100%;
}

footer p {
    margin: 0;
    font-size: 1rem;
}