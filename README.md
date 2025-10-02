<!DOCTYPE html>
<html>
<head>
    <title>Моя Тапалка</title>
    <meta charset="utf-8">
    <script src="https://telegram.org/js/telegram-web-app.js"></script> <!-- Подключение Telegram Web App -->
    <style>
        body { text-align: center; font-family: sans-serif; background: #202020; color: white; }
        #coin { font-size: 80px; cursor: pointer; user-select: none; }
        #score { font-size: 40px; margin: 20px; }
    </style>
</head>
<body>
    <h1>ТАПАЛКА</h1>
    <div id="score">Монеты: 0</div>
    <div id="coin" onclick="tap()">🪙</div>

    <script>
        let score = 0;
        const coinElement = document.getElementById('coin');
        const scoreElement = document.getElementById('score');

        function tap() {
            score++;
            scoreElement.textContent = Монеты: ${score};
            
            // Анимация нажатия
            coinElement.style.transform = 'scale(0.9)';
            setTimeout(() => { coinElement.style.transform = 'scale(1)'; }, 100);
        }

        // Инициализация Telegram Web App
        Telegram.WebApp.ready();
        Telegram.WebApp.expand(); // Раскрыть на весь экран
    </script>
</body>
</html>
