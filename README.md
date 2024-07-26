<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lobster Calculator</title>
    <style>
        body {
            background-image: url('https://raw.githubusercontent.com/sigongan/lobster-calculator2/main/images/3mm8ar9f.png');
            background-size: cover;
            background-repeat: no-repeat;
            background-attachment: fixed;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: 'Arial', sans-serif;
        }
        .container {
            background-color: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }
        h1 {
            font-size: 36px;
            margin-bottom: 20px;
        }
        label {
            font-size: 24px;
            display: block;
            margin-bottom: 5px;
        }
        input {
            font-size: 18px;
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            font-size: 24px;
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        #result {
            margin-top: 20px;
            font-size: 24px;
            color: #333;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Lobster Calculator</h1>
        <form id="lobsterForm">
            <label for="weight">Lobster Weight (grams):</label>
            <input type="number" id="weight" name="weight" step="0.01" required>
            <button type="submit">Calculate</button>
        </form>
        <div id="result"></div>
    </div>
    <script>
        document.getElementById('lobsterForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const weightInGrams = parseFloat(document.getElementById('weight').value);
            const weightInKg = weightInGrams / 1000;
            const pricePerKg = 160;
            const laborCost = 20;
            const totalPrice = (weightInKg * pricePerKg) + laborCost;
            document.getElementById('result').textContent = `Total Price: ${totalPrice.toLocaleString()} AUD`;
        });
    </script>
</body>
</html>
