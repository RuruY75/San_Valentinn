<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Quieres ser mi San Valentín?</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&display=swap');

        body {
            background-color: #041E42; /* Azul Pantone */
            color: white;
            font-family: 'Great Vibes', cursive;
            margin: 0;
            padding: 0;
            text-align: center;
            transition: all 0.5s ease;
        }

        h1, h2 {
            color: #c2b280; /* Beige más oscuro */
            transition: 0.3s ease-in-out;
        }

        h1:hover, h2:hover {
            transform: scale(1.05);
        }

        .container {
            width: 90%;
            margin: auto;
            max-width: 800px;
            padding: 20px;
            display: none; /* Escondemos el contenido al principio */
        }

        .section {
            position: relative;
            background-color: rgba(255, 255, 255, 0.15);
            padding: 20px;
            margin: 20px 0;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            transition: 0.3s ease-in-out;
            border: 5px solid #c2b280; /* Marco beige */
        }

        .section:hover {
            transform: scale(1.02);
        }

        .button {
            display: inline-block;
            background-color: #FF8C94;
            color: white;
            padding: 15px 30px;
            border-radius: 25px;
            font-size: 1.2em;
            text-decoration: none;
            transition: 0.3s ease-in-out;
            margin: 10px;
        }

        .button:hover {
            background-color: #ff6b81;
            transform: scale(1.05);
        }

        .button-no {
            background-color: #c2b280; /* Beige más oscuro */
            color: #041E42; /* Azul Pantone */
            padding: 15px 30px;
            border-radius: 25px;
            font-size: 1.2em;
            text-decoration: none;
            transition: 0.3s ease-in-out;
            margin: 10px;
            position: relative;
        }

        .button-no:hover {
            background-color: #041E42; /* Azul Pantone */
            color: #c2b280; /* Beige más oscuro */
            transform: scale(1.05);
        }

        #message {
            display: none;
            font-size: 1.5em;
            color: #FF8C94;
            margin-top: 20px;
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }

        #message.show {
            display: block;
            opacity: 1;
        }

        /* Animación de la carta */
        .card {
            width: 300px;
            height: 400px;
            background-color: #c2b280; /* Beige más oscuro */
            margin: 50px auto;
            border-radius: 15px;
            position: relative;
            cursor: pointer;
            transform: scale(1);
            transition: transform 0.5s ease-in-out;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .card:hover {
            transform: scale(1.05);
        }

        .card-content {
            font-size: 1.3em;
            color: #041E42; /* Azul Pantone */
            text-align: center;
        }

        .card.open {
            transform: scale(0.8);
        }

        .card.open .card-content {
            opacity: 0;
            transition: opacity 0.5s ease-in-out;
        }

        .card.open .container {
            display: block; /* Mostrar el contenido cuando la carta se abre */
        }

    </style>
</head>
<body>

    <div class="card" id="card">
        <div class="card-content">
            <p>Tienes un mensaje importante</p>
        </div>
    </div>

    <div class="container">
        <h1>¿Por qué tú?</h1>
        <div class="section">
            <p>Hemos pasado muchas cosas juntos, primeras veces en muchas cosas, eres tú porque eres la única que realmente ha tocado mi corazón. Quiero que tú seas mi San Valentín porque eres la persona más especial para mí en toda la existencia, eres mi bonita. Quiero que sigamos compartiendo muchos momentos más, juntitos los dos.</p>
        </div>

        <h2>5 razones por las que eres mi elección perfecta</h2>
        <div class="section">
            <p>1. Porque eres perfecta de todas las maneras.</p>
            <p>2. Porque has marcado mi vida como nadie más lo ha hecho.</p>
            <p>3. Porque contigo siento lo que no puedo con nadie más.</p>
            <p>4. Cada vez que estoy contigo me haces vibrar el alma.</p>
            <p>5. Contigo todo es especial.</p>
        </div>

        <h2>Señales de que debes decir sí</h2>
        <div class="section">
            <p>Si al leer esto tu corazón se aceleró, es una señal.</p>
            <p>Si sonreíste en algún momento, es otra señal.</p>
            <p>Si has pensado en mí mientras lees, ya sabes la respuesta.</p>
        </div>

        <h2>¿Quieres ser mi San Valentín?</h2>
        <a href="#" class="button">¡Sí, quiero!</a>
        <a href="#" class="button-no">No</a>

        <div id="message">Eso locona sabía que aceptarias, te quiero muchísimo</div>
    </div>

    <script>
        const card = document.getElementById('card');
        const container = document.querySelector('.container');
        const yesButton = document.querySelector('.button');
        const noButton = document.querySelector('.button-no');
        const message = document.getElementById('message');

        const noMessages = [
            "¿Estás segura?",
            "Di que sí, porfis",
            "¿De verdad no quieres?",
            "Vamos, no seas tímida",
            "Sabes que quiero que digas que sí",
            "Solo un 'sí', porfa"
        ];

        // Cuando se hace clic en la carta
        card.addEventListener('click', () => {
            card.classList.add('open'); // Abrir la carta
            setTimeout(() => {
                container.style.display = "block"; // Mostrar el contenido
            }, 500);
        });

        yesButton.addEventListener('click', () => {
            message.classList.add('show'); // Mostrar mensaje cuando se presiona el botón "Sí"
        });

        noButton.addEventListener('click', () => {
            // Cambiar el texto del botón "No" aleatoriamente
            const randomMessage = noMessages[Math.floor(Math.random() * noMessages.length)];
            noButton.textContent = randomMessage;
        });
    </script>

</body>
</html>
