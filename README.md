Protótipo de um site de críticas de filmes simulando o ecossistema Netflix

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Veja Críticas desses Filmes</title>
   
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
