<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>ML Sports Betting</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            width: 80%;
            margin: auto;
        }
        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }
        main {
            display: flex;
            justify-content: space-between;
            padding: 20px;
        }
        .games-list {
            width: 60%;
        }
        .betting-slip {
            width: 35%;
            background-color: #fff;
            padding: 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #333;
            color: white;
        }
        .game {
            background-color: #fff;
            margin: 10px 0;
            padding: 10px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .betting-slip .title {
            text-align: center;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px;
            border: none;
            cursor: pointer;
            display: block;
            width: 100%;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>ML Sports Betting</h1>
        </header>
        <main>
            <div class="games-list">
                <div class="game">
                    <h2>Game 1: Team A vs Team B</h2>
                    <p>Odds: Team A 1.5 - Team B 2.5</p>
                    <button onclick="addToSlip('Game 1', 'Team A', 1.5)">Bet on Team A</button>
                    <button onclick="addToSlip('Game 1', 'Team B', 2.5)">Bet on Team B</button>
                </div>
                <!-- More games can be added here -->
            </div>
            <div class="betting-slip">
                <h2 class="title">Your Betting Slip</h2>
                <div id="bet-slip-content">
                    <!-- Bets added to the slip will appear here -->
                </div>
                <button id="place-bet">Place Bet</button>
            </div>
        </main>
        <footer>
            <p>&copy; 2024 ML Sports Betting</p>
        </footer>
    </div>
    <script>
        const slipContent = document.getElementById('bet-slip-content');
        const bets = [];
        function addToSlip(game, team, odds) {
            const bet = { game, team, odds };
            bets.push(bet);
            renderSlip();
        }
        function renderSlip() {
            slipContent.innerHTML = ''; // Clear existing slip content
            bets.forEach(bet => {
                const betDiv = document.createElement('div');
                betDiv.textContent = `${bet.game}: Bet on ${bet.team} at ${bet.odds}`;
                slipContent.appendChild(betDiv);
            });
        }
        document.getElementById('place-bet').addEventListener('click', () => {
            console.log('Placing bet:', bets);
            // Here you would add the code to handle the bet placement,
            // including calling the ML model to get the prediction
        });
    </script>
</body>
</html>