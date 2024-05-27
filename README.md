<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pregunta Importante</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #0d0d0d;
            color: #ff69b4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            text-align: center;
            border: 2px solid #ff1493;
            border-radius: 15px;
            padding: 20px;
            background: linear-gradient(145deg, #1a1a1a, #0d0d0d);
            box-shadow: 10px 10px 20px #080808, -10px -10px 20px #141414;
        }
        h1 {
            color: #ff1493;
            text-shadow: 0 0 10px #ff1493;
        }
        input[type="text"] {
            padding: 10px;
            border: 2px solid #ff1493;
            border-radius: 5px;
            width: 80%;
            margin-bottom: 20px;
            background-color: #1a1a1a;
            color: #ff69b4;
            box-shadow: inset 2px 2px 5px #0d0d0d, inset -2px -2px 5px #1f1f1f;
        }
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            background-color: #ff1493;
            color: white;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s ease;
            box-shadow: 0 0 10px #ff1493, 0 0 20px #ff1493;
        }
        button:hover {
            background-color: #ff69b4;
            box-shadow: 0 0 20px #ff69b4, 0 0 30px #ff69b4;
        }
        #response {
            margin-top: 20px;
            font-size: 18px;
            color: #ff69b4;
            text-shadow: 0 0 10px #ff69b4;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Queres salir conmigo?</h1>
        <input type="text" id="responseInput" placeholder="Escribe si o no">
        <button onclick="checkResponse()">Enviar</button>
        <div id="response"></div>
    </div>

    <script>
        function checkResponse() {
            const input = document.getElementById('responseInput').value.toLowerCase();
            const response = document.getElementById('response');
            if (input === 'no') {
                response.textContent = 'Invalido';
                response.style.color = '#ff0000';
            } else if (input === 'si') {
                response.textContent = 'ya se';
                response.style.color = '#32cd32';
            } else {
                response.textContent = 'Si o no carajo';
                response.style.color = '#ffa500';
            }
        }
    </script>
</body>
</html>
