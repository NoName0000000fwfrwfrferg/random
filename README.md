<!DOCTYPE html>
<html lang="kk">
<head>
    <title>game</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Рандом ойын</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #007BFF;
            color: white;
            padding: 20px;
        }
        .game {
            margin: 20px auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 10px;
            max-width: 400px;
            background-color: #fff;
        }
        .game button {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .game button:hover {
            background-color: #0056b3;
        }
        .result {
            margin-top: 20px;
            font-size: 18px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <header>
        <h1>Рандом ойын</h1>
    </header>
    <div class="game">
        <h2>Болжам жасаңыз!</h2>
        <p>1 мен 10 аралығындағы санды табыңыз.</p>
        <button onclick="playGame()">Сан таңдау</button>
        <div class="result" id="result">Нәтиже осында шығады</div>
    </div>
    <footer>
        <p>Барлық құқықтар қорғалған &copy; 2025</p>
    </footer>

    <script>
        function playGame() {
            const randomNumber = Math.floor(Math.random() * 10) + 1;
            const userGuess = prompt("1 мен 10 аралығындағы санды енгізіңіз:");
            
            if (userGuess == randomNumber) {
                document.getElementById("result").textContent = `Құттықтаймын! Сіз дұрыс таптыңыз: ${randomNumber}`;
            } else {
                document.getElementById("result").textContent = `Кешіріңіз, дұрыс жауап: ${randomNumber}`;
            }
        }
    </script>
</body>
</html>

