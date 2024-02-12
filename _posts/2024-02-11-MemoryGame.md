
<html lang="en"><head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Emoji Memory Game</title>
<style>
  .grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    margin: 20px auto;
    max-width: 600px;
  }
  .card {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100px;
    background-color: #f0f0f0;
    font-size: 2rem;
    cursor: pointer;
  }
  .hidden {
    background-color: #9e9e9e;
  }
</style>
</head>
<body>