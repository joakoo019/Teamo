<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Lluvia de Amor</title>
  <style>
    body {
      margin: 0;
      background: #ffdee9;
      overflow: hidden;
      height: 100vh;
    }
    .corazon {
      position: absolute;
      top: -50px;
      color: #e63946;
      animation: caer 5s linear infinite;
      font-size: 30px;
    }
    @keyframes caer {
      0% { transform: translateY(0); }
      100% { transform: translateY(110vh); }
    }
  </style>
</head>
<body>

<script>
  function crearCorazon() {
    const corazon = document.createElement("div");
    corazon.classList.add("corazon");
    corazon.style.left = Math.random() * window.innerWidth + "px";
    corazon.style.fontSize = (20 + Math.random() * 30) + "px";
    corazon.innerHTML = "❤️";
    document.body.appendChild(corazon);

    setTimeout(() => {
      corazon.remove();
    }, 5000);
  }

  setInterval(crearCorazon, 300);
</script>

</body>
</html>
