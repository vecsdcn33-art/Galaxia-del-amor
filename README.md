# Galaxia-del-amor
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Galaxia de Amor</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: radial-gradient(circle at center, #0b0014 0%, #000000 100%);
      color: #fff;
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
      text-align: center;
    }
    h1 {
      font-size: 3em;
      margin-top: 40px;
      color: #ff69b4;
      text-shadow: 0 0 15px #ff69b4;
    }
    .heart {
      font-size: 4em;
      animation: pulse 2s infinite;
      color: #ff1493;
    }
    @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.2); }
      100% { transform: scale(1); }
    }
    .stars {
      position: absolute;
      width: 100%;
      height: 100%;
      background: url('https://www.transparenttextures.com/patterns/stardust.png');
      opacity: 0.2;
      z-index: -1;
      animation: twinkle 12s infinite;
    }
    @keyframes twinkle {
      0%, 100% { opacity: 0.2; }
      50% { opacity: 0.5; }
    }
    .chapter {
      margin: 20px auto;
      width: 70%;
      font-size: 1.2em;
      display: none;
    }
    .controls {
      margin-top: 30px;
    }
    button {
      background-color: #ff69b4;
      border: none;
      padding: 10px 20px;
      margin: 5px;
      color: white;
      font-size: 1em;
      cursor: pointer;
      border-radius: 5px;
      box-shadow: 0 0 10px #ff69b4;
    }
    button:hover {
      background-color: #ff1493;
    }
  </style>
</head>
<body>
  <div class="stars"></div>
  <h1>🌌 Galaxia de Amor</h1>
  <div class="heart">💖</div>

  <div class="controls">
    <button onclick="showChapter(1)">Capítulo 1</button>
    <button onclick="showChapter(2)">Capítulo 2</button>
    <button onclick="showChapter(3)">Capítulo 3</button>
  </div>

  <div id="chapter1" class="chapter">
    <p>Hace eones, dos estrellas errantes se encontraron en la vastedad del universo. Su colisión no fue destrucción, sino creación: nació la Galaxia de Amor.</p>
  </div>
  <div id="chapter2" class="chapter">
    <p>En el corazón de esta galaxia, una constelación llamada *Corazón Eterno* guía a los viajeros perdidos hacia el amor verdadero. Sus luces laten al ritmo de los sentimientos.</p>
  </div>
  <div id="chapter3" class="chapter">
    <p>Dicen que si dos almas se miran bajo la Nebulosa Rosada, sus destinos se entrelazan para siempre. ¿Te atreves a explorarla?</p>
  </div>

  <audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-love.mp3" type="audio/mpeg">
    Tu navegador no soporta audio HTML5.
  </audio>

  <script>
    function showChapter(num) {
      for (let i = 1; i <= 3; i++) {
        document.getElementById("chapter" + i).style.display = "none";
      }
      document.getElementById("chapter" + num).style.display = "block";
    }
  </script>
</body>
</html>
