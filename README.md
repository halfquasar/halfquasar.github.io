<html>
<head>
  <meta charset="UTF-8">

  <style>
    .cd {
      width: 180px;
      height: 180px;
      margin: 25px auto;
      border-radius: 50%;
      background: repeating-radial-gradient(
        circle,
        #333 0px,
        #777 2px,
        #444 4px
      );
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .cd img {
      width: 65px;
      height: 65px;
      border-radius: 50%;
    }

    .playing {
      animation: rotate 4s linear infinite;
    }

    @keyframes rotate {
      to { transform: rotate(360deg); }
    }
  </style>
</head>

<body>
  <h1>你好喵！</h1>
  <p>這裡什麼都沒有喵</p>
  <img src="IMG_20261031_031019.jpg" alt="图片" width="300">

  <hr>

  <div class="cd" id="cd">
    <img src="冀西南林路行_109951166554891221.jpg" alt="唱片封面">
  </div>

  <audio id="music" autoplay loop>
    <source src="万能青年旅店 - 采石.mp3" type="audio/mpeg">
  </audio>

  <script>
    const music = document.getElementById("music");
    const cd = document.getElementById("cd");

    music.addEventListener("play", () => {
      cd.classList.add("playing");
    });

    music.addEventListener("pause", () => {
      cd.classList.remove("playing");
    });

    music.play().catch(() => {
      // 自动播放被浏览器阻止时，等待用户操作
    });
  </script>
</body>
</html>
