!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Roblox Login</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="login-container">
        <h2>Login to Roblox Fan Hub</h2>
        <form id="loginForm">
            <input type="text" id="username" placeholder="Enter Username" required>
            <input type="password" id="password" placeholder="Enter Password" required>
            <button type="submit">Login</button>
        </form>
        <p id="error-message"></p>
    </div>

    <script src="script.js"></script>
</body>
</html
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    text-align: center;
}

.login-container {
    background: white;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    width: 300px;
    margin: 100px auto;
}

h2 {
    color: #333;
}

input {
    width: 90%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    background-color: #ff4747;
    color: white;
    padding: 10px;
    border: none;
    width: 100%;
    cursor: pointer;
    border-radius: 5px;
}

button:hover {
    background-color: #ff2020;
}

#error-message {
    color: red;
    font-size: 14px;
}
document.getElementById("loginForm").addEventListener("submit", function(event) {
    event.preventDefault(); // Prevents page reload

    // Get input values
    let username = document.getElementById("username").value;
    let password = document.getElementById("password").value;

    // Simple username and password (for testing)
    let correctUsername = "RobloxFan";
    let correctPassword = "1234";

    // Check if login is correct
    if (username === correctUsername && password === correctPassword) {
        alert("Login successful! Welcome, " + username);
        window.location.href = "home.html"; // Redirect to home page (create home.html)
    } else {
        document.getElementById("error-message").innerText = "Invalid username or password!";
    }
});
