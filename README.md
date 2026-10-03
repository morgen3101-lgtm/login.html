<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>NEXORA - Login</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #eef0ff, #f8f9ff);
    }

    .container {
      width: 100%;
      max-width: 420px;
      padding: 20px;
    }

    .login-card {
      background: white;
      padding: 35px;
      border-radius: 24px;
      box-shadow: 0 15px 45px rgba(40, 45, 90, 0.12);
    }

    .logo {
      text-align: center;
      font-size: 34px;
      font-weight: 800;
      color: #5b5cf0;
      margin-bottom: 8px;
    }

    .subtitle {
      text-align: center;
      color: #8991a3;
      font-size: 14px;
      margin-bottom: 30px;
    }

    .input-group {
      margin-bottom: 17px;
    }

    label {
      display: block;
      margin-bottom: 7px;
      font-size: 14px;
      font-weight: 600;
      color: #343b4d;
    }

    input {
      width: 100%;
      padding: 14px;
      border: 1px solid #e1e4ec;
      border-radius: 12px;
      outline: none;
      font-size: 15px;
      transition: 0.2s;
    }

    input:focus {
      border-color: #5b5cf0;
      box-shadow: 0 0 0 3px rgba(91, 92, 240, 0.1);
    }

    .password-row {
      position: relative;
    }

    .show-password {
      position: absolute;
      right: 14px;
      top: 14px;
      border: none;
      background: transparent;
      color: #777f91;
      cursor: pointer;
    }

    .forgot {
      display: block;
      text-align: right;
      margin: 5px 0 20px;
      color: #5b5cf0;
      font-size: 13px;
      text-decoration: none;
    }

    .login-button {
      width: 100%;
      padding: 14px;
      border: none;
      border-radius: 12px;
      background: linear-gradient(135deg, #5b5cf0, #7c3aed);
      color: white;
      font-size: 16px;
      font-weight: bold;
      cursor: pointer;
    }

    .login-button:hover {
      opacity: 0.92;
    }

    .divider {
      display: flex;
      align-items: center;
      gap: 10px;
      margin: 25px 0;
      color: #a0a6b5;
      font-size: 12px;
    }

    .divider::before,
    .divider::after {
      content: "";
      flex: 1;
      height: 1px;
      background: #e7e9ef;
    }

    .create-account {
      width: 100%;
      display: block;
      text-align: center;
      padding: 13px;
      border: 1px solid #5b5cf0;
      border-radius: 12px;
      color: #5b5cf0;
      text-decoration: none;
      font-weight: bold;
    }

    .back {
      display: block;
      text-align: center;
      margin-top: 20px;
      color: #8991a3;
      text-decoration: none;
      font-size: 13px;
    }
  </style>
</head>

<body>

  <div class="container">

    <div class="login-card">

      <div class="logo">
        NEXORA
      </div>

      <div class="subtitle">
        Connect · Share · Discover
      </div>

      <form onsubmit="login(event)">

        <div class="input-group">
          <label>Email</label>

          <input
            type="email"
            id="email"
            placeholder="Enter your email"
            required
          >
        </div>

        <div class="input-group">

          <label>Password</label>

          <div class="password-row">

            <input
              type="password"
              id="password"
              placeholder="Enter your password"
              required
            >

            <button
              type="button"
              class="show-password"
              onclick="togglePassword()"
            >
              👁
            </button>

          </div>

        </div>

        <a href="#" class="forgot">
          Forgot password?
        </a>

        <button
          type="submit"
          class="login-button"
        >
          Log In
        </button>

      </form>

      <div class="divider">
        OR
      </div>

      <a href="#" class="create-account">
        Create New Account
      </a>

      <a href="index.html" class="back">
        ← Back to NEXORA
      </a>

    </div>

  </div>


  <script>

    function togglePassword() {

      const password =
        document.getElementById("password");

      if (password.type === "password") {

        password.type = "text";

      } else {

        password.type = "password";

      }

    }


    function login(event) {

      event.preventDefault();

      alert(
        "Login interface ready. Real authentication will be added next."
      );

    }

  </script>

</body>
</html>
