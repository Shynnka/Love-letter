<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Для тебя ❤️</title>
  <style>
    body {
      margin: 0;
      background-color: #ffe6f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: 'Segoe UI', sans-serif;
    }

    .envelope {
      width: 250px;
      height: 150px;
      background-color: white;
      position: relative;
      border-radius: 8px;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
      transition: transform 0.5s ease;
    }

    .envelope:hover {
      transform: scale(1.02);
    }

    .heart {
      position: absolute;
      top: 15px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 30px;
      color: red;
    }

    .label {
      position: absolute;
      bottom: 10px;
      width: 100%;
      text-align: center;
      font-size: 16px;
      color: rgba(0, 0, 0, 0.4);
      pointer-events: none;
    }

    .letter {
      position: absolute;
      top: 0;
      left: 0;
      width: 250px;
      height: 150px;
      background-color: white;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
      transform: scaleY(0);
      transform-origin: top;
      transition: transform 0.6s ease;
      padding: 20px;
      box-sizing: border-box;
      overflow: hidden;
      z-index: 10;
    }

    .letter.open {
      transform: scaleY(1);
    }

    .letter p {
      font-size: 14px;
      line-height: 1.5;
      color: #333;
      margin: 0;
    }
  </style>
</head>
<body>

<div class="envelope" id="envelope">
  <div class="heart">❤️</div>
  <div class="label">нажми чтобы открыть</div>
  <div class="letter" id="letter">
    <p>Сүйікті жарым, ғашықтар күнімен! 🥰<br><br>
      Ты моя опора, моя защита, крепкое плечо на которое могу положиться в любое время.
      Спасибо за твое тепло, поддержку и заботу✨<br><br>
      Люблю тебя безмерно❤️ Махаббатымыз мәңгі болсын!
    </p>
  </div>
</div>

<script>
  const envelope = document.getElementById('envelope');
  const letter = document.getElementById('letter');

  envelope.addEventListener('click', () => {
    letter.classList.toggle('open');
  });
</script>

</body>
</html>
