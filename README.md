<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lobster Calculator</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

        body {
            background-image: url('https://images.unsplash.com/photo-1529121262420-fd3bfe5c54d1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-repeat: no-repeat;
            background-attachment: fixed;
            margin: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: 'Roboto', sans-serif;
            color: #333;
        }
        .container {
            background-color: rgba(255, 255, 255, 0.9);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
            width: 340px;
            text-align: center;
            transition: transform 0.3s ease-in-out;
        }
        .container:hover {
            transform: translateY(-10px);
        }
        h1 {
            font-size: 36px;
            margin-bottom: 20px;
            font-weight: 700;
            color: #0056b3;
        }
        label {
            font-size: 20px;
            display: block;
            margin-bottom: 5px;
            font-weight: 700;
        }
        input {
            font-size: 18px;
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }
        button {
            font-size: 20px;
            width: 100%;
            padding: 12px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
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
