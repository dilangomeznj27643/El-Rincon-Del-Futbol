<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Página Interactiva - Nacional, Juego y Formulario</title>         
  <style>  
    /* --- ESTILOS GENERALES --- */
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f0f0f0;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    header {
      background-color: #006400;
      width: 100%;
      padding: 15px 0;
      text-align: center;
      color: white;
      font-size: 22px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.3);
    }

    nav {
      margin: 15px 0;
    }

    nav button {
      background-color: #2e8b57;
      color: white;
      border: none;
      padding: 10px 20px;
      margin: 0 10px;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
      transition: background-color 0.3s ease;
    }

    nav button:hover {
      background-color: #1e6f43;
    }

    section {
      display: none;
      width: 100%;
      max-width: 1000px;
      background-color: white;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
      border-radius: 8px;
      padding: 20px;
      margin-bottom: 30px;
    }

    section.active {
      display: block;
    }

    /* --- ESTILOS DE LA PRIMERA SECCIÓN (NACIONAL 2016) --- */
    #nacional {
      background-image: url('https://www.valoraanalitik.com/wp-content/uploads/2023/06/Atletico-Nacional-1-1024x597.jpg');
      background-size: cover;
      background-position: center;
      color: #333;
    }

    #nacional .overlay {
      background-color: rgba(255, 255, 255, 0.85);
      padding: 20px;
      border-radius: 8px;
    }

    #nacional h1, #nacional h2 {
      color: #006400;
    }

    #nacional img {
      display: block;
      margin: 10px auto;
      max-width: 100%;
      border-radius: 6px;
    }

    iframe {
      display: block;
      margin: 20px auto;
      max-width: 100%;
      border-radius: 8px;
    }

    /* --- ESTILOS DE LA SEGUNDA SECCIÓN (JUEGO DE MEMORIA) --- */
    #juego {
      background-image: url('https://www.marketingregistrado.com/img/noticias/champions-league-stadium.jpg');
      background-size: cover;
      background-position: center;
      color: white;
      text-shadow: 1px 1px 3px rgba(0,0,0,0.7);
    }

    #juego .game-info {
      text-align: center;
    }

    #juego button {
      background-color: #3498db;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 16px;
      margin-bottom: 20px;
      padding: 10px 20px;
    }

    #juego button:hover {
      background-color: #2980b9;
    }

    .game-container {
      display: grid;
      grid-template-columns: repeat(5, 100px);
      grid-gap: 10px;
      justify-content: center;
      margin: 20px auto;
    }

    .card {
      width: 100px;
      height: 100px;
      background-color: rgba(44, 62, 80, 0.8);
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 10px;
      cursor: pointer;
    }

    .card img {
      width: 80%;
      display: none;
    }

    .flipped {
      background-color: rgba(236, 240, 241, 0.9);
    }

    .flipped img {
      display: block;
    }

    .matched {
      background-color: #27ae60;
    }

    /* --- ESTILOS DE LA TERCERA SECCIÓN (FORMULARIO) --- */
    #formulario {
      background-color: #f4f4f4;
    }

    #formulario .container {
      width: 100%;
      max-width: 600px;
      margin: auto;
      background-color: #fff;
      padding: 20px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
    }

    #formulario input, #formulario select {
      width: 100%;
      padding: 10px;
      margin: 5px 0 15px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    #formulario input[type="submit"] {
      background-color: #4CAF50;
      color: white;
      border: none;
      cursor: pointer;
    }

    #formulario input[type="submit"]:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>

  <header>El Rincon Del Futbol</header>

  <nav>
    <button onclick="mostrarSeccion('nacional')">🏆 Nacional 2016</button>
    <button onclick="mostrarSeccion('juego')">🧠 Juego de Memoria</button>
    <button onclick="mostrarSeccion('formulario')">📝 Registro</button>
  </nav>

  <!-- SECCIÓN 1: NACIONAL -->
  <section id="nacional" class="active">
    <div class="overlay">
      <h1>Atlético Nacional - Libertadores 2016</h1>
      <h2>Introducción</h2>
      <p>Atlético Nacional de Medellín se coronó campeón de la Copa Libertadores 2016, logrando así su segundo título continental después del obtenido en 1989. El equipo dirigido por Reinaldo Rueda desplegó un fútbol vistoso, sólido en defensa y efectivo en ataque, siendo considerado por muchos como el mejor equipo de América en ese año</p>
      <img src="https://cdn.conmebol.com/wp-content/uploads/2016/07/verde_5.jpg" width="400">
      <h2>La Campaña</h2>
        <p>Atlético Nacional realizó una campaña histórica en la Copa Libertadores 2016. El equipo fue primero en la fase de grupos con 16 puntos, la cifra más alta de ese año. Posteriormente, eliminó a Huracán (Argentina), Rosario Central (Argentina) y Sao Paulo (Brasil), para finalmente disputar la final contra Independiente del Valle (Ecuador).</p>
        <img src="https://elcomercio.pe/resizer/ovVcs3jvBQDEOm89-N5XKmgoGuA=/619x347/smart/filters:format(jpeg):quality(75)/arc-anglerfish-arc2-prod-elcomercio.s3.amazonaws.com/public/CIUFYT3W7FG73FXQRFCKBOFSVA.jpg" alt="Campaña de Atlético Nacional en la Libertadores" width="400">
      <h2>La Final</h2>
      <p>La final se jugó en dos partidos. En la ida, en Quito, el resultado fue 1-1 con gol de Orlando Berrío. En la vuelta, en Medellín, el 27 de julio de 2016, Miguel Borja anotó el gol de la victoria que le dio el título a Atlético Nacional. El marcador global fue 2-1, consagrando al club como campeón continental.</p>
