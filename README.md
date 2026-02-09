<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Valentine’s</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
  body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background: pink;
    overflow-x: hidden;
    text-align: center;
    transition: background 1.5s ease;
  }

  .container {
    padding: 40px 20px;
    transition: opacity 1.5s ease;
  }

  h1 {
    font-family: 'Pacifico', cursive;
    font-size: clamp(36px, 6vw, 52px);
    color: #ff3f7f;
  }

  .big-heart {
    font-size: 70px;
    margin: 10px 0;
  }

  .stickers {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 20px;
  }

  .stickers img {
    width: 80px;
    max-width: 22vw;
  }

  button {
    margin-top: 30px;
    padding: 14px 28px;
    font-size: 18px;
    border: none;
    border-radius: 30px;
    cursor: pointer;
    background: #ff5fa2;
    color: white;
    font-family: 'Poppins', sans-serif;
  }

  button:active {
    transform: scale(0.95);
  }

  .small-heart {
    position: absolute;
    color: #ff7aa2;
    font-size: 18px;
    animation: float 6s infinite;
  }

  @keyframes float {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-700px); opacity: 0; }
  }

  #message {
    display: none;
    white-space: pre-wrap;
    font-size: clamp(15px, 3.8vw, 18px);
    max-width: 720px;
    margin: 40px auto;
    padding: 0 20px;
    color: #0f3d2e;
  }

  .heart-explosion {
    position: absolute;
    font-size: 24px;
    animation: explode 1s forwards;
  }

  @keyframes explode {
    0% { transform: scale(1); opacity: 1; }
    100% { transform: translate(var(--x), var(--y)) scale(2); opacity: 0; }
  }
</style>
</head>

<body>

<div class="container" id="start">
  <h1>Happy Valentine’s</h1>
  <div class="big-heart">❤️</div>

  <div class="stickers">
    <img src="https://imgur.com/a/05OGAjj">
    <img src="https://imgur.com/a/5mHSk9o">
    <img src="https://imgur.com/a/oNetWVu">
    <img src="https://imgur.com/a/xwxFHid">
  </div>

  <button onclick="startValentine()">Click Me!</button>
</div>

<div id="message"></div>

<!-- Background Music -->
<audio id="bgMusic" loop>
  <source src="https://limewire.com/d/6AZLI#cAN3RCnjs2" type="audio/mpeg">
</audio>

<script>
  // floating hearts
  for (let i = 0; i < 25; i++) {
    let heart = document.createElement("div");
    heart.className = "small-heart";
    heart.innerHTML = "💗";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.bottom = "-20px";
    heart.style.animationDelay = Math.random() * 5 + "s";
    document.body.appendChild(heart);
  }

  function startValentine() {
    document.querySelector("button").innerText = "YEY!";
    document.getElementById("bgMusic").play();

    setTimeout(() => {
      document.getElementById("start").style.opacity = 0;
      document.body.style.background = "#7ED957";

      setTimeout(showMessage, 1500);
    }, 800);
  }

  const text = `Happy Valentine’s, my baby, my love, babe, bro.

I just want to say how thankful I am that you came into my life. Having you here means more to me than I can ever fully explain. I love you for who you are, exactly as you are, and I would still want you in every possible way.

I love how you make me feel cared for and loved, even without saying much. I appreciate all the things you do, even the smallest ones, because they mean a lot to me. Every little effort, every moment, I notice and I value them.

I value you, and I value us. I’m fully committed to you and to what we’re building together. I don’t want to rush anything, but I do see a future with you, and I would love to face your parents and your kuyas someday when the time is right.

Once again, Happy Valentine’s.

Love,
Jones`;

  function showMessage() {
    const msg = document.getElementById("message");
    msg.style.display = "block";
    let i = 0;

    function type() {
      if (i < text.length) {
        msg.innerHTML += text.charAt(i);
        i++;
        setTimeout(type, 35);
      } else {
        let btn = document.createElement("button");
        btn.innerText = "Happy Valentine’s!";
        btn.onclick = explodeHearts;
        msg.appendChild(document.createElement("br"));
        msg.appendChild(btn);
      }
    }
    type();
  }

  function explodeHearts() {
    document.body.style.background = "pink";
    for (let i = 0; i < 35; i++) {
      let heart = document.createElement("div");
      heart.className = "heart-explosion";
      heart.innerHTML = "💖";
      heart.style.left = "50vw";
      heart.style.top = "50vh";
      heart.style.setProperty("--x", (Math.random() * 400 - 200) + "px");
      heart.style.setProperty("--y", (Math.random() * 400 - 200) + "px");
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 1000);
    }
  }
</script>

</body>
</html>

<!-- Background Music -->
<audio id="bgMusic" loop>
  <source src="https://limewire.com/d/6AZLI#cAN3RCnjs2" type="audio/mpeg">
</audio>

<script>
  // floating hearts
  for (let i = 0; i < 25; i++) {
    let heart = document.createElement("div");
    heart.className = "small-heart";
    heart.innerHTML = "💗";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.bottom = "-20px";
    heart.style.animationDelay = Math.random() * 5 + "s";
    document.body.appendChild(heart);
  }

  function startValentine() {
    document.querySelector("button").innerText = "YEY!";
    document.getElementById("bgMusic").play();

    setTimeout(() => {
      document.getElementById("start").style.opacity = 0;
      document.body.style.background = "#7ED957";

      setTimeout(showMessage, 1500);
    }, 800);
  }

  const text = `Happy Valentine’s, my baby, my love, babe, bro.

I just want to say how thankful I am that you came into my life. Having you here means more to me than I can ever fully explain. I love you for who you are, exactly as you are, and I would still want you in every possible way.

I love how you make me feel cared for and loved, even without saying much. I appreciate all the things you do, even the smallest ones, because they mean a lot to me. Every little effort, every moment, I notice and I value them.

I value you, and I value us. I’m fully committed to you and to what we’re building together. I don’t want to rush anything, but I do see a future with you, and I would love to face your parents and your kuyas someday when the time is right.

Once again, Happy Valentine’s.

Love,
Jones`;

  function showMessage() {
    const msg = document.getElementById("message");
    msg.style.display = "block";
    let i = 0;

    function type() {
      if (i < text.length) {
        msg.innerHTML += text.charAt(i);
        i++;
        setTimeout(type, 35);
      } else {
        let btn = document.createElement("button");
        btn.innerText = "Happy Valentine’s!";
        btn.onclick = explodeHearts;
        msg.appendChild(document.createElement("br"));
        msg.appendChild(btn);
      }
    }
    type();
  }

  function explodeHearts() {
    document.body.style.background = "pink";
    for (let i = 0; i < 35; i++) {
      let heart = document.createElement("div");
      heart.className = "heart-explosion";
      heart.innerHTML = "💖";
      heart.style.left = "50vw";
      heart.style.top = "50vh";
      heart.style.setProperty("--x", (Math.random() * 400 - 200) + "px");
      heart.style.setProperty("--y", (Math.random() * 400 - 200) + "px");
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 1000);
    }
  }
</script>

</body>
</html>
