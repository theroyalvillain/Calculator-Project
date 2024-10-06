# CodeAlpha-Projects
# calculator-program
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
        }
        .calculator {
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.1);
        }
        #result {
            width: 100%;
            height: 50px;
            text-align: right;
            margin-bottom: 20px;
            font-size: 24px;
            padding-right: 10px;
            border: 2px solid #ccc;
            border-radius: 5px;
        }
        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-gap: 10px;
        }
        button {
            padding: 20px;
            font-size: 20px;
            border: none;
            background-color: #f0f0f0;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #d1d1d1;
        }
        .equal {
            background-color: #4CAF50;
            color: white;
        }
        .equal:hover {
            background-color: #45a049;
        }
        .clear {
            background-color: #f44336;
            color: white;
        }
        .clear:hover {
            background-color: #d32f2f;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="result" disabled>
        <div class="buttons">
            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('/')">/</button>
            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="appendValue('*')">*</button>
            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="appendValue('-')">-</button>
            <button onclick="appendValue('0')">0</button>
            <button onclick="appendValue('.')">.</button>
            <button onclick="calculate()" class="equal">=</button>
            <button onclick="appendValue('+')">+</button>
            <button onclick="clearResult()" class="clear">C</button>
        </div>
    </div>

    <script>
        function appendValue(value) {
            document.getElementById("result").value += value;
        }

        function calculate() {
            let result = document.getElementById("result").value;
            if (result) {
                document.getElementById("result").value = eval(result);
            }
        }

        function clearResult() {
            document.getElementById("result").value = '';
        }
    </script>
</body>
</html>
