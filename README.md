<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>Eid Surprise 😏</title>

  <style>
    body {
      text-align: center;
      margin-top: 100px;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ffecd2, #fcb69f);
      overflow: hidden;
    }

    h2 {
      font-size: 30px;
    }

    button {
      padding: 12px 25px;
      font-size: 18px;
      margin: 10px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      transition: 0.3s;
    }

    #yes {
      background-color: #28a745;
      color: white;
    }

    #no {
      position: absolute;
      background-color: #dc3545;
      color: white;
    }
  </style>
</head>

<body>

<h2>ঈদ সালামি দিবা তো? 😌💸</h2>

<button id="yes" onclick="love()">দিবো 💸</button>
<button id="no">না 😏</button>

<script>
let size = 18;

function love() {
  alert("তাহলে এখনই পাঠাও 😎\n\nBkash/Nagad: 01775373639 💸");
}

const noBtn = document.getElementById("no");

document.addEventListener("mousemove", (e) => {
  const rect = noBtn.getBoundingClientRect();

  const distance = Math.hypot(
    e.clientX - (rect.left + rect.width / 2),
    e.clientY - (rect.top + rect.height / 2)
  );

  if (distance < 120) {
    moveButton();
  }
});

noBtn.addEventListener("click", () => {
  size += 10;
  const yesBtn = document.getElementById("yes");
  yesBtn.style.fontSize = size + "px";
  yesBtn.style.padding = (size/2) + "px " + (size) + "px";
});

function moveButton() {
  const x = Math.random() * (window.innerWidth - 100);
  const y = Math.random() * (window.innerHeight - 50);
  noBtn.style.left = x + "px";
  noBtn.style.top = y + "px";
}
</script>

</body>
</html>