<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SYSTEM FAILURE - CRITICAL</title>
    <style>
        body {
            background-color: black;
            color: #00FF00; /* Verde Terminal clássico */
            font-family: 'Courier New', Courier, monospace;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
            /* Animação de piscar vermelho apenas no início (2 segundos) */
            animation: initialFlash 2s steps(1) 1;
        }

        /* Define a piscada vermelha inicial */
        @keyframes initialFlash {
            0%, 20%, 40% { background-color: red; }
            10%, 30%, 50% { background-color: black; }
            100% { background-color: black; }
        }

        .container {
            text-align: center;
            max-width: 80%;
        }

        /* Estilo para as imagens reais */
        .hacker-image {
            max-width: 250px;
            height: auto;
            margin: 20px auto;
            display: block;
            border: 2px solid #00FF00;
            box-shadow: 0 0 15px #00FF00;
            /* Efeito de glitch suave nas imagens */
            animation: imgGlitch 3s infinite;
        }

        @keyframes imgGlitch {
            0% { transform: translate(0,0); opacity: 1; }
            95% { transform: translate(0,0); opacity: 1; }
            96% { transform: translate(5px, -2px); opacity: 0.8; }
            97% { transform: translate(-5px, 2px); opacity: 0.8; }
            98% { transform: translate(0,0); opacity: 1; }
        }

        .terminal-text {
            text-align: left;
            margin-bottom: 30px;
            display: inline-block;
        }

        .line {
            margin-bottom: 8px;
            white-space: nowrap;
            overflow: hidden;
            border-right: 2px solid #00FF00;
            /* Começa invisível para o delay da digitação */
            width: 0; 
            animation: typing 1.5s steps(30, end) forwards, blink-caret .75s step-end infinite;
        }

        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }

        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #00FF00; }
        }

        .danger-text { color: red; font-weight: bold; }
        .success-text { color: cyan; }

        /* Estilo do texto grande */
        .perdeu-playboy {
            font-size: 8vw; /* Tamanho responsivo baseado na largura da tela */
            color: #FF0000; /* Vermelho Alerta */
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 10px;
            text-shadow: 0 0 20px red;
            margin-top: 30px;
            animation: pulse 1s ease-in-out infinite alternate;
        }

        @keyframes pulse {
            from { transform: scale(1); opacity: 0.7; }
            to { transform: scale(1.05); opacity: 1; }
        }
    </style>
</head>
<body>

    <div class="container">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a6/Anonymous_emblem.svg" alt="Anonymous" class="hacker-image">

        <div class="terminal-text">
            <div class="line" style="animation-delay: 2.5s;">> ACESSANDO NÚCLEO...</div>
            <div class="line" style="animation-delay: 4.0s;">> <span class="danger-text">CRITICAL: Firewall Bypass: SUCCESS</span></div>
            <div class="line" style="animation-delay: 5.5s;">> Extraindo Hash de Administrador... [OK]</div>
            <div class="line" style="animation-delay: 7.0s;">> <span class="success-text">SISTEMA COMPROMETIDO.</span></div>
        </div>

        <div class="perdeu-playboy">PERDEU PLAYBOY</div>

        <img src="https://cdn.pixabay.com/photo/2017/01/31/15/34/icon-2025118_1280.png" alt="Skull" class="hacker-image" style="max-width: 150px; animation-delay: 1s;">
    </div>

</body>
</html>
