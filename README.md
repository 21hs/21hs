<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bem Vindo</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
      background-color: #f4f4f4;
    }
    .container {
      text-align: center;
    }
    .typing {
      font-size: 2em;
      font-weight: bold;
      color: #333;
      white-space: nowrap;
      border-right: 3px solid #000;
      display: inline-block;
      padding-right: 10px;
      animation: typing 2s steps(10) 1s infinite, blink 0.75s step-end infinite;
    }
    @keyframes typing {
      from {
        width: 0;
      }
      to {
        width: 16ch;
      }
    }
    @keyframes blink {
      50% {
        border-color: transparent;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="typing" id="typeEffect">Bem Vindo</div>
  </div>

  <script>
    // Essa função irá reiniciar a animação de digitação e apagamento.
    function resetTypingEffect() {
      const typingElement = document.getElementById("typeEffect");
      typingElement.style.animation = "none"; // Reseta a animação
      typingElement.offsetHeight; // Força o reflow para reiniciar a animação
      typingElement.style.animation = "typing 2s steps(10) 1s infinite, blink 0.75s step-end infinite"; // Reaplica a animação
    }

    // Chama a função para reiniciar a animação a cada 5 segundos (tempo de duração da animação)
    setInterval(resetTypingEffect, 5000);
  </script>

</body>
</html>
