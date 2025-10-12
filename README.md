<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NAMORADOS?</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      height: 100vh;
      background: radial-gradient(circle at top, #ffb6c1, #ff69b4, #ff1493);
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: "Poppins", sans-serif;
      overflow: hidden;
      animation: backgroundMove 10s infinite alternate ease-in-out;
    }

    @keyframes backgroundMove {
      0% { background-position: left top; }
      100% { background-position: right bottom; }
    }

    h1 {
      font-size: 3rem; /* menor agora */
      color: white;
      text-shadow: 0 0 15px #fff, 0 0 30px #ff69b4, 0 0 60px #ff1493;
      animation: pulse 2s infinite alternate;
      text-align: center;
    }

    @keyframes pulse {
      from {
        transform: scale(1);
        text-shadow: 0 0 15px #fff, 0 0 30px #ff69b4, 0 0 60px #ff1493;
      }
      to {
        transform: scale(1.05);
        text-shadow: 0 0 30px #fff, 0 0 50px #ff69b4, 0 0 100px #ff1493;
      }
    }

    .heart {
      position: absolute;
      color: white;
      font-size: 1.2rem;
      animation: float 6s linear infinite;
      opacity: 0.8;
    }

    @keyframes float {
      from {
        transform: translateY(100vh) scale(0.5);
        opacity: 0;
      }
      25% {
        opacity: 1;
      }
      to {
        transform: translateY(-10vh) scale(1.2);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1>NAMORADOS?</h1>

  <script>
    function createHeart() {
      const heart = document.createElement("div");
      heart.classList.add("heart");
      heart.innerHTML = "❤️";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = 4 + Math.random() * 4 + "s";
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 8000);
    }

    setInterval(createHeart, 500);
  </script>
</body>
</html>
