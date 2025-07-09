<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login - CampBridge</title>
  <style>
    body {
      background-color: #f2f2f2;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .login-box {
      background-color: #ffffff;
      padding: 40px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      width: 100%;
      max-width: 360px;
    }

    .login-box h2 {
      text-align: center;
      color: #2C7CEE;
      margin-bottom: 24px;
    }

    input[type="email"],
    input[type="password"] {
      width: 100%;
      padding: 12px;
      margin-bottom: 16px;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1rem;
    }

    button {
      width: 100%;
      padding: 12px;
      background-color: #2C7CEE;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 1rem;
      cursor: pointer;
    }

    button:hover {
      background-color: #1a5ac8;
    }

    .note {
      font-size: 0.9rem;
      text-align: center;
      margin-top: 16px;
      color: #666;
    }

    .logout-box {
      display: none;
      background-color: #ffffff;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      text-align: center;
      max-width: 360px;
    }

    .logout-box p {
      margin-bottom: 16px;
      font-size: 1.1rem;
    }
  </style>
</head>
<body>

<div class="login-box" id="loginBox">
  <h2>CampBridge Login</h2>
  <form onsubmit="handleLogin(event)">
    <input type="email" placeholder="Email" required>
    <input type="password" placeholder="Password" required>
    <button type="submit">Login</button>
  </form>
  <div class="note">Not real yet – will connect to dashboard in future.</div>
</div>

<div class="logout-box" id="logoutBox">
  <p>Welcome back to CampBridge!</p>
  <button onclick="handleLogout()">Sign Out</button>
</div>

<script>
  function handleLogin(event) {
    event.preventDefault();
    document.getElementById("loginBox").style.display = "none";
    document.getElementById("logoutBox").style.display = "block";
  }

  function handleLogout() {
    document.getElementById("logoutBox").style.display = "none";
    document.getElementById("loginBox").style.display = "block";
  }
</script>

</body>
</html>
