<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Эффект волн</title>
  <style>
    /* Основной контейнер для волн */
    .waveContainer {
      position: fixed;
      bottom: 0;
      width: 100%;
      height: 150px; /* Изменяй высоту волн */
      overflow: hidden;
    }

    /* Волны */
    .wave {
      position: absolute;
      width: 200%; /* Дважды больше ширины окна */
      height: 150px; /* Высота волн */
      background: linear-gradient(to right, #0088FF, #0059b3); /* Цвет волн */
      animation: wave 7s linear infinite; /* Анимация */
    }

    /* Первый слой волн */
    .wave:nth-child(1) {
      top: 0;
      z-index: 1000;
      animation-delay: 0s;
    }

    /* Второй слой волн */
    .wave:nth-child(2) {
      top: 10px;
      z-index: 999;
      opacity: 0.8; /* Прозрачность */
      animation-delay: -3s;
    }

    /* Третий слой волн */
    .wave:nth-child(3) {
      top: 20px;
      z-index: 998;
      opacity: 0.6; /* Прозрачность */
      animation-delay: -6s;
    }

    /* Анимация волн */
    @keyframes wave {
      0% {
        left: -50%;
      }
      50% {
        left: 0;
      }
      100% {
        left: -50%;
      }
    }
  </style>
</head>
<body>
  <!-- Основное содержимое страницы -->
  <h1>Пример страницы с волнами</h1>
  <p>Ваш контент здесь.</p>

  <!-- Контейнер для волн -->
  <div class="waveContainer">
    <div class="wave"></div>
    <div class="wave"></div>
    <div class="wave"></div>
  </div>
</body>
</html>
