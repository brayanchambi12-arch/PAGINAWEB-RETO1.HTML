<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Instrumentos Musicales</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #111;
        }

        /* ENCABEZADO */
        header {
            background-color: #1769bd;
            color: white;
            text-align: center;
            padding: 20px 10px;
        }

        header h1 {
            margin: 0;
            font-size: 22px;
        }

        header p {
            margin: 8px 0 0;
            font-size: 11px;
        }

        /* MENÚ */
        nav {
            background-color: #144d9e;
            text-align: center;
            padding: 10px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 11px;
            font-weight: bold;
            margin: 0 16px;
        }

        nav a:hover {
            text-decoration: underline;
        }

        /* CONTENEDOR PRINCIPAL */
        .contenedor {
            width: 700px;
            margin: 20px auto;
            display: grid;
            grid-template-columns: 1fr 1fr 195px;
            gap: 12px;
            align-items: start;
        }

        /* TARJETAS */
        .tarjeta {
            background-color: white;
            border-radius: 7px;
            padding: 13px;
            box-shadow: 0 2px 7px rgba(0,0,0,0.15);
        }

        /* IMAGEN / BLOQUE DEL INSTRUMENTO */
        .instrumento {
            height: 152px;
            background-color: #1769bd;
            border-radius: 5px;
            color: white;

            display: flex;
            align-items: center;
            justify-content: center;

            font-size: 30px;
            font-weight: bold;
            text-align: center;
        }

        .instrumento.guitarra {
            background-color: #1769bd;
        }

        .instrumento.piano {
            background-color: #237dcc;
        }

        .instrumento.bateria {
            background-color: #0790c9;
        }

        .instrumento.violon {
            background-color: #0b9ca8;
        }

        /* TEXTO DE TARJETAS */
        .tarjeta h2 {
            color: #0861b9;
            font-size: 16px;
            margin: 9px 0;
        }

        .tarjeta p {
            font-size: 11px;
            line-height: 1.5;
            margin: 0;
        }

        /* BARRA LATERAL */
        .lateral {
            background-color: #dff1fc;
            border-radius: 7px;
            padding: 16px;
        }

        .lateral h2 {
            color: #1455a0;
            font-size: 16px;
            margin: 0 0 10px;
        }

        .lateral ul {
            padding-left: 15px;
            margin: 0;
        }

        .lateral li {
            font-size: 11px;
            margin-bottom: 7px;
        }

        /* PIE */
        footer {
            background-color: #144d9e;
            color: white;
            text-align: center;
            padding: 12px;
            font-size: 11px;
            margin-top: 30px;
        }

        /* RESPONSIVE */
        @media (max-width: 800px) {

            .contenedor {
                width: 95%;
                grid-template-columns: 1fr 1fr;
            }

            .lateral {
                grid-column: 1 / 3;
            }
        }

        @media (max-width: 550px) {

            .contenedor {
                grid-template-columns: 1fr;
            }

            .lateral {
                grid-column: auto;
            }

            nav a {
                display: inline-block;
                margin: 5px 8px;
            }
        }
    </style>
</head>

<body>

    <!-- ENCABEZADO -->
    <header>
        <h1>INSTRUMENTOS MUSICALES</h1>
        <p>Encuentra el instrumento perfecto para expresar tu música</p>
    </header>


    <!-- MENÚ -->
    <nav>
        <a href="#">Inicio</a>
        <a href="#">Instrumentos</a>
        <a href="#">Categorías</a>
        <a href="#">Nosotros</a>
        <a href="#">Contacto</a>
    </nav>


    <!-- CONTENIDO -->
    <main class="contenedor">

        <!-- GUITARRA -->
        <article class="tarjeta">

            <div class="instrumento guitarra">
                🎸 Guitarra
            </div>

            <h2>Guitarras</h2>

            <p>
                Encuentra guitarras acústicas, eléctricas y clásicas
                para principiantes y músicos profesionales.
            </p>

        </article>


        <!-- PIANO -->
        <article class="tarjeta">

            <div class="instrumento piano">
                🎹 Piano
            </div>

            <h2>Pianos</h2>

            <p>
                Descubre pianos digitales y teclados ideales para
                aprender, practicar y realizar presentaciones.
            </p>

        </article>


        <!-- BATERÍA -->
        <article class="tarjeta">

            <div class="instrumento bateria">
                🥁 Batería
            </div>

            <h2>Baterías</h2>

            <p>
                Baterías acústicas y electrónicas para tocar rock,
                pop, jazz y muchos estilos musicales.
            </p>

        </article>


        <!-- VIOLÍN -->
        <article class="tarjeta">

            <div class="instrumento violon">
                🎻 Violín
            </div>

            <h2>Violines</h2>

            <p>
                Violines de diferentes tamaños y acabados para
                estudiantes, aficionados y músicos profesionales.
            </p>

        </article>


        <!-- BARRA LATERAL -->
        <aside class="lateral">

            <h2>Instrumentos populares</h2>

            <ul>
                <li>Guitarras</li>
                <li>Pianos</li>
                <li>Baterías</li>
                <li>Violines</li>
                <li>Saxofones</li>
                <li>Teclados</li>
            </ul>

        </aside>

    </main>


    <!-- PIE DE PÁGINA -->
    <footer>
        © 2026 Instrumentos Musicales - Todos los derechos reservados
    </footer>

</body>
</html>
