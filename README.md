<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperaturas da Semana</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
            background-color: #e1f5fe;
        }
        table {
            margin: 0 auto;
            border-collapse: collapse;
            width: 70%;
        }
        th, td {
            border: 1px solid #0288d1;
            padding: 10px;
            font-size: 16px;
        }
        th {
            background-color: #0288d1;
            color: white;
        }
        tr:nth-child(even) {
            background-color: #b3e5fc;
        }
        input {
            width: 60px;
            padding: 5px;
            text-align: center;
        }
    </style>
</head>
<body>
    <h1>Temperaturas da Semana</h1>
    <table>
        <tr>
            <th>Dia</th>
            <th>Temperatura (°C)</th>
            <th>Temperatura (°F)</th>
        </tr>
        <tr>
            <td>Segunda-feira</td>
            <td><input type="number" id="seg" oninput="atualizarFahrenheit('seg', 'fseg')" value="20"></td>
            <td id="fseg">68</td>
        </tr>
        <tr>
            <td>Terça-feira</td>
            <td><input type="number" id="ter" oninput="atualizarFahrenheit('ter', 'fter')" value="22"></td>
            <td id="fter">71.6</td>
        </tr>
        <tr>
            <td>Quarta-feira</td>
            <td><input type="number" id="qua" oninput="atualizarFahrenheit('qua', 'fqua')" value="19"></td>
            <td id="fqua">66.2</td>
        </tr>
        <tr>
            <td>Quinta-feira</td>
            <td><input type="number" id="qui" oninput="atualizarFahrenheit('qui', 'fqui')" value="24"></td>
            <td id="fqui">75.2</td>
        </tr>
        <tr>
            <td>Sexta-feira</td>
            <td><input type="number" id="sex" oninput="atualizarFahrenheit('sex', 'fsex')" value="21"></td>
            <td id="fsex">69.8</td>
        </tr>
        <tr>
            <td>Sábado</td>
            <td><input type="number" id="sab" oninput="atualizarFahrenheit('sab', 'fsab')" value="23"></td>
            <td id="fsab">73.4</td>
        </tr>
        <tr>
            <td>Domingo</td>
            <td><input type="number" id="dom" oninput="atualizarFahrenheit('dom', 'fdom')" value="18"></td>
            <td id="fdom">64.4</td>
        </tr>
    </table>

    <script>
        function atualizarFahrenheit(celsiusId, fahrenheitId) {
            let celsius = document.getElementById(celsiusId).value;
            let fahrenheit = (parseFloat(celsius) * 9/5) + 32;
            document.getElementById(fahrenheitId).innerText = fahrenheit.toFixed(1);
        }
    </script>
</body>
</html>
