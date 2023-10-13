# temperatureC
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
</head>
<body>

    <h1>Temperature Converter</h1>

    <form>
        <label for="celsius">Celsius:</label>
        <input type="number" id="celsius" placeholder="Enter Celsius" oninput="convert('celsius')">

        <label for="fahrenheit">Fahrenheit:</label>
        <input type="number" id="fahrenheit" placeholder="Enter Fahrenheit" oninput="convert('fahrenheit')">
    </form>

    <script>
        function convert(unit) {
            if (unit === 'celsius') {
                let celsius = document.getElementById('celsius').value;
                let fahrenheit = (celsius * 9/5) + 32;
                document.getElementById('fahrenheit').value = fahrenheit.toFixed(2);
            } else if (unit === 'fahrenheit') {
                let fahrenheit = document.getElementById('fahrenheit').value;
                let celsius = (fahrenheit - 32) * 5/9;
                document.getElementById('celsius').value = celsius.toFixed(2);
            }
        }
    </script>

</body>
</html>
