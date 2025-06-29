<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Zona Gamer</title>
    <style>
        :root {
            --morado: #e6e6fa;
            --morado-fuerte: #9370db;
            --coral: #ff6f91;
            --dorado: #ffd700;
            --gris: #f8f8f8;
            --oscuro: #2d2d2d;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: white;
            color: var(--oscuro);
            line-height: 1.6;
        }

        header {
            background-color: var(--morado);
            padding: 1em;
            text-align: center;
        }

        header h1 {
            margin-bottom: 10px;
        }

        nav {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 10px;
        }

        nav a {
            text-decoration: none;
            color: var(--oscuro);
            font-weight: bold;
        }

        .btn-suscribete {
            background-color: var(--coral);
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .btn-suscribete:hover {
            background-color: #e85c7d;
        }

        main {
            display: flex;
            flex-wrap: wrap;
            padding: 2em;
            gap: 2em;
            justify-content: center;
        }

        .banner {
            display: block;
            width: 70%;
            max-height: 200px;
            object-fit: cover;
        }

        .contenido {
            flex: 1 1 300px;
            max-width: 600px;
        }

        .control {
            width: 100px;
            margin: 1em 0;
        }

        .barra {
            height: 6px;
            background-color: var(--coral);
            width: 100px;
            margin: 1em 0;
            border-radius: 4px;
        }

        .lineas div {
            background-color: var(--morado-fuerte);
            height: 8px;
            margin: 6px 0;
            border-radius: 4px;
            width: 80%;
        }

        .aside-columna {
            display: flex;
            flex-direction: column;
            gap: 2em;
            flex: 0.5 0.5 150px;
        }

        aside {
            background-color: var(--morado);
            padding: 1em;
            border-radius: 10px;
        }

        aside h3 {
            margin-bottom: 0.5em;
        }

        aside ul {
            list-style: none;
            padding-left: 0;
            margin: 1em 0;
        }

        aside ul li {
            margin-bottom: 0.5em;
        }

        aside ul li a {
            text-decoration: none;
            color: var(--oscuro);
        }

        .iconos {
            margin-top: 1em;
            text-align: center;
        }

        .iconos span {
            font-size: 1.5em;
            margin-right: 10px;
        }

        footer {
            background-color: var(--morado-fuerte);
            text-align: center;
            color: var(--dorado);
            padding: 1em;
            margin-top: 2em;
        }

        .redes-footer {
            margin-top: 1em;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .icono-red {
            width: 32px;
            height: 32px;
            transition: transform 0.3s;
        }

        .icono-red:hover {
            transform: scale(1.2);
        }

        .formulario {
            padding: 1.5em;
            background-color: var(--gris);
            margin: 2em auto;
            border-radius: 12px;
            max-width: 400px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        .formulario h2 {
            margin-bottom: 1em;
            text-align: center;
        }

        .campo {
            margin-bottom: 1em;
        }

        .campo label {
            display: block;
            margin-bottom: 0.4em;
            font-weight: bold;
        }

        .campo input,
        .campo textarea {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 6px;
            transition: border-color 0.3s;
        }

        .campo input:focus,
        .campo textarea:focus {
            border-color: var(--morado-fuerte);
            outline: none;
        }

        .formulario button {
            margin-top: 1em;
            width: 100%;
        }

        @media (max-width: 768px) {
            nav {
                flex-direction: column;
                gap: 10px;
                align-items: center;
            }

            main {
                flex-direction: column;
                padding: 1em;
            }

            .contenido,
            .aside-columna {
                max-width: 100%;
                flex: 1 1 100%;
                margin-left: 0;
            }

            .formulario {
                margin: 1em;
                padding: 1.5em;
                max-width: 90%;
            }

            header h1 {
                font-size: 1.5em;
            }

            .btn-suscribete {
                width: 100%;
                max-width: 200px;
            }

            .iconos {
                text-align: center;
            }
        }

        /* NUEVAS RESEÑAS CON ESTRELLAS */
        .reseñas-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5em;
            margin-top: 2em;
        }

        .tarjeta {
            background-color: var(--gris);
            padding: 1em;
            border-radius: 10px;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
        }

        .tarjeta img {
            width: 100%;
            border-radius: 8px;
            margin-bottom: 0.8em;
        }

        .tarjeta h3 {
            margin: 0.5em 0 0.3em;
            color: var(--oscuro);
        }

        .tarjeta p {
            margin-bottom: 0.5em;
            font-size: 0.95em;
        }

        .estrellas {
            font-size: 1.2em;
            color: var(--dorado);
        }

        /* Estilos para el nuevo sistema de comentarios */
        #comentarios-reseñas {
            background-color: var(--gris);
            padding: 1em;
            border-radius: 10px;
        }

        #comentarios-reseñas h3 {
            margin-bottom: 0.8em;
            text-align: center;
        }

        #comentarios-form .campo {
            margin-bottom: 0.8em;
        }

        #comentarios-form input,
        #comentarios-form textarea {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 6px;
            box-sizing: border-box; /* Asegura que el padding no afecte el ancho total */
        }

        #comentarios-form button {
            width: 100%;
            padding: 10px;
            background-color: var(--coral);
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        #comentarios-form button:hover {
            background-color: #e85c7d;
        }

        #lista-comentarios {
            margin-top: 1.5em;
            border-top: 1px solid #eee;
            padding-top: 1em;
        }

        .comentario-item {
            background-color: #f0f0f0;
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 0.8em;
            margin-bottom: 1em;
        }

        .comentario-item strong {
            display: block;
            margin-bottom: 0.3em;
            color: var(--oscuro);
        }

        .comentario-item small {
            display: block;
            color: #666;
            font-size: 0.8em;
            margin-top: 0.5em;
        }
    </style>
