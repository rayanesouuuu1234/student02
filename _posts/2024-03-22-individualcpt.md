<!DOCTYPE html>
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

body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 15px 0;
    text-align: center;
}

main {
    width: 80%;
    margin: 20px auto;
    padding: 15px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

form {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
    margin-bottom: 20px;
}

form label {
    text-align: right;
    margin-right: 10px;
}

form input, form select, form button {
    width: 100%;
    padding: 10px;
    margin: 5px 0;
    border-radius: 5px;
    border: 1px solid #ccc;
}

form button {
    background-color: #4CAF50;
    color: white;
    cursor: pointer;
}

#prediction-result {
    text-align: center;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: #333;
    color: white;
}

