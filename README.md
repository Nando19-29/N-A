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
