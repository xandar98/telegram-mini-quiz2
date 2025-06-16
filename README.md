<!DOCTYPE html>
<html>
<head>
  <title>Mini Quiz</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body { font-family: sans-serif; background: #111; color: #fff; padding: 20px; text-align: center; }
    .question { margin: 20px 0; }
    button { padding: 10px 20px; margin: 5px; background: #1e88e5; border: none; color: white; border-radius: 5px; }
  </style>
</head>
<body>
  <h2>🧠 Mini Quiz App</h2>
  <div id="quiz">
    <div class="question">
      <p>Q1: What is the capital of France?</p>
      <button onclick="check(this, false)">Berlin</button>
      <button onclick="check(this, false)">Madrid</button>
      <button onclick="check(this, true)">Paris</button>
    </div>
  </div>
  <p id="result"></p>
  <script>
    function check(btn, correct) {
      document.getElementById("result").innerText = correct ? "✅ Correct!" : "❌ Wrong!";
      [...document.querySelectorAll("button")].forEach(b => b.disabled = true);
    }
  </script>
</body>
</html>