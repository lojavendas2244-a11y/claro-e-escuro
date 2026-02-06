<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FELIPHY SITE</title>

  <style>
    :root {
      --green: #00ff00;
      --black: #000000;
    }

    body {
      font-family: Helvetica, Arial, sans-serif;
      background: var(--bg);
      color: var(--fontcolor);
      padding: 20px;
      transition: 0.3s;
    }

    ul {
      padding-left: 20px;
    }

    .list {
      list-style: square;
    }

    #msg {
      font-family: monospace;
    }

    button {
      padding: 10px 20px;
      margin-top: 15px;
      font-weight: bold;
      cursor: pointer;
      border: none;
    }

    .light-theme {
      --bg: var(--green);
      --fontcolor: var(--black);
    }

    .dark-theme {
      --bg: var(--black);
      --fontcolor: var(--green);
    }
  </style>
</head>

<body class="light-theme">

  <h1>Lista de tarefas</h1>

  <p id="msg">Tarefas atuais:</p>

  <ul>
    <li class="list">Adicionar estilos visuais</li>
    <li class="list">Adicionar temas claros e escuros</li>
    <li class="list">Habilitar a alternância de temas</li>
  </ul>

  <button id="btn">Modo Escuro</button>

  <script>
    const btn = document.getElementById('btn');

    btn.addEventListener('click', () => {
      document.body.classList.toggle('dark-theme');
      document.body.classList.toggle('light-theme');

      if (document.body.classList.contains('dark-theme')) {
        btn.textContent = 'Modo Claro';
      } else {
        btn.textContent = 'Modo Escuro';
      }
    });
  </script>

</body>
</html>



