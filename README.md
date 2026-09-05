<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Acordes & Teclas - Tienda de Instrumentos Musicales</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <style>
        /* === RESET Y CONFIGURACIÓN GENERAL PARA EVITAR DESBORDAMIENTO === */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Open Sans', sans-serif;
            background-color: #f8f9fa;
            color: #333;
            overflow-x: hidden; /* Evita el desplazamiento horizontal */
        }

        img {
            max-width: 100%;
            height: auto; /* Las imágenes se adaptan automáticamente sin deformarse */
            display: block;
        }

        h1, h2, h3 {
            font-family: 'Montserrat', sans-serif;
        }

        /* === 1. BARRA SUPERIOR === */
        .top-bar {
            background-color: #1a1a1a;
            color: #ddd;
            padding: 8px 5%;
            font-size: 0.85em;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 5px;
        }

        /* === 2. LOGOTIPO === */
        header.logo-section {
            background-color: #fff;
            padding: 20px;
            text-align: center;
            border-bottom: 3px solid #b30000;
        }
        header.logo-section img {
            width: 70px;
            margin: 0 auto;
        }
        header.logo-section h2 {
            margin-top: 10px;
            color: #b30000;
            font-size: 1.8em;
            letter-spacing: 1px;
        }

        /* === 3. MASTHEAD === */
        .masthead {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1511379938547-c1f69419868d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1200&q=80') center/cover;
            color: white;
            text-align: center;
            padding: 80px 20px;
        }
        .masthead h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        .masthead p {
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }

        /* === 4. NAVEGACIÓN (Horizontal por defecto) === */
        nav {
            background-color: #333;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }
        nav ul li a {
            display: block;
            padding: 15px 20px;
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.9em;
            transition: background 0.3s;
        }
        nav ul li a:hover {
            background-color: #b30000;
        }

        /* === 5. CONTENEDOR PRINCIPAL (Contenido + Barra Lateral) === */
        .container {
            display: flex;
            max-width: 1200px;
            margin: 30px auto;
            gap: 30px;
            padding: 0 20px;
        }

        /* Contenido Principal con Artículos */
        main.content {
            flex: 3;
        }
        main.content h2 {
            font-size: 2rem;
            margin-bottom: 25px;
            color: #222;
        }

        /* Grilla de artículos (Se adapta automáticamente a columnas) */
        .articles-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        article {
            background: #fff;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        article:hover {
            transform: translateY(-5px);
        }
        article img {
            border-radius: 5px;
            margin-bottom: 15px;
            height: 160px;
            object-fit: cover;
            width: 100%;
        }
        article h3 {
            color: #b30000;
            margin-bottom: 10px;
        }
        article p {
            color: #666;
            font-size: 0.95em;
        }

        /* Barra Lateral (Aside) */
        aside.sidebar {
            flex: 1;
            background: #fff;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            height: fit-content;
        }
        aside.sidebar h3 {
            color: #222;
            border-bottom: 2px solid #b30000;
            padding-bottom: 8px;
            margin-bottom: 15px;
        }
        aside.sidebar p {
            font-size: 0.95em;
            color: #555;
            margin-bottom: 15px;
            line-height: 1.5;
        }

        /* === 6. PIE DE PÁGINA === */
        footer.footer {
            background-color: #222;
            color: #fff;
            text-align: center;
            padding: 40px 20px;
            margin-top: 50px;
        }
        .sub-footer {
            background-color: #111;
            color: #777;
            text-align: center;
            padding: 15px;
            font-size: 0.85em;
        }

        /* ==========================================================
           RESPONSIVE DESIGN (MEDIA QUERIES PARA CELULARES Y TABLETS)
           ========================================================== */
        @media (max-width: 768px) {
            /* 1. Menú horizontal pasa a vertical */
            nav ul {
                flex-direction: column;
                text-align: center;
            }
            nav ul li a {
                padding: 12px;
                border-bottom: 1px solid #444;
            }

            /* 2. Contenedor principal pasa a columna (Mueve la barra lateral debajo) */
            .container {
                flex-direction: column;
            }

            /* 3. Artículos pasan a una sola columna */
            .articles-grid {
                grid-template-columns: 1fr;
            }

            /* Ajustes estéticos para pantallas pequeñas */
            .masthead h1 {
                font-size: 2rem;
            }
            .top-bar {
                flex-direction: column;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- Barra superior -->
    <div class="top-bar">
        <span>📍 Av. La Música 456, Lima</span>
        <span>📞 (01) 555-4321</span>
    </div>

    <!-- Logotipo -->
    <header class="logo-section">
        <img src="https://cdn-icons-png.flaticon.com/512/3659/3659738.png" alt="Logotipo">
        <h2>Acordes & Teclas</h2>
    </header>

    <!-- Masthead -->
    <section class="masthead">
        <h1>Tu Pasión por la Música</h1>
        <p>Instrumentos de alta calidad para músicos profesionales y aficionados.</p>
    </section>

    <!-- Navegación -->
    <nav>
        <ul>
            <li><a href="#">Inicio</a></li>
            <li><a href="#">Guitarras</a></li>
            <li><a href="#">Teclados</a></li>
            <li><a href="#">Percusión</a></li>
            <li><a href="#">Contacto</a></li>
        </ul>
    </nav>

    <!-- Contenedor Principal: Contenido + Barra Lateral -->
    <div class="container">
        
        <!-- Contenido Principal con Artículos -->
        <main class="content">
            <h2>Nuestros Instrumentos Destacados</h2>
            
            <div class="articles-grid">
                <!-- Artículo 1 -->
                <article>
                    <img src="images (1).jpg" alt="Guitarras Eléctricas">
                    <h3>Guitarras Eléctricas</h3>
                    <p>Gran variedad de modelos Stratocaster, Les Paul y Ibanez con calibración profesional incluida.</p>
                </article>

                <!-- Artículo 2 -->
                <article>
                    <img src="https://images.unsplash.com/photo-1552422535-c45813c61732?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Pianos y Teclados">
                    <h3>Pianos Digitales</h3>
                    <p>Teclados sensitivos de 88 notas con acción de martillo para estudiantes y pianistas avanzados.</p>
                </article>

                <!-- Artículo 3 -->
                <article>
                    <img src="https://images.unsplash.com/photo-1519892300165-cb5542fb47c7?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Baterías">
                    <h3>Baterías Acústicas</h3>
                    <p>Kits completos de percusión con herrajes de alta durabilidad y excelente resonancia.</p>
                </article>

                <!-- Artículo 4 -->
                <article>
                    <img src="https://images.unsplash.com/photo-1598488035139-bdbb2231ce04?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=80" alt="Audio">
                    <h3>Audio y Monitores</h3>
                    <p>Equipamiento esencial para home studios, interfaces de audio y micrófonos de condensador.</p>
                </article>
            </div>
        </main>

        <!-- Barra Lateral (Aside - Se moverá automáticamente debajo en celulares) -->
        <aside class="sidebar">
            <h3>Oferta Especial</h3>
            <p>Obtén un <strong>20% de descuento</strong> en cuerdas y accesorios menores presentando este sitio web en nuestra tienda física.</p>
            <h3>Horarios</h3>
            <p>Lunes a Sábado:<br>10:00 am - 8:00 pm</p>
        </aside>

    </div>

    <!-- Pie de página -->
    <footer class="footer">
        <h3>Acordes & Teclas</h3>
        <p>Equipando a los músicos desde 2015.</p>
    </footer>

    <div class="sub-footer">
        <p>&copy; 2026 Acordes & Teclas. Todos los derechos reservados.</p>
    </div>

</body>
</html>
