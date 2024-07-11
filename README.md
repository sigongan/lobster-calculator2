<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lobster Calculator</title>
    <link href="https://fonts.googleapis.com/css2?family=Cute+Font&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Cute Font', cursive;
            background: url('images/3mm8ar9f.png') no-repeat center center fixed;
            background-size: cover;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
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
            <label for="weight">Lobster Weight (kg):</label>
            <input type="number" id="weight" name="weight" step="0.01" required>
            
            <button type="submit">Calculate</button>
        </form>
        <div id="result"></div>
    </div>
    <script>
        document.getElementById('lobsterForm').addEventListener('submit', function(event) {
            event.preventDefault();
            
            const weight = parseFloat(document.getElementById('weight').value);
            const pricePerKg = 160; // Price per kilogram (AUD)
            const laborCost = 20; // Labor cost (AUD)
            
            const totalPrice = (weight * pricePerKg) + laborCost;
            
            document.getElementById('result').textContent = `Total Price: ${totalPrice.toLocaleString()} AUD`;
        });
    </script>
</body>
</html>


