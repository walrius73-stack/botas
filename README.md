<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para ti ❤️</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            background: #000;
            height: 100vh;
            overflow: hidden;
            font-family: Arial, sans-serif;
        }

        #inicio {
            position: fixed;
            inset: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background: #000;
            z-index: 10;
            cursor: pointer;
            transition: opacity 1s ease;
        }

        #inicio img {
            width: 100%;
            height: 100%;
            object-fit: contain;
        }

        #mensaje {
            position: absolute;
            bottom: 8%;
            width: 90%;
            text-align: center;
            color: white;
            font-size: 24px;
            text-shadow: 0 2px 10px black;
        }

        #video {
            width: 100%;
            height: 100%;
            object-fit: contain;
            display: none;
        }
    </style>
</head>

<body>

    <div id="inicio" onclick="mostrarVideo()">
        <img src="imagen.jpg">
        <div id="mensaje">
            Toca la pantalla ❤️
        </div>
    </div>

    <video id="video" controls>
        <source src="video.mp4" type="video/mp4">
        Tu navegador no puede reproducir este video.
    </video>

    <script>
        function mostrarVideo() {
            const inicio = document.getElementById("inicio");
            const video = document.getElementById("video");

            inicio.style.opacity = "0";

            setTimeout(() => {
                inicio.style.display = "none";
                video.style.display = "block";
                video.play();
            }, 1000);
        }
    </script>

</body>
</html>
