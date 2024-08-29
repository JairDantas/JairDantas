<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tela de Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            margin: 0;
        }
        .login-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 300px;
            width: 100%;
        }
        .login-container h2 {
            margin: 0 0 15px;
            font-size: 24px;
            text-align: center;
        }
        .login-container input {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            border: 1px solid #ddd;
            border-radius: 5px;
            box-sizing: border-box;
        }
        .login-container button {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
        }
        .login-container button:hover {
            background-color: #0056b3;
        }
        .message {
            margin-top: 10px;
            text-align: center;
            font-size: 16px;
            color: red;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h2>Login</h2>
        <input type="text" id="username" placeholder="Usuário">
        <input type="password" id="password" placeholder="Senha">
        <button onclick="validateLogin()">Entrar</button>
        <div id="message" class="message"></div>
    </div>

    <script>
        function validateLogin() {
            // Usuário e senha corretos para validação
            const correctUsername = "admin";
            const correctPassword = "password123";

            // Obter os valores dos campos
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;

            // Mensagem de feedback
            const messageElement = document.getElementById("message");

            // Validar usuário e senha
            if (username === correctUsername && password === correctPassword) {
                messageElement.textContent = "Login efetuado com sucesso";
                messageElement.style.color = "green";
            } else {
                messageElement.textContent = "Erro: usuário e senha não encontrados";
                messageElement.style.color = "red";
            }
        }
    </script>
</body>
</html>
