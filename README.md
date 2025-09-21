[Feliz Día.html](https://github.com/user-attachments/files/22454121/Feliz.Dia.html)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Feliz Día</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: center;
            background: #000033; /* Fondo azul oscuro para noche */
            overflow: hidden;
            position: relative;
        }

        /* Estrellas en el fondo */
        .stars {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        .star {
            position: absolute;
            background: white;
            border-radius: 50%;
            opacity: 0.8;
            animation: twinkle 1.5s infinite alternate;
        }

        @keyframes twinkle {
            from { opacity: 0.5; }
            to { opacity: 1; }
        }

        /* Generar estrellas aleatorias */
        .star:nth-child(1) { top: 10%; left: 20%; width: 2px; height: 2px; animation-delay: 0s; }
        .star:nth-child(2) { top: 15%; left: 50%; width: 3px; height: 3px; animation-delay: 0.5s; }
        .star:nth-child(3) { top: 20%; left: 80%; width: 1px; height: 1px; animation-delay: 1s; }
        .star:nth-child(4) { top: 30%; left: 10%; width: 2px; height: 2px; animation-delay: 0.2s; }
        .star:nth-child(5) { top: 40%; left: 40%; width: 3px; height: 3px; animation-delay: 0.8s; }
        .star:nth-child(6) { top: 50%; left: 70%; width: 1px; height: 1px; animation-delay: 1.2s; }
        .star:nth-child(7) { top: 60%; left: 30%; width: 2px; height: 2px; animation-delay: 0.4s; }
        .star:nth-child(8) { top: 70%; left: 60%; width: 3px; height: 3px; animation-delay: 1s; }
        .star:nth-child(9) { top: 80%; left: 90%; width: 1px; height: 1px; animation-delay: 0.6s; }
        .star:nth-child(10) { top: 90%; left: 15%; width: 2px; height: 2px; animation-delay: 1.4s; }
        /* Puedes agregar más estrellas si quieres */

        /* Frase */
        .frase {
            font-family: 'Brush Script MT', cursive; /* Fuente linda y cursiva */
            font-size: 3em;
            color: #FFD700; /* Amarillo dorado para que resalte */
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            margin-top: 20px;
            z-index: 1;
        }

        /* Suelo */
        .suelo {
            position: absolute;
            bottom: 0;
            width: 100%;
            height: 50px;
            background: linear-gradient(to bottom, #006400, #228B22); /* Verde para el suelo */
            z-index: 1;
        }

        /* Flores brotando */
        .flores {
            position: absolute;
            bottom: 50px; /* Justo encima del suelo */
            width: 100%;
            display: flex;
            justify-content: space-around;
            z-index: 2;
        }

        .flor {
            position: relative;
            width: 20px;
            height: 0; /* Comienza en 0 para la animación */
            background: #228B22; /* Tallo verde */
            animation: brotar 3s ease-in-out forwards;
            transform-origin: bottom;
        }

        @keyframes brotar {
            from {
                height: 0;
            }
            to {
                height: 100px;
            }
        }

        .petalos {
            position: absolute;
            top: -25px;
            left: -15px;
            width: 50px;
            height: 50px;
            background: radial-gradient(circle, #FFD700 40%, #FFCC00 100%); /* Amarillo para pétalos */
            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
        }

        .flor:nth-child(1) { animation-delay: 0.5s; }
        .flor:nth-child(2) { animation-delay: 1s; }
        .flor:nth-child(3) { animation-delay: 1.5s; }
        .flor:nth-child(4) { animation-delay: 2s; }
    </style>
</head>
<body>
    <div class="stars">
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
        <div class="star"></div>
    </div>
    <div class="frase">Feliz día, te amo</div>
    <div class="flores">
        <div class="flor"><div class="petalos"></div></div>
        <div class="flor"><div class="petalos"></div></div>
        <div class="flor"><div class="petalos"></div></div>
        <div class="flor"><div class="petalos"></div></div>
    </div>
    <div class="suelo"></div>
</body>
</html>
