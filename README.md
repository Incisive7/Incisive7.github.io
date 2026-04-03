<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manbobobo - Il Gatto Bipede</title>
    <style>
        :root {
            --cat-black: #1a1a1a;
            --eye-white: #ffffff;
            --accent-color: #f1c40f;
        }

        body {
            font-family: 'Courier New', Courier, monospace;
            background-color: #2c3e50;
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 40px;
        }

        .card {
            background-color: var(--cat-black);
            border: 3px solid var(--eye-white);
            border-radius: 20px;
            padding: 30px;
            max-width: 500px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
        }

        .avatar-container {
            background: #333;
            width: 150px;
            height: 150px;
            margin: 0 auto 20px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            border: 2px dashed var(--eye-white);
        }

        /* Rappresentazione stilizzata degli occhi di Manbobobo */
        .eye {
            width: 40px;
            height: 40px;
            background-color: black;
            border: 4px solid white;
            border-radius: 50%;
            display: inline-block;
            margin: 0 10px;
        }

        h1 {
            color: var(--accent-color);
            text-transform: uppercase;
            letter-spacing: 3px;
            margin-bottom: 5px;
        }

        .tag {
            background: var(--eye-white);
            color: black;
            padding: 5px 15px;
            border-radius: 15px;
            font-weight: bold;
            font-size: 0.8rem;
        }

        .description {
            margin-top: 25px;
            line-height: 1.6;
            text-align: left;
        }

        .stats-list {
            list-style: none;
            padding: 0;
            margin-top: 20px;
        }

        .stats-list li {
            margin-bottom: 10px;
            padding-left: 25px;
            position: relative;
        }

        .stats-list li::before {
            content: "🐾";
            position: absolute;
            left: 0;
        }

        footer {
            margin-top: 30px;
            font-size: 0.7rem;
            opacity: 0.6;
        }
    </style>
</head>
<body>

    <div class="card">
        <div class="avatar-container">
            <div class="eye"></div>
            <div class="eye"></div>
        </div>
        
        <span class="tag">PERSONAGGIO ANIMATO</span>
        <h1>Manbobobo</h1>
        
        <div class="description">
            <p><strong>Manbobobo</strong> non è un gatto come tutti gli altri. È un piccolo eroe tascabile dal pelo nerissimo e dalla silhouette... morbidamente rotonda.</p>
            
            <ul class="stats-list">
                <li><strong>Statura:</strong> Estremamente piccolo e "ciciotto".</li>
                <li><strong>Portamento:</strong> Cammina orgogliosamente su due gambe.</li>
                <li><strong>Sguardo:</strong> Occhi neri profondi con un inconfondibile bordo bianco.</li>
                <li><strong>Colore:</strong> Nero assoluto, come un'ombra simpatica.</li>
            </ul>
        </div>
    </div>

    <footer>
        Progetto Manbobobo - Creato per GitHub
    </footer>

</body>
</html>
</html>
