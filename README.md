Protótipo de um site de críticas de filmes simulando o ecossistema Netflix

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Veja Críticas desses Filmes</title>
     <style>
        /* Estilo geral da página */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #141414;
            color: white;
            text-align: center;
        }

        /* Estilo do título principal */
        h1 {
            text-align: center;
            margin: 20px 0;
            font-size: 2.5em;
            color: #e50914;
        }

        /* Estilo do texto centralizado */
        .center-text {
            font-size: 1.8em;
            margin: 40px 0;
            color: white;
        }

        /* Contêiner do carrossel de vídeos */
        .video-carousel {
            display: flex;
            overflow-x: auto;
            scroll-behavior: smooth;
            padding: 20px;
            gap: 15px;
            margin: 0 auto;
            max-width: 95vw;
        }

        /* Estilo dos vídeos */
        .video-container {
            flex: 0 0 auto;
            position: relative;
            width: 300px;
            border-radius: 10px;
            overflow: hidden;
        }

        .video-container img {
            width: 100%;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        /* Efeito de hover na thumbnail */
        .video-container img:hover {
            transform: scale(1.1);
        }

        iframe {
            display: none;
            border: none;
            border-radius: 10px;
        }

        /* Botões de navegação */
        .nav-button {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background-color: rgba(0, 0, 0, 0.7);
            border: none;
            color: white;
            font-size: 2em;
            cursor: pointer;
            z-index: 10;
            padding: 10px;
            border-radius: 50%;
        }

        .nav-button.left {
            left: 10px;
        }

        .nav-button.right {
            right: 10px;
        }
    </style>
</head>
<body>
    <!-- Título principal -->
    <h1>Isaflix</h1>

    <!-- Carrossel de vídeos -->
    <div class="video-carousel" id="carousel">
        <!-- Vídeo 1 -->
        <div class="video-container">
            <a href="https://www.youtube.com/watch?v=yzynBLih7Kc" target="_blank">
                <img src="https://img.youtube.com/vi/yzynBLih7Kc/hqdefault.jpg" alt="Thumbnail do vídeo 1">
            </a>
        </div>

        <!-- Vídeo 2 -->
        <div class="video-container">
            <a href="https://www.youtube.com/watch?v=eWtv4vFaEwM" target="_blank">
                <img src="https://img.youtube.com/vi/eWtv4vFaEwM/hqdefault.jpg" alt="Thumbnail do vídeo 2">
            </a>
        </div>

        <!-- Vídeo 3 -->
        <div class="video-container">
            <a href="https://www.youtube.com/watch?v=CMw5T3NsdEE" target="_blank">
                <img src="https://img.youtube.com/vi/CMw5T3NsdEE/hqdefault.jpg" alt="Thumbnail do vídeo 3">
            </a>
        </div>

        <!-- Vídeo 4 -->
        <div class="video-container">
            <a href="https://www.youtube.com/watch?v=C4HCdXPIy8w" target="_blank">
                <img src="https://img.youtube.com/vi/C4HCdXPIy8w/hqdefault.jpg" alt="Thumbnail do vídeo 4">
            </a>
        </div>
    </div>

    <!-- Botões de navegação -->
    <button class="nav-button left" onclick="scrollLeft()">&#10094;</button>
    <button class="nav-button right" onclick="scrollRight()">&#10095;</button>

    <!-- Texto centralizado abaixo dos vídeos -->
    <div class="center-text">
        Veja críticas dos seus filmes favoritos
    </div>

    <script>
        const carousel = document.getElementById('carousel');

        function scrollLeft() {
            carousel.scrollBy({
                left: -300,
                behavior: 'smooth'
            });
        }

        function scrollRight() {
            carousel.scrollBy({
                left: 300,
                behavior: 'smooth'
            });
        }
    </script>
</body>
</html>
