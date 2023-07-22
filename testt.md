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
    #cat {
      font-family: monospace;
      white-space: pre;
      font-size: 20px;
    }
    #textBubble {
      background-color: #28282B;
      border-radius: 10px;
      padding: 10px;
      margin-top: 20px;
    }
  </style>
</head>

<body>
  <p>
    <span id="text">dear diary i feel itchy like there's bugs under my skin</span>
  </p><br>
  <b>hiatus: 17/07/2023 ~ </b ><br>
  <p><b><a href="http://ininteligible.com/crap">check out some crap</a></b></p>
  <p><b><a href="https://music.youtube.com/playlist?list=PLkXnmiNUtXu4k0EjW1nsuzWER50VAanJZ">the ultimate emo playlist</a></b></p><br>
  <div id="cat">
     /\_/\  
    ( o.o ) 
     > ^ <
  </div>
  <div id="textBubble">
    <p id="randomText">Loading...</p>
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
    // Array of random texts
    const randomTexts = [
      "Hello, human!",
      "Meow! How are you?",
      "I need some catnip.",
      "Purrrfect day!",
      "You're the cat's meow!",
      "I'm feline good!",
      "Feed me, hooman!",
      "Let's paw-ty!",
      "Scratch my belly!",
      "I can haz cheezburger?"
    ];
    
    // Function to choose a random text from the array
    function getRandomText() {
      const randomIndex = Math.floor(Math.random() * randomTexts.length);
      return randomTexts[randomIndex];
    }
    
    // Function to display the random text in the text bubble
    function displayRandomText() {
      const textBubble = document.getElementById("randomText");
      textBubble.textContent = getRandomText();
    }
    
    // Display a random text when the page loads
    displayRandomText();
  </script>
</body>

</html>