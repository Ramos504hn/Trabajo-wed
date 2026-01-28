<!DOCTYPE html>
<html>
<head>
    <title>Mi App de Gatitos</title>
    <style>
        body { font-family: sans-serif; text-align: center; background: #f0f0f0; }
        button { padding: 10px 20px; font-size: 16px; cursor: pointer; border-radius: 5px; }
    </style>
</head>
<body>
    <h1>Generador de Saludos</h1>
    <button onclick="saludar()">¡Haz clic aquí!</button>
    <p id="mensaje"></p>

    <script>
        function saludar() {
            document.getElementById("mensaje").innerText = "¡Hola! Tu app está funcionando 🚀";
        }
    </script>
</body>
</html>
