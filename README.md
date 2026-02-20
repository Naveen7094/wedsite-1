# AI-BASED-FERTILIZER-RECOMMENDATIONS-SYSTEM
fertilizer-ai/
│
├── login.html
├── register.html
├── dashboard.html
├── style.css
├── script.js
└── images/
     ├── urea.jpg
     ├── dap.jpg
     ├── potash.jpg
     ├── compost.jpg
     ├── npk.jpg
<!DOCTYPE html>
<html>
<head>
    <title>Login - AI Fertilizer System</title>
    <link rel="stylesheet" href="style.css">
</head>
<body class="login-body">

    <div class="login-container">
        <h2>AI Fertilizer Recommendation</h2>

        <form onsubmit="return loginUser()">
            <input type="text" id="username" placeholder="Username" required>
            <input type="password" id="password" placeholder="Password" required>
            <button type="submit">Login</button>
        </form>

        <p>New User? <a href="register.html">Register Here</a></p>
    </div>
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
<!DOCTYPE html>
<html>
<head>
    <title>AI Fertilizer Recommendation</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>AI Based Fertilizer Recommendation System</h1>
</header>

<div class="container">

    <h2>Enter Soil Details</h2>

    <input type="number" id="nitrogen" placeholder="Nitrogen (N)">
    <input type="number" id="phosphorus" placeholder="Phosphorus (P)">
    <input type="number" id="potassium" placeholder="Potassium (K)">
    <input type="number" id="ph" placeholder="pH Value">
    <input type="text" id="crop" placeholder="Crop Type">

    <button onclick="recommendFertilizer()">Get Recommendation</button>

    <h3 id="result"></h3>

</div>

<hr>

<h2 style="text-align:center;">Available Fertilizer Products</h2>

<div class="products">

    <div class="card">
        <img src="images/urea.jpg">
        <h3>Urea</h3>
    </div>

    <div class="card">
        <img src="images/dap.jpg">
        <h3>DAP</h3>
    </div>

    <div class="card">
        <img src="images/potash.jpg">
        <h3>Potash</h3>
    </div>

    <div class="card">
        <img src="images/compost.jpg">
        <h3>Organic Compost</h3>
    </div>

    <div class="card">
        <img src="images/npk.jpg">
        <h3>NPK 20-20-20</h3>
    </div>

</div>

<script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial;
    margin: 0;
    padding: 0;
    background: #f4f4f4;
}

header {
    background: green;
    color: white;
    padding: 15px;
    text-align: center;
}

.container {
    text-align: center;
    padding: 20px;
}

input {
    display: block;
    margin: 10px auto;
    padding: 8px;
    width: 250px;
}

button {
    padding: 10px 20px;
    background: green;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background: darkgreen;
}

.products {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    padding: 20px;
}

.card {
    background: white;
    padding: 15px;
    width: 180px;
    box-shadow: 0 0 10px gray;
    text-align: center;
}

.card img {
    width: 100%;
    height: 120px;
}

/* Login Page */
.login-body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.login-container {
    background: white;
    padding: 30px;
    box-shadow: 0 0 15px gray;
    text-align: center;
}
// REGISTER FUNCTION
function registerUser() {
    let user = document.getElementById("newUser").value;
    let pass = document.getElementById("newPass").value;

    localStorage.setItem("username", user);
    localStorage.setItem("password", pass);

    alert("Registration Successful!");
    window.location.href = "login.html";
    return false;
}

// LOGIN FUNCTION
function loginUser() {
    let user = document.getElementById("username").value;
    let pass = document.getElementById("password").value;

    let storedUser = localStorage.getItem("username");
    let storedPass = localStorage.getItem("password");

    if (user === storedUser && pass === storedPass) {
        alert("Login Successful!");
        window.location.href = "dashboard.html";
    } else {
        alert("Invalid Credentials!");
    }

    return false;
}

// AI FERTILIZER RECOMMENDATION LOGIC
function recommendFertilizer() {
    let n = parseInt(document.getElementById("nitrogen").value);
    let p = parseInt(document.getElementById("phosphorus").value);
    let k = parseInt(document.getElementById("potassium").value);
    let ph = parseFloat(document.getElementById("ph").value);
    let crop = document.getElementById("crop").value.toLowerCase();

    let result = "";

    if (n < 50) {
        result = "Recommended: Urea (Nitrogen Deficiency)";
    }
    else if (p < 40) {
        result = "Recommended: DAP (Phosphorus Deficiency)";
    }
    else if (k < 40) {
        result = "Recommended: Potash (Potassium Deficiency)";
    }
    else if (ph < 6) {
        result = "Recommended: Lime Treatment (Low pH)";
    }
    else {
        result = "Recommended: NPK 20-20-20 Balanced Fertilizer";
    }

    document.getElementById("result").innerHTML = result;
}

<script src="script.js"></script>
</body>
</html>
