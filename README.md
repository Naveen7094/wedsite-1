# AI-BASED-FERTILIZER-RECOMMENDATIONS-SYSTEM
ai-fertilizer-recommendation-system/
│
├── index.html
├── login.html
├── register.html
├── style.css
├── script.js
├── README.md
└── images/
     ├── urea.jpg
     ├── dap.jpg
     ├── potash.jpg
     ├── compost.jpg
     ├── npk.jpg
<!DOCTYPE html>
<html>
<head>
    <title>AI Fertilizer Recommendation System</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>AI Based Fertilizer Recommendation System</h1>
</header>

<div class="container">
    <h2>Enter Soil Details</h2>

    <input type="number" id="nitrogen" placeholder="Nitrogen (N)" required>
    <input type="number" id="phosphorus" placeholder="Phosphorus (P)" required>
    <input type="number" id="potassium" placeholder="Potassium (K)" required>
    <input type="number" id="ph" placeholder="pH Value" required>
    <input type="text" id="crop" placeholder="Crop Type" required>

    <button onclick="recommendFertilizer()">Get Recommendation</button>

    <h3 id="result"></h3>
</div>

<hr>

<h2 class="center">Available Fertilizer Products</h2>

<div class="products">
    <div class="card">
        <img src="images/urea.jpg" alt="Urea">
        <h3>Urea</h3>
    </div>

    <div class="card">
        <img src="images/dap.jpg" alt="DAP">
        <h3>DAP</h3>
    </div>

    <div class="card">
        <img src="images/potash.jpg" alt="Potash">
        <h3>Potash</h3>
    </div>

    <div class="card">
        <img src="images/compost.jpg" alt="Compost">
        <h3>Organic Compost</h3>
    </div>

    <div class="card">
        <img src="images/npk.jpg" alt="NPK">
        <h3>NPK 20-20-20</h3>
    </div>
</div>

<script src="script.js"></script>
</body>
</html>
