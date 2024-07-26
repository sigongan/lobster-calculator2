 <style>
        body {
           background-image: url('https://github.com/sigongan/lobster-calculator2/blob/main/images/3mm8ar9f.png?raw=true');
        background-size: cover;
        background-repeat: no-repeat;
        background-attachment: fixed;
            background-size: cover;
            background-repeat: no-repeat;
            background-attachment: fixed;
            padding: 0;
            display: flex;
            justify-content: center;
@@ -73,7 +73,7 @@
    <div class="container">
        <h1>Lobster Calculator</h1>
        <form id="lobsterForm">
            <label for="weight">Lobster Weight (kg):</label>
            <label for="weight">Lobster Weight (grams):</label>
            <input type="number" id="weight" name="weight" step="0.01" required>
            
            <button type="submit">Calculate</button>
@@ -84,16 +84,16 @@
        document.getElementById('lobsterForm').addEventListener('submit', function(event) {
            event.preventDefault();
            
            const weight = parseFloat(document.getElementById('weight').value);
            const weightInGrams = parseFloat(document.getElementById('weight').value);
            const weightInKg = weightInGrams / 1000; // Convert grams to kilograms
            const pricePerKg = 160; // Price per kilogram (AUD)
            const laborCost = 20; // Labor cost (AUD)
            
            const totalPrice = (weight * pricePerKg) + laborCost;
            const totalPrice = (weightInKg * pricePerKg) + laborCost;
            
            document.getElementById('result').textContent = `Total Price: ${totalPrice.toLocaleString()} AUD`;
        });
    </script>
</body>
</html>
