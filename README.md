<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Открытка</title>
    <style>
      body {
        background-color: beige;
        font-family: Arial, sans-serif;
        text-align: center;
      }
      .card {
        width: 400px;
        height: 400px;
        border: 2px solid black;
        margin: 0 auto;
        position: relative;
        overflow: hidden;
      }
      .card-front {
        background-image: url('https://i.imgur.com/qS1lBqz.jpg');
        background-size: cover;
        background-position: center;
        width: 100%;
        height: 100%;
      }
      .card-back {
        background-color: white;
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        transform: rotateY(180deg);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        transition: transform 0.6s ease-in-out;
      }
      .card-back h2 {
        font-size: 36px;
        color: black;
        margin-bottom: 20px;
      }
      .card-back p {
        font-size: 24px;
        color: black;
        margin-bottom: 20px;
      }
      .card-back button {
        padding: 10px 20px;
        font-size: 18px;
        background-color: #ff6f69;
        border: none;
        color: white;
        cursor: pointer;
      }
      .card.flipped .card-back {
        transform: rotateY(0deg);
      }
    </style>
  </head>

  <body>
    <div class="card" onclick="this.classList.toggle('flipped')">
      <div class="card-front"></div>
      <div class="card-back">
        <h2>Дорогая Камила …, </h2>
        <p>Поздравляю нас с полгодом Общения! Время пролетело незаметно, мы прошли многое вместе и я очень рад, что ты есть в моей жизни. Хочу пожелать нам еще больше счастливых моментов вместе и продолжения нашего знакомства!</p>
        <button>Открыть</button>
      </div>
    </div>
  </body>

  <script>
    const button = document.querySelector('button');
    const card = document.querySelector('.card');

    button.addEventListener('click', () => {
      card.classList.toggle('flipped');
    });
  </script>
</html>
