<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Teacher's Day Sir</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #050505;
  font-family: Arial, sans-serif;
  color: white;
  overflow: hidden;
}

/* Background stars */
.star {
  position: fixed;
  width: 3px;
  height: 3px;
  background: white;
  border-radius: 50%;
  animation: twinkle 2s infinite alternate;
}

@keyframes twinkle {
  from { opacity: 0.2; }
  to { opacity: 1; }
}

/* Card */
.card {
  width: 90%;
  max-width: 420px;
  padding: 30px;
  text-align: center;
  border: 1px solid #444;
  border-radius: 25px;
  background: rgba(20,20,20,0.92);
  box-shadow: 0 0 40px rgba(255,255,255,0.08);
  animation: appear 1.5s ease;
}

@keyframes appear {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

h1 {
  font-size: 30px;
  letter-spacing: 2px;
}

.subtitle {
  color: #aaa;
  margin-bottom: 25px;
}

.letter {
  text-align: left;
  line-height: 1.7;
  color: #ddd;
  min-height: 230px;
}

.signature {
  margin-top: 20px;
  text-align: right;
  font-weight: bold;
}

button {
  margin-top: 20px;
  padding: 12px 25px;
  border: 1px solid white;
  border-radius: 30px;
  background: transparent;
  color: white;
  cursor: pointer;
  font-size: 15px;
  transition: 0.3s;
}

button:hover {
  background: white;
  color: black;
  transform: scale(1.05);
}

.footer {
  margin-top: 20px;
  font-size: 10px;
  letter-spacing: 3px;
  color: #777;
}
</style>
</head>

<body>

<div class="card">

  <h1>🎓 Happy Teacher's Day</h1>

  <div class="subtitle">
    To our amazing Sir
  </div>

  <div class="letter" id="letter"></div>

  <button onclick="showLetter()">
    Open Message 💌
  </button>

  <div class="footer">
    MADE WITH CODE • FROM YOUR STUDENT
  </div>

</div>

<script>

const message = `
Dear Sir,

Happy Teacher's Day! 🎉

Thank you for your patience, guidance,
and everything you have taught us.

Hindi lang po lessons ang itinuro ninyo
sa amin, kundi pati ang pagiging
responsable, matiyaga, at hindi
sumusuko kapag nahihirapan.

We may not always say it,
but we truly appreciate your effort
and sacrifices as our teacher.

Thank you for believing in us
and for continuing to guide us.

Happy Teacher's Day, Sir! ❤️

Keep inspiring students
and keep being an amazing teacher.

— From your student, LynxDta
`;

let i = 0;

function showLetter() {

  const letter = document.getElementById("letter");

  letter.innerHTML = "";
  i = 0;

  function typeWriter() {

    if (i < message.length) {

      letter.innerHTML +=
        message.charAt(i)
          .replace(/\n/g, "<br>");

      i++;

      setTimeout(typeWriter, 25);
    }
  }

  typeWriter();
}


/* Create stars */

for (let i = 0; i < 50; i++) {

  const star = document.createElement("div");

  star.className = "star";

  star.style.left =
    Math.random() * 100 + "vw";

  star.style.top =
    Math.random() * 100 + "vh";

  star.style.animationDelay =
    Math.random() * 2 + "s";

  document.body.appendChild(star);
}

</script>

</body>
</html>