</head>
<body>
    <header>
        <h1>Zona Gamer</h1>
        <nav>
            <a href="#reseñas">Reseñas</a>
            <a href="#enlaces">Redes</a>
            <a href="#contacto">Contacto</a>
            <button class="btn-suscribete">Suscríbete</button>
        </nav>
    </header>

    <main>
        <section class="contenido" id="reseñas">
            <h2>Bienvenido a Zona Gamer</h2>
            <iframe class="banner" width="560" height="315" src="https://www.youtube.com/embed/TU_ID_DE_VIDEO_DE_YOUTUBE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

            <p>En Zona Gamer encontrarás noticias, análisis y reseñas de los videojuegos más populares del momento.
                Nos enfocamos en ofrecerte una visión clara, divertida y actualizada del mundo gaming.</p>
            <div class="barra"></div>
            <div class="lineas">
                <div></div>
                <div></div>
                <div></div>
            </div>

            <h3>Reseñas destacadas</h3>
            <div class="reseñas-grid">
                <article class="tarjeta">
                    <img src="https://img.asmedia.epimg.net/resizer/v2/https%3A%2F%2Fstatic.prisa.com%2Fgamepedia%2Fimagenes%2F2023%2F11%2F20%2Fgame_cover%2F774570624.jpg?auth=36ef38a10aa4e0037af065f66673329eb3f0b7772abfbbcc03cc8c04221955f2&width=280&height=420&smart=true" alt="The Last of Us Part II Remastered" class="banner" />
                    <h3>The Last of Us: Parte II Remasterizado</h3>
                    <p><strong>Análisis:</strong> PS5, PC · <em>hace 1 día</em></p>
                    <p>Esta versión mejorada pule un clásico moderno con gráficos impresionantes y un nuevo modo que revitaliza la tensa aventura de Ellie y Joel. Imperdible.</p>
                    <div class="estrellas">⭐⭐⭐⭐⭐</div>
                </article>

                <article class="tarjeta">
                    <img src="https://img.asmedia.epimg.net/resizer/v2/https%3A%2F%2Fstatic.prisa.com%2Fgamepedia%2Fimagenes%2F2023%2F6%2F9%2Fgame_cover%2F228518559.jpg?auth=437bc5628cbb2a8472c3fb2e1d2a6c8802ee9824396951b7484062b15d2e324b&width=280&height=420&smart=true" alt="Marvel's Spider-Man 2" class="banner" />
                    <h3>Marvel's Spider-Man 2</h3>
                    <p><strong>Análisis:</strong> PS5, PC · <em>hace 2 días</em></p>
                    <p>Peter Parker y Miles Morales se unen para enfrentar nuevas amenazas como Venom y Kraven. Un título lleno de acción, con una jugabilidad fluida y una historia emocionante.</p>
                    <div class="estrellas">⭐⭐⭐⭐⭐</div>
                </article>

                <article class="tarjeta">
                    <img src="https://img.asmedia.epimg.net/resizer/v2/https%3A%2F%2Fstatic.prisa.com%2Fgamepedia%2Fimagenes%2F2024%2F2%2F1%2Fgame_cover%2F730860170.jpg?auth=4a956cb34fe27daf1792ac024aca37ac87db35dec4c6a5b05483053a4a7a49ea&width=280&height=420&smart=true" alt="Death Stranding 2" class="banner" />
                    <h3>Death Stranding 2 - Análisis</h3>
                    <p><strong>Análisis:</strong> PS5 · <em>hace 3 días</em></p>
                    <p>Kojima regresa con una obra que pule detalles jugables y nos ofrece una experiencia artística inolvidable.</p>
                    <div class="estrellas">⭐⭐⭐⭐⭐</div>
                </article>

                <article class="tarjeta">
                    <img src="https://img.asmedia.epimg.net/resizer/v2/https%3A%2F%2Fstatic.prisa.com%2Fgamepedia%2Fimagenes%2F2024%2F05%2F16%2Fgame_cover%2F545788307.jpg?auth=67df546b8639f3704c8df049194b7b7c0a314509050bcc3d7380dbe7d72c7925&width=280&height=420&smart=true" alt="Assassin's Creed Shadows" class="banner" />
                    <h3>Assassin's Creed Shadows</h3>
                    <p><strong>Plataformas:</strong> PC, PS5, Xbox Series · <em>lanzamiento pronto</em></p>
                    <p>Assassin's Creed Shadows es un videojuego de aventura y acción ambientada en el Japón feudal. Vive las historias entrelazadas de Naoe, una experta Assassin shinobi, y Yasuke, el poderoso samurái africano, en los últimos años del turbulento periodo Sengoku.</p>
                    <div class="estrellas">⭐⭐⭐⭐⭐</div>
                </article>

                <article class="tarjeta">
                    <img src="https://sm.ign.com/ign_es/cover/w/warhammer-/warhammer-40000-speed-freeks_16gp.jpg" alt="Speed Freeks">
                    <h3>Warhammer 40,000: Speed Freeks</h3>
                    <p><strong>Análisis:</strong> PC · <em>hace 5 días</em></p>
                    <p>Combina caos, velocidad y explosiones en una experiencia multijugador brutal para los fans de Warhammer.</p>
                    <div class="estrellas">⭐⭐⭐⭐</div>
                </article>

                <article class="tarjeta">
                    <img src="https://alfabetajuega.com/hero/2025/06/fbc-firebreak.1750710536.5157.jpg?width=1200" alt="Firebreak">
                    <h3>FBC: Firebreak</h3>
                    <p><strong>Análisis:</strong> Xbox/PC · <em>hace 7 días</em></p>
                    <p>Acción táctica, buen rendimiento y muchas armas. Ideal para quienes disfrutan de shooters competitivos.</p>
                    <div class="estrellas">⭐⭐⭐⭐</div>
                </article>
            </div>
        </section>

        <div class="aside-columna">
            <aside id="enlaces">
                <h3>Enlaces Recomendados</h3>
                <ul>
                    <li><a href="https://www.youtube.com" target="_blank">⭐ YouTube</a></li>
                    <li><a href="https://www.twitch.tv" target="_blank">⭐ Twitch</a></li>
                    <li><a href="https://discord.com" target="_blank">⭐ Discord</a></li>
                </ul>
                <button class="btn-suscribete">Suscríbete</button>
                <div class="iconos">
                    <span>🎮</span>
                    <span>🐦</span>
                    <span>⭐</span>
                </div>
            </aside>

            <aside id="comentarios-reseñas">
                <h3>Deja tu Comentario</h3>
                <form id="comentarios-form">
                    <div class="campo">
                        <label for="nombre-comentario">Tu Nombre:</label>
                        <input type="text" id="nombre-comentario" name="nombre-comentario" required />
                    </div>
                    <div class="campo">
                        <label for="texto-comentario">Comentario:</label>
                        <textarea id="texto-comentario" name="texto-comentario" rows="4" required></textarea>
                    </div>
                    <button type="submit">Publicar Comentario</button>
                </form>

                <div id="lista-comentarios">
                    <h4>Comentarios:</h4>
                    </div>
            </aside>
            </div>
    </main>

    <section class="formulario" id="contacto">
        <h2>Contáctanos</h2>
        <form onsubmit="return enviarFormulario(event)">
            <div class="campo">
                <label for="nombre">Nombre:</label>
                <input type="text" id="nombre" name="nombre" required />
            </div>

            <div class="campo">
                <label for="email">Correo:</label>
                <input type="email" id="email" name="email" required />
            </div>

            <div class="campo">
                <label for="mensaje">Mensaje:</label>
                <textarea id="mensaje" name="mensaje" rows="4" required></textarea>
            </div>

            <button type="submit" class="btn-suscribete">Enviar</button>
        </form>
    </section>

    <footer>
        <p>©️ 2025 Zona Gamer - Todos los derechos reservados</p>

        <div class="redes-footer">
            <a href="https://www.youtube.com" target="_blank" title="YouTube">
                <img src="https://cdn-icons-png.flaticon.com/512/1384/1384060.png" alt="YouTube" class="icono-red" />
            </a>
            <a href="https://www.twitch.tv" target="_blank" title="Twitch">
                <img src="https://cdn-icons-png.flaticon.com/512/5968/5968819.png" alt="Twitch" class="icono-red" />
            </a>
            <a href="https://discord.com" target="_blank" title="Discord">
                <img src="https://cdn-icons-png.flaticon.com/512/2111/2111370.png" alt="Discord" class="icono-red" />
            </a>
        </div>

    </footer>

    <script>
        function enviarFormulario(e) {
            e.preventDefault();
            alert("¡Gracias por contactarnos! Pronto te responderemos!");
            e.target.reset();
            return false;
        }

        // --- LÓGICA DEL SISTEMA DE COMENTARIOS ---
        const comentariosForm = document.getElementById('comentarios-form');
        const nombreComentarioInput = document.getElementById('nombre-comentario');
        const textoComentarioInput = document.getElementById('texto-comentario');
        const listaComentariosDiv = document.getElementById('lista-comentarios');

        const MAX_COMENTARIOS = 10; // Define el número máximo de comentarios

        // Cargar comentarios al iniciar la página
        document.addEventListener('DOMContentLoaded', cargarComentarios);

        // Manejar el envío del formulario de comentarios
        comentariosForm.addEventListener('submit', function(e) {
            e.preventDefault(); // Evita que la página se recargue

            const nombre = nombreComentarioInput.value.trim();
            const comentario = textoComentarioInput.value.trim();

            if (nombre === '' || comentario === '') {
                alert('Por favor, ingresa tu nombre y un comentario.');
                return;
            }

            const fecha = new Date().toLocaleString('es-ES', { day: '2-digit', month: '2-digit', year: 'numeric', hour: '2-digit', minute: '2-digit' });

            const nuevoComentario = {
                nombre: nombre,
                texto: comentario,
                fecha: fecha
            };

            guardarComentario(nuevoComentario);
            // No llamamos a mostrarComentario directamente, sino a cargarComentarios
            // para que se gestione el límite y el orden.
            cargarComentarios();

            // Limpiar el formulario
            comentariosForm.reset();
        });

        // Función para cargar los comentarios desde localStorage
        function cargarComentarios() {
            const comentariosGuardados = localStorage.getItem('zonaGamerComentarios');
            let comentarios = [];
            if (comentariosGuardados) {
                comentarios = JSON.parse(comentariosGuardados);
            }

            // Limpiar el contenedor actual de comentarios
            listaComentariosDiv.innerHTML = '<h4>Comentarios:</h4>';

            if (comentarios.length === 0) {
                const noComentarios = document.createElement('p');
                noComentarios.textContent = 'Aún no hay comentarios. ¡Sé el primero en dejar uno!';
                listaComentariosDiv.appendChild(noComentarios);
            } else {
                // Mostrar los comentarios, empezando por los más recientes (últimos 10)
                // Usamos slice(-MAX_COMENTARIOS) para obtener los últimos 10
                // y luego reverse() para mostrarlos del más nuevo al más viejo
                comentarios.slice(-MAX_COMENTARIOS).reverse().forEach(comentario => {
                    const comentarioItem = document.createElement('div');
                    comentarioItem.classList.add('comentario-item');

                    const nombreElement = document.createElement('strong');
                    nombreElement.textContent = comentario.nombre;
                    comentarioItem.appendChild(nombreElement);

                    const textoElement = document.createElement('p');
                    textoElement.textContent = comentario.texto;
                    comentarioItem.appendChild(textoElement);

                    const fechaElement = document.createElement('small');
                    fechaElement.textContent = `Publicado el: ${comentario.fecha}`;
                    comentarioItem.appendChild(fechaElement);

                    listaComentariosDiv.appendChild(comentarioItem);
                });
            }
        }

        // Función para guardar un nuevo comentario en localStorage y gestionar el límite
        function guardarComentario(comentario) {
            const comentariosGuardados = localStorage.getItem('zonaGamerComentarios');
            let comentarios = [];
            if (comentariosGuardados) {
                comentarios = JSON.parse(comentariosGuardados);
            }

            comentarios.push(comentario); // Agrega el nuevo comentario al final

            // Si hay más de MAX_COMENTARIOS, elimina el más antiguo (el primero del array)
            if (comentarios.length > MAX_COMENTARIOS) {
                comentarios.shift(); // Elimina el primer elemento del array
            }

            localStorage.setItem('zonaGamerComentarios', JSON.stringify(comentarios));
        }

        // --- LÓGICA ADICIONAL PARA SIMULAR COMENTARIOS DE BOT (OPCIONAL) ---
        // Si quisieras que hubiera comentarios "pre-cargados" como si fueran de bots
        // o para probar, puedes añadir un array inicial y cargarlo en localStorage
        // solo si no hay comentarios ya.
        // Descomenta el siguiente bloque si quieres probarlo:

        /*
        function inicializarComentariosDeBot() {
            if (!localStorage.getItem('zonaGamerComentarios')) {
                const comentariosIniciales = [
                    { nombre: "GamerPro99", texto: "¡Excelente reseña de The Last of Us Part II! Estoy de acuerdo con cada palabra.", fecha: "26/06/2025, 10:00 PM" },
                    { nombre: "PixelPioneer", texto: "Spider-Man 2 es increíble, ¡la mejor experiencia de superhéroes hasta ahora!", fecha: "26/06/2025, 10:05 PM" },
                    { nombre: "ComandoCritico", texto: "Death Stranding 2 es una obra de arte, Kojima nunca decepciona.", fecha: "26/06/2025, 10:15 PM" },
                    { nombre: "Jugador Casual", texto: "Me encantan los juegos de un solo jugador, ¡esta página es genial!", fecha: "26/06/2025, 10:20 PM" },
                    { nombre: "FanDeRPG", texto: "Espero más reseñas de RPGs en el futuro.", fecha: "26/06/2025, 10:25 PM" }
                ];
                localStorage.setItem('zonaGamerComentarios', JSON.stringify(comentariosIniciales));
            }
        }
        // Llama a esta función una vez al cargar la página si quieres pre-cargar
        // comentarios solo la primera vez que un usuario visita el sitio.
        // Si ya hay comentarios en el localStorage del usuario, no hará nada.
        inicializarComentariosDeBot();
        cargarComentarios(); // Vuelve a cargar para mostrar los comentarios iniciales si se añadieron
        */
    </script>
</body>
</html>
