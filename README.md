# pagina-web-est-tica
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Variedades y Papelería La Reja - Mejoras</title>
    
    <link rel="stylesheet" href="styles.css">

    <script>
        // Función para simular una solicitud al servidor
        function obtenerInventario() {
            // Se simulan datos que un servidor enviaría al cliente
            const productos = [
                { nombre: "Cuaderno Profesional", precio: "$2.500" },
                { nombre: "Bolígrafo Tinta Negra", precio: "$1.000" },
                { nombre: "Carpeta de Oficio", precio: "$3.200" }
            ];

            // El cliente (navegador) recibe los datos y actualiza la página
            const lista = document.getElementById('lista-productos');
            lista.innerHTML = '<h4>Inventario Recibido del Servidor:</h4>';
            
            productos.forEach(producto => {
                const item = document.createElement('p');
                item.textContent = `${producto.nombre} - ${producto.precio}`;
                lista.appendChild(item);
            });
        }
    </script>
</head>
<body>
    <h1>VARIEDADES Y PAPELERIA LA REJA</h1>
    <p class="descripcion">
        Bienvenidos a su papelería de confianza. Aquí encontrarás todo lo que necesitas para tu oficina y escuela.
    </p>

    <div class="caja-interaccion">
        <p>
            El <strong>cliente</strong> (tu navegador) <span class="solicitud">solicita información</span>, y el <strong>servidor</strong> la <span class="respuesta">procesa y envía</span>.
        </p>
        <p>
            Haz clic en el botón para simular una solicitud al servidor y cargar nuestro inventario.
        </p>
        <button onclick="obtenerInventario()">Ver Inventario</button>
        <div id="lista-productos" class="inventario-caja">
            </div>
    </div>
</body>
</html>
