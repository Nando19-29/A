# A
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
  word-wrap: break-word;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Make final line responsive */
.love-text {
  display: inline-block;
  font-family: 'Playfair Display', serif;
  font-size: clamp(24px, 6vw, 36px); /* Responsive font size */
  word-wrap: break-word;
  text-align: center;
}
</style>
</head>

<body>

<!-- Step 1 -->
<div class="container" id="step1">
  <button onclick="stepOne()">Press</button>
</div>

<!-- Step 2 -->
<div class="container text" id="step2">
  Do you know?
  <br><br>
  <button onclick="stepTwo()">Press</button>
</div>

<!-- Step 3 -->
<div class="container text" id="step3">
  <span class="love-text">Nando loves you more than anything ❤️</span>
  <br><br>
  <button onclick="stepThree()">Press</button>
</div>

<script>
function stepOne() {
  document.getElementById("step1").style.display = "none";
  document.getElementById("step2").style.display = "block";
}

function stepTwo() {
  document.getElementById("step2").style.display = "none";
  document.getElementById("step3").style.display = "block";
}

function stepThree() {
  // Final step stays visible
  alert("❤️ Nando loves you forever! ❤️");
}
</script>

</body>
</html>
