<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Me perdonas?</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f8ff; /* Color de fondo suave */
            font-family: 'Arial', sans-serif;
            margin: 0;
        }
        .container {
            text-align: center;
            background-color: #ffffff; /* Fondo blanco para el contenedor */
            border-radius: 10px; /* Bordes redondeados */
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1); /* Sombra sutil */
            padding: 30px; /* Espaciado interno */
            max-width: 400px; /* Ancho máximo */
        }
        h1 {
            color: #333; /* Color del texto */
            margin-bottom: 20px; /* Espaciado debajo del título */
        }
        button {
            margin: 10px;
            padding: 15px 30px; /* Padding mejorado */
            font-size: 18px;
            cursor: pointer;
            border: none; /* Sin borde */
            border-radius: 5px; /* Bordes redondeados */
            background-color: #007bff; /* Color de fondo azul */
            color: white; /* Color del texto */
            transition: background-color 0.3s; /* Transición suave */
        }
        button:hover {
            background-color: #0056b3; /* Color al pasar el ratón */
        }
        #mensaje {
            font-size: 24px;
            color: green; /* Color del mensaje */
            margin-top: 20px;
            display: none; /* Ocultar mensaje inicialmente */
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>¿Me perdonas?</h1>
        <button id="botonSi">Sí</button>
        <button id="botonNo">No</button>
        <p id="mensaje"></p>
    </div>

    <script>
        // Acción al presionar "Sí"
        document.getElementById('botonSi').onclick = function() {
            document.getElementById('mensaje').innerText = "Gracias, tqm";
            document.getElementById('mensaje').style.display = "block"; // Mostrar mensaje
            // Desactivar los botones para evitar más clics
            document.getElementById('botonSi').disabled = true;
            document.getElementById('botonNo').disabled = true;
        };

        // Acción al presionar "No"
        document.getElementById('botonNo').onclick = function() {
            // Redirigir a una página aleatoria dentro del mismo sitio infinitamente
            setTimeout(function() {
                window.location.href = window.location.href; // Recargar la página
            }, 100);
        };
    </script>

</body>
</html>
