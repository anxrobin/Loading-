<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Be My Valentine 💖</title>

<style>
  body {
    margin: 0;
    height: 100vh;
    background: linear-gradient(135deg, #ff758c, #ff7eb3);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: "Segoe UI", sans-serif;
  }

  .card {
    background: white;
    padding: 40px 30px;
    border-radius: 20px;
    text-align: center;
    box-shadow: 0 20px 40px rgba(0,0,0,0.2);
    max-width: 320px;
    width: 90%;
  }

  h1 {
    margin-bottom: 25px;
    color: #333;
  }

  .buttons {
    position: relative;
    height: 120px;
  }

  button {
    padding: 12px 26px;
    font-size: 18px;
    border-radius: 30px;
    border: none;
    cursor: pointer;
    transition: all 0.3s ease;
  }

  .yes {
    background: #ff4d6d;
    color: white;
  }

  .no {
    background: #e0e0e0;
    color: #333;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    margin-top: 60px;
  }
</style>
</head>

<body>

<div class="card">
  <h1>Will you be my Valentine? 💘</h1>

  <div class="buttons">
    <button class="yes" id="yesBtn">Yes 💖</button>
    <button class="no" id="noBtn">No</button>
  </div>
</div>

<script>
  const noMessages = [
    "No",
    "Are you sure?",
    "Think again 😐",
    "That hurts 💔",
    "Don’t be cruel 😭",
    "Okay… last try 😞"
  ];

  let index = 0;
  let scale = 1;

  const noBtn = document.getElementById("noBtn");
  const yesBtn = document.getElementById("yesBtn");

  noBtn.addEventListener("click", () => {
    // Change text
    noBtn.innerText = noMessages[index];
    index = (index + 1) % noMessages.length;

    // Move button randomly
    const x = Math.random() * 120 - 60;
    const y = Math.random() * 60 - 30;
    noBtn.style.transform = `translate(${x}px, ${y}px)`;

    // Grow YES button smoothly
    scale += 0.15;
    yesBtn.style.transform = `scale(${scale})`;
  });

  yesBtn.addEventListener("click", () => {
    document.body.innerHTML = `
      <div style="
        height:100vh;
        display:flex;
        align-items:center;
        justify-content:center;
        background:linear-gradient(135deg,#ff758c,#ff7eb3);
        font-family:Segoe UI;
        color:white;
        text-align:center;
      ">
        <h1>Yay! 💕<br>You just made me very happy 😘</h1>
      </div>
    `;
  });
</script>

</body>
</html># Loading-
