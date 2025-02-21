# ABC
Abecedario
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ABC Challenge</title>

    <!-- Vincular el archivo CSS -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Imágenes en el abecedario -->
    <h1>Abecedario con imágenes</h1>
    <div id="alphabet">
        <img src="images/a.png" alt="Letra A">
        <img src="images/b.png" alt="Letra B">
        <img src="images/c.png" alt="Letra C">
        <!-- Agregar más imágenes según sea necesario -->
    </div>

    <!-- Encabezados visibles para aplicar colores -->
    <h3 class="color-blue">Este es un h3 azul</h3>
    <h3 class="color-red">Este es un h3 rojo</h3>
    <h3>Este es un h3 con color predeterminado</h3>

    <!-- Encabezado h5 interactivo -->
    <h5 id="interactive-h5">Haz clic aquí para cambiar de color</h5>

    <!-- Vincular el archivo JavaScript -->
    <script src="script.js"></script>
</body>
</html>

CSS
/* Cambiar el fondo de toda la página a gris */
body {
    background-color: gray;
}

/* Cambiar el color del h3 a verde por defecto */
h3 {
    color: green;
}
Javascript
/* Clase para aplicar el color azul a h3 específicos */
.color-blue {
    color: blue;
}

/* Clase para aplicar el color rojo a h3 específicos */
.color-red {
    color: red;
}

// Cambiar colores aleatorios cuando se hace clic en el h5
document.getElementById("interactive-h5").addEventListener("click", function() {
    // Lista de colores aleatorios
    const colors = ["green", "blue", "red"];
    
    // Elegir un color aleatorio
    const randomColor = colors[Math.floor(Math.random() * colors.length)];

    // Cambiar el color del texto
    this.style.color = randomColor;
});
