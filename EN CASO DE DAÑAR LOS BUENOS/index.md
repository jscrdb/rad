<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ininteligible</title>
  <style>
    :root {
      --bg-color: #282a36;
      --text-color: #f8f8f2;
      --link-color: #bd93f9;
      --sepia-color: #c0c090; /* Nuevo color sepia */
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-color);
      font-family: Arial, sans-serif;
      transition: background-color 0.5s, color 0.5s;
    }

    a {
      color: var(--link-color);
    }

    /* Estilos para el texto que se escribe letra por letra */
    #text {
      display: inline-block;
      overflow: hidden;
      white-space: nowrap;
      border-right: 0.15em solid var(--text-color);
      animation: typing 4s steps(14), blink-caret 0.75s step-end infinite;
    }
    @keyframes typing {
      from {
        width: 0;
      }
      to {
        width: 100%;
      }
    }
    @keyframes blink-caret {
      from,
      to {
        border-color: transparent;
      }
      50% {
        border-color: var(--text-color);
      }
    }
    
    .spoiler {
        cursor: pointer;
        padding: 5px;
        border: 1px solid #ccc;
    }
    
    .spoiler-content {
        display: none;
    }
    
  </style>
</head>

<body>
  <p>
    <span id="text">dear diary i feel itchy like there's bugs under my skin</span>
  </p><br>
  <p>I have no idea what to put here. Maybe if I code a theme selector, it'll seem like I know what I'm doing, and no one will be able to tell I got my rudimentary HTML and CSS knowledge from a laminated brochure from the '90s. So here's the selector.</p><br>
  
  <div class="spoiler" onclick="toggleSpoiler()">
      POST UMI: SURVIVAL HORROR (tap to see)
      <div class="spoiler-content">
          <img src="uploads/foryoureyes/postumisurvivalhorror.PNG" alt="Error, whoops.">
      </div>
  </div>

  <label for="theme-select">Pick your poison:</label>
  <select id="theme-select">
    <option value="dark">Nic Cage (Dracula)</option>
    <option value="light">Light</option>
    <option value="sepia">Sepia</option> <!-- Nueva opción de tema sepia -->
  </select>

  <script>
    // Script para cambiar el tema según la selección del usuario
    const selectElement = document.getElementById('theme-select');
    const root = document.documentElement;

    selectElement.addEventListener('change', (event) => {
      const theme = event.target.value;
      if (theme === 'dark') {
        root.style.setProperty('--bg-color', '#282a36');
        root.style.setProperty('--text-color', '#f8f8f2');
        root.style.setProperty('--link-color', '#bd93f9');
      } else if (theme === 'light') {
        root.style.setProperty('--bg-color', '#f8f8f2');
        root.style.setProperty('--text-color', '#282a36');
        root.style.setProperty('--link-color', '#6200ea');
      } else if (theme === 'sepia') {
        root.style.setProperty('--bg-color', 'var(--sepia-color)');
        root.style.setProperty('--text-color', '#704214');
        root.style.setProperty('--link-color', '#704214');
      }
    });
  </script>
</body>

</html>
