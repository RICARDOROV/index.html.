# index.html.
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Palabra del Día</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: #f0f8ff;
        }
        .container {
            text-align: center;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #333;
        }
        .word {
            font-size: 2rem;
            color: #007acc;
        }
        .meaning {
            margin-top: 10px;
            font-size: 1.2rem;
            color: #555;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Palabra del Día</h1>
        <div class="word" id="word">Cargando...</div>
        <div class="meaning" id="meaning">Por favor espera...</div>
    </div>
    <script>
        const words = [
            { word: "Épico", meaning: "Relativo a la poesía heroica o extraordinario." },
            { word: "Serendipia", meaning: "Hallazgo afortunado e inesperado que se produce cuando se está buscando otra cosa." },
            { word: "Inefable", meaning: "Algo tan increíble que no puede ser expresado con palabras." },
            { word: "Resiliencia", meaning: "Capacidad para adaptarse frente a las adversidades." },
            { word: "Elocuencia", meaning: "Habilidad para expresarse con fluidez y persuasión." }
        ];

        const today = new Date().getDate();
        const dailyWord = words[today % words.length];

        document.getElementById('word').textContent = dailyWord.word;
        document.getElementById('meaning').textContent = dailyWord.meaning;
    </script>
</body>
</html>
