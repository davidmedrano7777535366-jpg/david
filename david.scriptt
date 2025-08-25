const preguntas = [
  {
    texto: "¿messi es mejor que cristiano?",
    opciones: [
      "si",
      "no",
      "tal vez",
      "nunca"
    ],
    correcta: 1
  },
  {
    texto: "¿lamin es mejor que mastantuono?",
    opciones: [
      "si",
      "siempre",
      "no",
      "nunca"
    ],
    correcta: 2
  },
  {
    texto: "¿argentina es campeon del mundo?",
    opciones: [
      "si ",
      "hizo trampa",
      "no",
      "era facil francia"
    ],
    correcta: 1
  },
  {
    texto: "¿Cuál es una ventaja de Starlink?",
    opciones: [
      "Requiere cableado",
      "Solo funciona en ciudades",
      "Permite conexión en zonas rurales",
      "Solo se usa en Estados Unidos"
    ],
    correcta: 2
  }
];

let preguntaActual = 0;

function mostrarPregunta() {
  const p = preguntas[preguntaActual];
  document.getElementById("pregunta").innerText = p.texto;

  const opcionesDiv = document.getElementById("opciones");
  opcionesDiv.innerHTML = "";

  p.opciones.forEach((opcion, index) => {
    const div = document.createElement("div");
    div.className = "opcion";
    div.innerText = opcion;
    div.onclick = () => verificarRespuesta(index);
    opcionesDiv.appendChild(div);
  });

  document.getElementById("resultado").innerText = "";
}

function verificarRespuesta(indiceSeleccionado) {
  const p = preguntas[preguntaActual];
  const resultado = document.getElementById("resultado");

  if (indiceSeleccionado === p.correcta) {
    resultado.innerText = "✅ ¡Correcto!";
  } else {
    resultado.innerText = `❌ Incorrecto. La respuesta era: "${p.opciones[p.correcta]}"`;
  }
}

function siguientePregunta() {
  if (preguntaActual < preguntas.length - 1) {
    preguntaActual++;
    mostrarPregunta();
  } else {
    document.getElementById("pregunta").innerText = "🎉 ¡Trivia finalizada!";
    document.getElementById("opciones").innerHTML = "";
    document.getElementById("resultado").innerText = "";
  }
}

mostrarPregunta();

