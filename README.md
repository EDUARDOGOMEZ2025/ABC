# ABC
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abecedario Interactivo</title>

    <!-- Vincular el archivo CSS -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Encabezado principal -->
    <h1>Abecedario con imágenes</h1>

    <!-- Contenedor con imágenes del abecedario -->
    <div id="alphabet">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a3/Letter_A.svg" alt="Letra A">
        <img src="https://upload.wikimedia.org/wikipedia/commons/b/bd/Letter_B.svg" alt="Letra B">
        <img src="https://upload.wikimedia.org/wikipedia/commons/c/c5/Letter_C.svg" alt="Letra C">
        <img src="https://upload.wikimedia.org/wikipedia/commons/d/d8/Letter_D.svg" alt="Letra D">
        <img src="https://upload.wikimedia.org/wikipedia/commons/e/e5/Letter_E.svg" alt="Letra E">
        <img src="https://upload.wikimedia.org/wikipedia/commons/f/f7/Letter_F.svg" alt="Letra F">
        <img src="https://upload.wikimedia.org/wikipedia/commons/g/g0/Letter_G.svg" alt="Letra G">
        <img src="https://upload.wikimedia.org/wikipedia/commons/8/89/Letter_H.svg" alt="Letra H">
        <img src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Letter_I.svg" alt="Letra I">
        <img src="https://upload.wikimedia.org/wikipedia/commons/6/62/Letter_J.svg" alt="Letra J">
        <img src="https://upload.wikimedia.org/wikipedia/commons/1/1d/Letter_K.svg" alt="Letra K">
        <img src="https://upload.wikimedia.org/wikipedia/commons/9/91/Letter_L.svg" alt="Letra L">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Letter_M.svg" alt="Letra M">
        <img src="https://upload.wikimedia.org/wikipedia/commons/0/0a/Letter_N.svg" alt="Letra N">
        <img src="https://upload.wikimedia.org/wikipedia/commons/d/d8/Letter_O.svg" alt="Letra O">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/a0/Letter_P.svg" alt="Letra P">
        <img src="https://upload.wikimedia.org/wikipedia/commons/4/4f/Letter_Q.svg" alt="Letra Q">
        <img src="https://upload.wikimedia.org/wikipedia/commons/d/d8/Letter_R.svg" alt="Letra R">
        <img src="https://upload.wikimedia.org/wikipedia/commons/f/f7/Letter_S.svg" alt="Letra S">
        <img src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Letter_T.svg" alt="Letra T">
        <img src="https://upload.wikimedia.org/wikipedia/commons/3/35/Letter_U.svg" alt="Letra U">
        <img src="https://upload.wikimedia.org/wikipedia/commons/4/4e/Letter_V.svg" alt="Letra V">
        <img src="https://upload.wikimedia.org/wikipedia/commons/3/3b/Letter_W.svg" alt="Letra W">
        <img src="https://upload.wikimedia.org/wikipedia/commons/1/18/Letter_X.svg" alt="Letra X">
        <img src="https://upload.wikimedia.org/wikipedia/commons/b/b4/Letter_Y.svg" alt="Letra Y">
        <img src="https://upload.wikimedia.org/wikipedia/commons/a/ab/Letter_Z.svg" alt="Letra Z">
    </div>

    <!-- Encabezados con estilos para aplicar colores -->
    <h3 class="color-blue">Este es un h3 azul</h3>
    <h3 class="color-red">Este es un h3 rojo</h3>
    <h3>Este es un h3 con color predeterminado</h3>

    <!-- Encabezado interactivo con evento de clic -->
    <h5 id="interactive-h5">Haz clic aquí para cambiar de color</h5>

    <!-- Vinculación del archivo JavaScript -->
    <script src="script.js"></script>
</body>
</html>
/* Cambiar el fondo de toda la página a gris */
body {
    background-color: gray;
    font-family: Arial, sans-serif;
    text-align: center;
    padding: 20px;
}

/* Estilizar las imágenes de las letras */
#alphabet img {
    width: 50px;
    height: 50px;
    margin: 5px;
    border: 2px solid black;
    border-radius: 5px;
    transition: transform 0.2s ease-in-out;
}

/* Efecto al pasar el mouse por las imágenes */
#alphabet img:hover {
    transform: scale(1.2);
}

/* Cambiar el color por defecto de los h3 a verde */
h3 {
    color: green;
}

/* Clase para aplicar el color azul */
.color-blue {
    color: blue;
}

/* Clase para aplicar el color rojo */
.color-red {
    color: red;
}

/* Encabezado interactivo con estilos específicos */
#interactive-h5 {
    color: white;
    background-color: black;
    padding: 10px;
    display: inline-block;
    cursor: pointer;
    border-radius: 5px;
}

/* Efecto de hover en el encabezado h5 */
#interactive-h5:hover {
    background-color: darkgray;
}
// Cambiar colores aleatorios cuando se hace clic en el h5
document.getElementById("interactive-h5").addEventListener("click", function () {
    // Lista de colores aleatorios
    const colors = ["green", "blue", "red"];
    
    // Elegir un color aleatorio
    const randomColor = colors[Math.floor(Math.random() * colors.length)];

    // Cambiar el color del texto
    this.style.color = randomColor;
});

// Agregar interactividad a las letras del abecedario
const alphabetImages = document.querySelectorAll("#alphabet img");

// Función para mostrar una alerta cuando se hace clic en una letra
alphabetImages.forEach((img) => {
    img.addEventListener("click", function () {
        // Obtener la letra desde el atributo 'alt'
        const letter = this.alt.split(" ")[1]; // Extrae la letra del texto 'Letra X'
        
        // Mostrar alerta con el mensaje
        alert(`Has hecho clic en la letra: ${letter}`);
        
        // Mostrar un mensaje en la consola
        console.log(`Interacción detectada en la letra: ${letter}`);
    });
});
