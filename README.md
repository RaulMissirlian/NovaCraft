<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NovaCraft | Servidor de Minecraft</title>
    <style>
        /* --- ESTILOS GENERALES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #121214;
            color: #e1e1e6;
            line-height: 1.6;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* --- NAV / ENCABEZADO --- */
        header {
            background-color: #1a1a1e;
            padding: 20px 0;
            border-bottom: 3px solid #8257e5;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #8257e5;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 20px;
        }

        .nav-links a:hover {
            color: #8257e5;
            transition: 0.3s;
        }

        /* --- HERO / BIENVENIDA --- */
        .hero {
            background: linear-gradient(rgba(18, 18, 20, 0.8), rgba(18, 18, 20, 0.9)), url('https://images.unsplash.com/photo-1607988795691-3d0147b43231?q=80&w=1920') no-repeat center center/cover;
            padding: 100px 0;
            text-align: center;
            border-bottom: 1px solid #29292e;
        }

        .hero h1 {
            font-size: 48px;
            margin-bottom: 10px;
            color: #fff;
        }

        .hero p {
            font-size: 18px;
            color: #a8a8b3;
            margin-bottom: 30px;
        }

        .ip-box {
            display: inline-block;
            background-color: #202024;
            padding: 12px 25px;
            border-radius: 8px;
            border: 2px dashed #8257e5;
            font-weight: bold;
            font-size: 20px;
            color: #fff;
            cursor: pointer;
        }

        /* --- SECCIÓN: CARACTERÍSTICAS --- */
        .section {
            padding: 60px 0;
        }

        .section-title {
            text-align: center;
            font-size: 32px;
            margin-bottom: 40px;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 4px;
            background-color: #8257e5;
            margin: 10px auto 0;
            border-radius: 2px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .card {
            background-color: #1a1a1e;
            padding: 30px;
            border-radius: 8px;
            border: 1px solid #29292e;
            text-align: center;
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: #8257e5;
        }

        .card h3 {
            margin-bottom: 15px;
            color: #fff;
        }

        /* --- SECCIÓN EXTRA: REGLAS RÁPIDAS --- */
        .rules-list {
            background-color: #1a1a1e;
            padding: 30px;
            border-radius: 8px;
            border-left: 5px solid #8257e5;
            max-width: 800px;
            margin: 0 auto;
        }

        .rules-list ol {
            padding-left: 20px;
        }

        .rules-list li {
            margin-bottom: 15px;
            font-size: 16px;
        }

        .rules-list strong {
            color: #fff;
        }

        /* --- TIENDA / RANGOS --- */
        .btn-store {
            display: inline-block;
            background-color: #8257e5;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            font-weight: bold;
            margin-top: 15px;
        }

        .btn-store:hover {
            background-color: #9466ff;
        }

        /* --- FOOTER --- */
        footer {
            background-color: #0c0c0d;
            padding: 30px 0;
            text-align: center;
            font-size: 14px;
            color: #737380;
            border-top: 1px solid #1a1a1e;
        }
    </style>
</head>
<body>

    <!-- BARRA DE NAVEGACIÓN -->
    <header>
        <div class="container nav-container">
            <div class="logo">NovaCraft</div>
            <nav>
                <ul class="nav-links">
                    <li><a href="#inicio">Inicio</a></li>
                    <li><a href="#caracteristicas">Características</a></li>
                    <li><a href="#reglas">Reglas</a></li>
                    <li><a href="#tienda">Tienda</a></li>
                    <li><a href="#staff">Staff</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- SECCIÓN DE BIENVENIDA -->
    <section id="inicio" class="hero">
        <div class="container">
            <h1>Bienvenido a NovaCraft</h1>
            <p>Una experiencia de juego única con la mejor comunidad.</p>
            <div class="ip-box" onclick="copiarIP()">
                IP: play.novacraft.me
            </div>
            <p style="margin-top: 15px; font-size: 14px; color: #737380;">¡Haz clic en la IP para copiarla!</p>
        </div>
    </section>

    <!-- CARACTERÍSTICAS -->
    <section id="caracteristicas" class="section">
        <div class="container">
            <h2 class="section-title">¿Por qué jugar con nosotros?</h2>
            <div class="grid">
                <div class="card">
                    <h3>Survival Custom</h3>
                    <p>Misiones diarias, economía equilibrada, protecciones de terreno y un mundo enorme por explorar.</p>
                </div>
                <div class="card">
                    <h3>0% Lag / Host 24/7</h3>
                    <p>Servidor optimizado al máximo para garantizar una fluidez perfecta durante tus partidas cotidianas.</p>
                </div>
                <div class="card">
                    <h3>Eventos Semanales</h3>
                    <p>Torneos, parkour, llaves especiales y recompensas exclusivas para los jugadores más activos.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- SECCIÓN AÑADIDA: REGLAS RÁPIDAS -->
    <section id="reglas" class="section" style="background-color: #16161a;">
        <div class="container">
            <h2 class="section-title">Reglas Básicas</h2>
            <div class="rules-list">
                <ol>
                    <li><strong>Respeto mutuo:</strong> No se tolera el insulto, la toxicidad ni la discriminación en los chats públicos o privados.</li>
                    <li><strong>Juego limpio:</strong> El uso de hacks, clientes modificados que den ventaja o el aprovechamiento de bugs está estrictamente prohibido.</li>
                    <li><strong>Cuidado del mapa:</strong> No está permitido el grifear (destruir) construcciones ajenas o zonas protegidas del servidor.</li>
                </ol>
            </div>
        </div>
    </section>

    <!-- TIENDA -->
    <section id="tienda" class="section">
        <div class="container">
            <h2 class="section-title">Apoya al Servidor</h2>
            <div class="grid">
                <div class="card">
                    <h3>Rango NOVA</h3>
                    <p>Acceso a comandos /fly, kits exclusivos, prefijo en el chat y prioridad al entrar.</p>
                    <a href="#" class="btn-store">Ver Rango</a>
                </div>
                <div class="card">
                    <h3>Rango VIP</h3>
                    <p>Beneficios estéticos, kits iniciales, más hogares (/sethome) y acceso a canales privados.</p>
                    <a href="#" class="btn-store">Ver Rango</a>
                </div>
            </div>
        </div>
    </section>

    <!-- STAFF -->
    <section id="staff" class="section" style="background-color: #16161a;">
        <div class="container">
            <h2 class="section-title">Equipo Administrativo</h2>
            <div class="grid" style="grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));">
                <div class="card">
                    <h3>Admin1</h3>
                    <p style="color: #8257e5; font-weight: bold;">Creador</p>
                </div>
                <div class="card">
                    <h3>Modera_Play</h3>
                    <p style="color: #4cd62b; font-weight: bold;">Moderador</p>
                </div>
            </div>
        </div>
    </section>

    <!-- PIE DE PÁGINA -->
    <footer>
        <div class="container">
            <p>&copy; 2026 NovaCraft. Todos los derechos reservados.</p>
            <p style="font-size: 12px; margin-top: 5px;">No estamos afiliados oficialmente con Mojang Studios.</p>
        </div>
    </footer>

    <!-- SCRIPT INTERACTIVO -->
    <script>
        function copiarIP() {
            // Función simple para alertar la copia (puedes cambiarlo por copiar directo al portapapeles)
            alert("¡IP copiada al portapapeles! Prepárate para entrar a NovaCraft.");
        }
    </script>
</body>
</html>
