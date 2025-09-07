<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meri Fuljadi ❤️</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: url('bg1.jpg') no-repeat center center fixed;
      background-size: cover;
      font-family: Arial, sans-serif;
      overflow-x: hidden;
      text-align: center;
      color: #fff;
    }

    h1 {
      font-size: 3em;
      margin-top: 20vh;
      text-shadow: 0 0 10px #ff99cc, 0 0 20px #ff66b2, 0 0 30px #ff3399;
      position: relative;
      z-index: 2;
    }

    .love-text {
      margin-top: 30px;
      font-size: 1.2em;
      color: #ffe6f0;
      max-width: 90%;
      margin-left: auto;
      margin-right: auto;
      line-height: 1.6em;
      z-index: 2;
      position: relative;
      text-shadow: 0 0 8px #000;
    }

    /* Falling hearts */
    .heart {
      position: fixed;
      top: -10px;
      color: red;
      font-size: 24px;
      animation: fall linear infinite;
      z-index: 1;
      text-shadow: 0 0 6px #fff;
    }

    @keyframes fall {
      to {
        transform: translateY(110vh);
        opacity: 0;
      }
    }

    /* Dark overlay so text is visible on bright photos */
    .overlay {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.4);
      z-index: 0;
    }
  </style>
</head>
<body>
  <div class="overlay"></div>
  <h1>Meri Fuljadi ❤️</h1>
  <div class="love-text" id="loveText"></div>

  <script>
    // Generate 5000 "I love you" messages
    const loveText = document.getElementById("loveText");
    let text = "";
    for (let i = 0; i < 5000; i++) {
      text += "I love you the most my love 💓 ";
    }
    loveText.innerText = text;

    // Create falling hearts
    function createHeart() {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerText = "💖";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (2 + Math.random() * 3) + "s";
      document.body.appendChild(heart);

      setTimeout(() => heart.remove(), 5000);
    }

    setInterval(createHeart, 200);
  </script>
</body>
</html>
