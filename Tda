<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>¡Conociendo el TDA!</title>
  <style>
    body {
      font-family: Comic Sans MS, cursive, sans-serif;
      background: linear-gradient(to bottom, #e0f7fa, #ffe0f0);
      padding: 20px;
      color: #333;
    }
    h1, h2 {
      color: #d81b60;
      text-align: center;
    }
    section {
      background-color: #ffffffd9;
      border-radius: 15px;
      padding: 20px;
      margin: 15px auto;
      max-width: 800px;
      box-shadow: 2px 4px 10px rgba(0,0,0,0.1);
    }
    ul {
      list-style-type: "⭐ ";
      padding-left: 20px;
    }
    .game {
      text-align: center;
      margin-top: 15px;
    }
    button {
      padding: 12px 20px;
      background-color: #ff80ab;
      border: none;
      border-radius: 10px;
      color: white;
      font-size: 18px;
      cursor: pointer;
    }
    .box {
      width: 120px;
      height: 120px;
      margin: 10px auto;
      border-radius: 12px;
    }
    #memory-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
    }
    .memory-card {
      width: 80px;
      height: 80px;
      background-color: #f8bbd0;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      font-size: 22px;
      cursor: pointer;
    }
  </style>
</head>
<body>

<h1>🌟 ¡Conozcamos el TDA! 🌟</h1>

<section>
  <h2>¿Quién descubrió el TDA?</h2>
  <p>El TDA fue descrito por primera vez en 1902 por el doctor George Still. Observó que algunos niños tenían dificultades para concentrarse o controlar su comportamiento.</p>
</section>

<section>
  <h2>¿Qué es el TDA?</h2>
  <p>El Trastorno por Déficit de Atención (TDA) es cuando a algunos niños les cuesta mucho trabajo concentrarse, poner atención o quedarse quietos por mucho tiempo. A veces se acompaña de hiperactividad (TDAH).</p>
</section>

<section>
  <h2>¿Cómo se siente?</h2>
  <ul>
    <li>Les cuesta terminar tareas o juegos.</li>
    <li>Se distraen con facilidad.</li>
    <li>A veces hablan mucho o se mueven sin parar.</li>
    <li>Olvidan cosas fácilmente.</li>
  </ul>
</section>

<section>
  <h2>¿Qué lo causa?</h2>
  <p>No hay una sola causa, pero puede estar relacionado con el cerebro, la genética o el ambiente. ¡No es culpa del niño ni de los papás!</p>
</section>

<section>
  <h2>¿Cómo se diagnostica?</h2>
  <p>Un médico o psicólogo hace preguntas a los papás, maestros y al niño. A veces usan pruebas para saber cómo piensa y se comporta el niño.</p>
</section>

<section>
  <h2>¿Qué ayuda al TDA?</h2>
  <ul>
    <li>Rutinas claras y horarios fijos.</li>
    <li>Juegos para mejorar la memoria y la atención.</li>
    <li>Apoyo de papás, maestros y especialistas.</li>
    <li>A veces se usan medicamentos.</li>
  </ul>
</section>

<section>
  <h2>🎮 ¡Vamos a jugar!</h2>

  <h3>1. Juego de atención: Haz clic cuando se ponga verde 💚</h3>
  <div class="game">
    <div id="colorBox" class="box" style="background-color:red;"></div>
    <button onclick="checkClick()">¡Haz clic aquí!</button>
    <p id="result"></p>
  </div>

  <h3>2. Juego de memoria: Encuentra los pares 🧠</h3>
  <div id="memory-container" class="game"></div>
</section>

<section>
  <h2>¡Tú puedes!</h2>
  <p>Con ayuda, cariño y juegos, todos los niños pueden aprender y divertirse. ¡Eres increíble tal como eres! 💖</p>
</section>

<script>
  // Juego de Atención
  const colorBox = document.getElementById("colorBox");
  const result = document.getElementById("result");
  const colores = ['red', 'blue', 'green', 'yellow'];
  function cambiarColor() {
    const nuevo = colores[Math.floor(Math.random() * colores.length)];
    colorBox.style.backgroundColor = nuevo;
    return nuevo;
  }
  let actual = cambiarColor();
  setInterval(() => actual = cambiarColor(), 2000);
  function checkClick() {
    if (actual === "green") {
      result.textContent = "¡Muy bien! 💚";
      result.style.color = "green";
    } else {
      result.textContent = "¡Ups! Intenta otra vez.";
      result.style.color = "red";
    }
  }

  // Juego de Memoria
  const pares = ['🐶','🐱','🐭','🐶','🐱','🐭'];
  let cartas = [];
  let memoria = [];
  let seleccionadas = [];

  function cargarJuegoMemoria() {
    cartas = pares.sort(() => 0.5 - Math.random());
    const contenedor = document.getElementById('memory-container');
    contenedor.innerHTML = '';
    cartas.forEach((emoji, i) => {
      const div = document.createElement('div');
      div.className = 'memory-card';
      div.dataset.index = i;
      div.textContent = '❓';
      div.onclick = () => seleccionar(i, div);
      contenedor.appendChild(div);
    });
  }

  function seleccionar(i, div) {
    if (seleccionadas.length >= 2 || memoria.includes(i)) return;
    div.textContent = cartas[i];
    seleccionadas.push({i, div});
    if (seleccionadas.length === 2) {
      setTimeout(() => {
        if (cartas[seleccionadas[0].i] === cartas[seleccionadas[1].i]) {
          memoria.push(seleccionadas[0].i, seleccionadas[1].i);
        } else {
          seleccionadas[0].div.textContent = '❓';
          seleccionadas[1].div.textContent = '❓';
        }
        seleccionadas = [];
      }, 800);
    }
  }

  cargarJuegoMemoria();
</script>

</body>
</html>
