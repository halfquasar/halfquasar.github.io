<html>
<head>
  <meta charset="UTF-8">
</head>
<body>
  <h1>你好喵！</h1>
  <p>這裡什麼都沒有喵</p>
  <p>（我想想這裡以後要加些什麼) </p>
  <img src="IMG_20261031_031019.jpg" alt="图片" width="300">

  <hr>
  <p id="notice">音樂稍等片刻……</p>
<script>
  setTimeout(function() {document.getElementById("notice").remove();
  }, 1000);
</script>

 <audio id="music" autoplay loop>
    <source src="万能青年旅店 - 采石.mp3" type="audio/mpeg">
  </audio>
    <hr>
   <input type="password" id="password" placeholder="请输入密码">
  <button onclick="checkPassword()">解锁</button>

  <p id="message"></p>
  function checkPassword() {
  var password = document.getElementById("password").value;
  var message = document.getElementById("message");

  if (password === "123") {
    message.textContent = "第一段秘密文字！";
  } else if (password === "456") {
    message.textContent = "第二段秘密文字！";
  } else if (password === "789") {
    message.textContent = "第三段秘密文字！";
  } else {
    message.textContent = "密码错误喵！";
  }
</body>
</html>
