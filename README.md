<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Presentación - Mario Enrique</title>
    <style>
        :root {
            --primary: #2563eb;
            --bg: #f8fafc;
            --card: #ffffff;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }

        .card {
            background: var(--card);
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            width: 100%;
            max-width: 400px;
            text-align: center;
        }

        .profile-pic {
            width: 100px;
            height: 100px;
            background: var(--primary);
            border-radius: 50%;
            margin: 0 auto 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2rem;
            font-weight: bold;
        }

        h1 {
            color: #1e293b;
            margin-bottom: 0.5rem;
        }

        p {
            color: #64748b;
            margin-bottom: 1.5rem;
        }

        textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #e2e8f0;
            border-radius: 10px;
            resize: none;
            box-sizing: border-box;
            margin-bottom: 1rem;
        }

        button {
            background: var(--primary);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
            transition: background 0.3s;
            width: 100%;
        }

        button:hover {
            background: #1d4ed8;
        }

        #status {
            margin-top: 1rem;
            font-size: 0.9rem;
            color: #10b981;
            display: none;
        }
    </style>
</head>
<body>

    <div class="card">
        <div class="profile-pic">ME</div>
        <h1>Mario Enrique</h1>
        <p>Desarrollador & Entusiasta del Código</p>
        
        <hr style="border: 0; border-top: 1px solid #eee; margin-bottom: 1.5rem;">

        <textarea id="messageInput" rows="4" placeholder="Escribe un mensaje para Mario..."></textarea>
        <button onclick="sendMessage()">Enviar Mensaje</button>
        
        <div id="status">¡Mensaje enviado con éxito! 🚀</div>
    </div>

    <script>
        function sendMessage() {
            const msg = document.getElementById('messageInput').value;
            const status = document.getElementById('status');

            if (msg.trim() === "") {
                alert("Por favor, escribe algo antes de enviar.");
                return;
            }

            // Simulación de envío
            console.log("Mensaje para Mario Enrique:", msg);
            
            status.style.display = "block";
            document.getElementById('messageInput').value = "";

            setTimeout(() => {
                status.style.display = "none";
            }, 3000);
        }
    </script>

</body>
</html>

