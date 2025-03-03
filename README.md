<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        .calculator {
            width: 200px;
            padding: 10px;
            background: white;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }
        #display {
            width: 100%;
            height: 40px;
            font-size: 1.5rem;
            text-align: right;
            margin-bottom: 10px;
        }
        .buttons button {
            width: 45px;
            height: 45px;
            font-size: 1.2rem;
            margin: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <input type="text" id="display" disabled>
        <div class="buttons">
            <button onclick="clearDisplay()">C</button>
            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('+')">+</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('-')">-</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('*')">*</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('0')">0</button>
            <button onclick="calculateResult()">=</button>
            <button onclick="appendValue('/')">/</button>
        </div>
    </div>
    <script>
        function appendValue(value) {
            document.getElementById("display").value += value;
        }
        function clearDisplay() {
            document.getElementById("display").value = "";
        }
        function calculateResult() {
            try {
                document.getElementById("display").value = eval(document.getElementById("display").value);
            } catch {
                document.getElementById("display").value = "Error";
            }
        }
    </script>
</body>
</html>