</p>
      <img src="https://cloudfront-us-east-1.images.arcpublishing.com/eluniverso/B4VA4CELD5AKHCSEGZT3SW6VMY.jpg" width="400">
      <h2>El Momento del Título</h2>
      <iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/I4608ZDrmFk" allowfullscreen></iframe>
    </div>
  </section>
[Creado por Dilan Gomez y Sebastian Zuluaga]

  <!-- SECCIÓN 2: JUEGO -->
  <section id="juego">
    <div class="game-info">
      <h1>Juego de Memoria</h1>
      <p>Encuentra las parejas de cartas.</p>
      <div id="timer">Tiempo restante: 60s</div>
      <button id="resetButton">Reiniciar Juego</button>
    </div>
    <div class="game-container" id="gameContainer"></div>
  </section>

  <!-- SECCIÓN 3: FORMULARIO -->
  <section id="formulario">
    <div class="container">
      <h2>Formulario de Registro</h2>
      <form>
        <label>Nombre Completo:</label>
        <input type="text" required>
        <label>Correo Electrónico:</label>
        <input type="email" required>
        <label>Contraseña:</label>
        <input type="password" required>
        <label>Fecha de Nacimiento:</label>
        <input type="date" required>
        <label>Género:</label>
        <select required>
          <option value="">Seleccionar...</option>
          <option value="masculino">Masculino</option>
          <option value="femenino">Femenino</option>
          <option value="otro">Otro</option>
        </select>
        <label>
          <input type="checkbox" required> Acepto los términos y condiciones
        </label>
        <input type="submit" value="Registrar">
      </form>
    </div>
  </section>

  <script>
    // --- CAMBIO DE SECCIONES ---
    function mostrarSeccion(id) {
      document.querySelectorAll('section').forEach(sec => sec.classList.remove('active'));
      document.getElementById(id).classList.add('active');
    }

    // --- JUEGO DE MEMORIA ---
    const cards = [
      { id: 1, image: 'https://img.a.transfermarkt.technology/portrait/big/28003-1740766555.jpg?lm=1' },
      { id: 2, image: 'https://assets.realmadrid.com/is/image/realmadrid/1330603286208?$Mobile$&fit=wrap&wid=312' },
      { id: 3, image: 'https://img.a.transfermarkt.technology/portrait/big/68290-1692601435.jpg?lm=1' },
      { id: 4, image: 'https://img.a.transfermarkt.technology/portrait/big/88103-1720681352.jpg?lm=1' },
      { id: 5, image: 'https://img.a.transfermarkt.technology/portrait/big/342229-1682683695.jpg?lm=1' },
      { id: 6, image: 'https://img.a.transfermarkt.technology/portrait/big/27992-1687776160.jpg?lm=1' },
      { id: 7, image: 'https://img.a.transfermarkt.technology/portrait/big/42457-1696364738.jpg?lm=1' },
      { id: 8, image: 'https://img.a.transfermarkt.technology/portrait/big/73396-1722444561.JPG?lm=1' },
      { id: 9, image: 'https://img.a.transfermarkt.technology/portrait/big/39152-1721184791.JPG?lm=1' },
      { id: 10, image: 'https://img.a.transfermarkt.technology/portrait/big/88998-1570439934.jpg?lm=1' },
    ];
    let allCards = [], flippedCards = [], matchedCards = [];
    let timeLeft = 60, timerInterval;

    const gameContainer = document.getElementById('gameContainer');
    const timerElement = document.getElementById('timer');
    const resetButton = document.getElementById('resetButton');

    resetButton.addEventListener('click', resetGame);

    function shuffle(array) {
      let newArray = array.slice();
      for (let i = newArray.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [newArray[i], newArray[j]] = [newArray[j], newArray[i]];
      }
      return newArray;
    }

    function createBoard() {
      gameContainer.innerHTML = '';
      allCards.forEach(card => {
        const cardElement = document.createElement('div');
        cardElement.classList.add('card');
        cardElement.dataset.id = card.id;
        const img = document.createElement('img');
        img.src = card.image;
        cardElement.appendChild(img);
        cardElement.addEventListener('click', () => flipCard(cardElement, card));
        gameContainer.appendChild(cardElement);
      });
    }

    function flipCard(cardElement, card) {
      if (flippedCards.length === 2 || cardElement.classList.contains('flipped') || cardElement.classList.contains('matched')) return;
      cardElement.classList.add('flipped');
      flippedCards.push({ cardElement, card });
      if (flippedCards.length === 2) setTimeout(checkMatch, 600);
    }

    function checkMatch() {
      const [first, second] = flippedCards;
      if (first.card.id === second.card.id) {
        first.cardElement.classList.add('matched');
        second.cardElement.classList.add('matched');
        matchedCards.push(first.card.id);
      } else {
        first.cardElement.classList.remove('flipped');
        second.cardElement.classList.remove('flipped');
      }
      flippedCards = [];
      if (matchedCards.length === cards.length) {
        clearInterval(timerInterval);
        alert('¡Felicidades, encontraste todas las parejas!');
      }
    }

    function startTimer() {
      timerElement.textContent = `Tiempo restante: ${timeLeft}s`;
      timerInterval = setInterval(() => {
        timeLeft--;
        timerElement.textContent = `Tiempo restante: ${timeLeft}s`;
        if (timeLeft <= 0) {
          clearInterval(timerInterval);
          alert('¡Se acabó el tiempo!');
        }
      }, 1000);
    }

    function resetGame() {
      clearInterval(timerInterval);
      timeLeft = 60;
      flippedCards = [];
      matchedCards = [];
      allCards = shuffle([...cards, ...cards]);
      createBoard();
      startTimer();
    }

    // Iniciar juego al cargar
    resetGame();
  </script>
</body>
</html>
