# N-A
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For You ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Poppins:wght@300;400;500&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(135deg, #f7b7c9, #f3e7d3, #b7c9f7);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Poppins', sans-serif;
  overflow: hidden;
}

.container {
  text-align: center;
  color: #2d2d2d;
}

button {
  padding: 16px 40px;
  font-size: 18px;
  border: none;
  border-radius: 40px;
  background: white;
  color: #c44d6d;
  cursor: pointer;
  box-shadow: 0 10px 25px rgba(0,0,0,0.15);
  animation: pulse 1.5s infinite;
}

@keyframes pulse {
  0% { transform: scale(1); }
  50% { transform: scale(1.08); }
  100% { transform: scale(1); }
}

.text {
  font-family: 'Playfair Display', serif;
  font-size: 36px;
  display: none;
  animation: fadeIn 2s forwards;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.scene {
  display: none;
  position: relative;
  width: 100%;
  height: 100vh;
}

.character {
  position: absolute;
  bottom: 0;
  width: 220px;
  animation: walkIn 3s forwards;
}

.girl {
  left: -300px;
  animation-name: girlWalk;
}

.boy {
  right: -300px;
  animation-name: boyWalk;
}

@keyframes girlWalk {
  to { left: 15%; }
}

@keyframes boyWalk {
  to { right: 15%; }
}

.dialogue {
  position: absolute;
  top: 20%;
  width: 40%;
  font-family: 'Playfair Display', serif;
  font-size: 26px;
  animation: fadeIn 2s forwards;
}

.left {
  left: 5%;
}

.right {
  right: 5%;
}

.hearts {
  position: absolute;
  width: 100%;
  height: 100%;
  pointer-events: none;
}

.heart {
  position: absolute;
  font-size: 20px;
  animation: floatUp 5s infinite;
}

@keyframes floatUp {
  from { transform: translateY(0); opacity: 1; }
  to { transform: translateY(-600px); opacity: 0; }
}
</style>
</head>

<body>

<div class="container" id="step1">
  <button onclick="stepOne()">Press</button>
</div>

<div class="container text" id="step2">
  Do you know?
  <br><br>
  <button onclick="stepTwo()">Press</button>
</div>

<div class="container text" id="step3">
  Nando loves you more than anything
  <br><br>
  <button onclick="stepThree()">Press</button>
</div>

<div class="scene" id="scene">
  <img src="https://i.imgur.com/8Qf8F6y.png" class="character girl">
  <img src="https://i.imgur.com/9J8ZQ4A.png" class="character boy">

  <div class="dialogue left" id="girlText" style="display:none;">
    Will you be mine forever?<br>
    I love uh so much Avijeet
  </div>

  <div class="dialogue right" id="boyText" style="display:none;">
    I love you more Nando
  </div>

  <div class="hearts" id="hearts"></div>
</div>

<script>
function stepOne() {
  step1.style.display = "none";
  step2.style.display = "block";
}

function stepTwo() {
  step2.style.display = "none";
  step3.style.display = "block";
}

function stepThree() {
  step3.style.display = "none";
  scene.style.display = "block";

  setTimeout(() => {
    girlText.style.display = "block";
  }, 3000);

  setTimeout(() => {
    boyText.style.display = "block";
    createHearts();
  }, 6000);
}

function createHearts() {
  for (let i = 0; i < 20; i++) {
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "%";
    heart.style.bottom = "0";
    heart.style.animationDelay = Math.random() * 3 + "s";
    hearts.appendChild(heart);
  }
}
</script>

</body>
</html>
<img src="https://cdn.pixabay.com/photo/2020/03/05/17/56/girl-4900598_1280.png" class="character girl">
<img src="https://cdn.pixabay.com/photo/2017/02/01/10/18/man-2034817_1280.png" class="character boy">
