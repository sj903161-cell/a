# a
# Love-website-

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Sweet Love 💗</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html { scroll-behavior: smooth; }

body {
  font-family: Georgia, serif;
  background: #fff1f5;
  color: #713c53;
  text-align: center;
  overflow-x: hidden;
}

header {
  min-height: 390px;
  padding: 65px 20px;
  background: linear-gradient(135deg,#ffd1e2,#fff0f5,#f8bfd5);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

h1 {
  color: #c04e7d;
  font-size: clamp(38px,9vw,62px);
  margin: 18px 0;
}

.subtitle {
  line-height: 1.8;
  font-size: 17px;
}

section {
  max-width: 900px;
  margin: auto;
  padding: 55px 20px;
}

h2 {
  color: #c04e7d;
  font-size: 30px;
  margin-bottom: 22px;
}

.card {
  background: white;
  padding: 28px;
  border-radius: 22px;
  box-shadow: 0 5px 22px #d98ba533;
  line-height: 2;
  margin: 20px auto;
}

button {
  background: #d95c8a;
  color: white;
  border: none;
  padding: 14px 25px;
  margin: 10px;
  border-radius: 30px;
  cursor: pointer;
  font-size: 15px;
  transition: .3s;
}

button:hover {
  background: #ad3c6b;
  transform: scale(1.04);
}

.gallery {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 14px;
}

.gallery img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  border: 7px solid white;
  border-radius: 14px;
  box-shadow: 0 4px 15px #d98ba533;
}

.hidden { display: none; }

.message {
  background: #ffe0eb;
  padding: 24px;
  border-radius: 20px;
  margin-top: 18px;
  line-height: 1.9;
  animation: appear .6s ease;
}

#timer {
  color: #c04e7d;
  font-size: 22px;
  font-weight: bold;
  line-height: 1.8;
}

.heart {
  position: fixed;
  bottom: -35px;
  pointer-events: none;
  z-index: 10;
  animation: floatUp linear forwards;
}

@keyframes floatUp {
  to {
    transform: translateY(-110vh) rotate(360deg);
    opacity: 0;
  }
}

@keyframes appear {
  from {opacity:0;transform:translateY(12px);}
  to {opacity:1;transform:translateY(0);}
}

footer {
  background: #f8cadb;
  padding: 30px 15px;
  line-height: 2;
}

@media(max-width:600px) {
  section { padding: 42px 16px; }
  .gallery { grid-template-columns: repeat(2,1fr); }
  .gallery img { height: 155px; }
  .card { padding: 21px; }
}
</style>
</head>

<body>

<header>
  <div style="font-size:45px">💗 🌸 💗</div>

  <h1>My Sweet Love</h1>

  <p class="subtitle">
    A little website made with love and beautiful memories.<br>
    Especially for <b>Anshika</b> 💕
  </p>

  <button onclick="document.getElementById('letter').scrollIntoView()">
    Open Your Surprise 💌
  </button>
</header>

<section id="letter">
  <h2>A Letter For You 💌</h2>

  <div class="card">
    <h3>Dear Anshika 💗</h3>

    <p>
      Thank you for being a beautiful part of my memories.
      Keep smiling always! 💗
      <br><br>
      Some people make ordinary moments beautiful.
      Your happiness and smile deserve endless good wishes.
      <br><br>
      May every day bring you happiness,
      success and countless reasons to smile.
      <br><br>
      With lots of love and best wishes,
      <br>
      <b>Sanyam Jain ❤️</b>
    </p>
  </div>
</section>

<section>
  <h2>Our Beautiful Memories 📸</h2>
  <p>Every picture holds a special memory.</p>

  <div class="gallery" style="margin-top:22px">
    <img src="photo1.jpg" alt="Memory one">
    <img src="photo2.jpg" alt="Memory two">
    <img src="photo3.jpg" alt="Memory three">
  </div>
</section>

<section>
  <h2>A Little Surprise 🎁</h2>
  <p>Something special is waiting for you!</p>

  <button onclick="showSurprise()">
    Tap Here Anshika 💗
  </button>

  <div id="surprise" class="message hidden">
    🌹 Anshika, always remember that you are
    appreciated, valued and deserving of happiness.
    Keep shining! 💖
  </div>
</section>

<section>
  <h2>Our Special Countdown ⏳</h2>

  <div class="card">
    <p>Counting down to 21 November 2026 💗</p>
    <div id="timer">Loading...</div>
  </div>
</section>

<section>
  <h2>A Secret Message 🔐</h2>

  <p>A little secret is hidden here...</p>

  <button onclick="showSecret()">
    Unlock Secret 💌
  </button>

  <div id="secret" class="message hidden">
    ✨ Dear Anshika,
    <br><br>
    This little website is a reminder to
    keep smiling and make beautiful memories.
    <br><br>
    Always stay happy! 💗
    <br><br>
    — Sanyam
  </div>
</section>

<section>
  <h2>Our Music Corner 🎵</h2>

  <p>Listen to a favourite song while exploring.</p>

  <audio id="music" src="music.mp3" loop></audio>

  <button onclick="toggleMusic()" id="musicBtn">
    ▶ Play Music
  </button>
</section>

<footer>
  Made with ❤️ by Sanyam Jain
  <br>
  Especially for Anshika 🌸
  <br>
  My Sweet Love 💗
</footer>

<script>

// Surprise
function showSurprise() {
  document.getElementById("surprise")
    .classList.remove("hidden");
}

// Secret message
function showSecret() {
  document.getElementById("secret")
    .classList.remove("hidden");
}

// Music
function toggleMusic() {
  const music = document.getElementById("music");
  const btn = document.getElementById("musicBtn");

  if (music.paused) {
    music.play().then(() => {
      btn.innerText = "❚❚ Pause Music";
    }).catch(() => {
      alert("Please upload your music.mp3 file.");
    });
  } else {
    music.pause();
    btn.innerText = "▶ Play Music";
  }
}

// Countdown: 21 November 2026
const specialDate =
  new Date("2026-11-21T00:00:00+05:30").getTime();

function updateTimer() {
  const now = Date.now();
  const difference = specialDate - now;
  const timer = document.getElementById("timer");

  if (difference <= 0) {
    timer.innerHTML =
      "🎉 The special day is here! 💗";
    return;
  }

  const days = Math.floor(difference / 86400000);
  const hours = Math.floor(
    (difference % 86400000) / 3600000
  );
  const minutes = Math.floor(
    (difference % 3600000) / 60000
  );
  const seconds = Math.floor(
    (difference % 60000) / 1000
  );

  timer.innerHTML =
    `${days} Days<br>` +
    `${hours} Hours<br>` +
    `${minutes} Minutes<br>` +
    `${seconds} Seconds`;
}

updateTimer();
setInterval(updateTimer,1000);

// Floating hearts
function createHeart() {
  const heart = document.createElement("div");

  heart.className = "heart";
  heart.innerHTML = ["💗","💕","💖","🌸"][
    Math.floor(Math.random()*4)
  ];

  heart.style.left = Math.random()*100 + "vw";
  heart.style.fontSize =
    (16 + Math.random()*20) + "px";
  heart.style.animationDuration =
    (5 + Math.random()*4) + "s";

  document.body.appendChild(heart);

  setTimeout(() => heart.remove(),9000);
}

setInterval(createHeart,800);

</script>

</body>
</html>
