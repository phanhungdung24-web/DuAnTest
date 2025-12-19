<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>Form Đăng Nhập</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f2f2f2;
        }
        .login-box {
            width: 300px;
            margin: 100px auto;
            padding: 20px;
            background: white;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h2 {
            text-align: center;
        }
        input {
            width: 100%;
            padding: 8px;
            margin: 8px 0;
        }
        button {
            width: 100%;
            padding: 8px;
            background: #007bff;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background: #0056b3;
        }
        .message {
            text-align: center;
            margin-top: 10px;
            color: red;
        }
    </style>
</head>
<body>

<div class="login-box">
    <h2>Đăng nhập</h2>
    <input type="text" id="username" placeholder="Tên đăng nhập">
    <input type="password" id="password" placeholder="Mật khẩu">
    <button onclick="login()">Đăng nhập</button>
    <div class="message" id="message"></div>
</div>

<script>
    function login() {
        const user = document.getElementById("username").value;
        const pass = document.getElementById("password").value;

        // Tài khoản demo
        if (user === "admin" && pass === "123456") {
            document.getElementById("message").style.color = "green";
            document.getElementById("message").innerText = "Đăng nhập thành công!";
        } else {
            document.getElementById("message").innerText = "Sai tài khoản hoặc mật khẩu!";
        }
    }
</script>

</body>
</html>
