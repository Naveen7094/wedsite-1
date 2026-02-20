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
<!DOCTYPE html>
<html>
<head>
    <title>Login</title>
    <link rel="stylesheet" href="style.css">
</head>
<body class="login-body">

<div class="login-container">
    <h2>Login</h2>

    <form onsubmit="return loginUser()">
        <input type="text" id="username" placeholder="Username" required>
        <input type="password" id="password" placeholder="Password" required>
        <button type="submit">Login</button>
    </form>

    <p>New User? <a href="register.html">Register Here</a></p>
</div>

<script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html>
<head>
    <title>Register</title>
    <link rel="stylesheet" href="style.css">
</head>
<body class="login-body">

<div class="login-container">
    <h2>Register</h2>

    <form onsubmit="return registerUser()">
        <input type="text" id="newUser" placeholder="Username" required>
        <input type="password" id="newPass" placeholder="Password" required>
        <button type="submit">Register</button>
    </form>

    <p><a href="login.html">Back to Login</a></p>
</div>

<script src="script.js"></script>
</body>
</html>
</body>
</html>
