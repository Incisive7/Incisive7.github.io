<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Il Mondo di Manbobobo</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive, sans-serif;
            background-color: #121212;
            color: white;
            text-align: center;
            margin: 0;
            padding: 20px;
        }

        nav {
            margin-bottom: 30px;
            padding: 15px;
            background: #1f1f1f;
            border-radius: 15px;
        }

        button {
            padding: 12px 25px;
            margin: 10px;
            font-size: 1.1rem;
            cursor: pointer;
            border: none;
            border-radius: 50px;
            transition: 0.3s;
            font-weight: bold;
        }

        .btn-roblox { background-color: #e74c3c; color: white; }
        .btn-sabi { background-color: #3498db; color: white; }
        button:hover { transform: scale(1.1); filter: brightness(1.2); }

        .page { display: none; padding: 20px; animation: fadeIn 0.5s; }
        .active { display: block; }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Manbobobo Design */
        .manbobobo {
            width: 120px;
            height: 140px;
            background: black;
            border-radius: 40% 40% 30% 30%;
            margin: 0 auto;
            position: relative;
            border: 2px solid #333;
            animation: bounce 1s infinite alternate;
        }
        .eye {
            width: 30px;
            height: 30px;
            background: black;
            border: 3px solid white;
            border-radius: 50%;
            display: inline-block;
            margin-top: 40px;
        }
        .food-box { font-size: 2rem; margin: 10px; display: inline-block; }

        /* Patrick Design */
        .patrick {
            width: 150px;
            height: 150px;
            background: #ff9999;
            clip-path: polygon(50% 0%, 80% 30%, 100% 70%, 70% 100%, 30% 100%, 0% 70%, 20% 30%);
            margin: 0 auto;
            animation: shake 0.5s infinite;
        }
        
        @keyframes bounce { to { transform: translateY(-20px); } }
        @keyframes shake { 0% { transform: rotate(1deg); } 50% { transform: rotate(-1deg); } 100% { transform: rotate(1deg); } }
    </style>
</head>
<body>

    <h1>🌟 Benvenuti nel Multiverso di Manbobobo 🌟</h1>

    <nav>
        <button class="btn-roblox" onclick="showPage('roblox')">Manbobobo Roblox</button>
        <button class="btn-sabi" onclick="showPage('sabi')">Manbobobo Sabihaozi</button>
    </nav>

    <div id="roblox" class="page">
        <h2>Sezione Roblox</h2>
        <div class="manbobobo">
            <div class="eye"></div>
            <div class="eye"></div>
            <div style="margin-top: 10px;">🐾</div>
        </div>
        <p>Manbobobo sta camminando su due gambe... cosa nasconde?</p>
        <div class="inventory">
            <div class="food-box" title="Scatola di Panini">📦🥪</div>
            <div class="food-box" title="Scatola di Spaghetti">📦🍝</div>
            <div class="food-box" title="Scatola di Panini">📦🥪</div>
        </div>
        <p><i>"Shhh! Non dire a nessuno dei miei panini!"</i></p>
    </div>

    <div id="sabi" class="page">
        <h2>Sezione Sabihaozi</h2>
        <div class="patrick">
            <div style="padding-top: 40px; font-size: 0.8rem;">👁️ 👁️<br>  👅  </div>
        </div>
        <h3 style="color: #ff9999;">PATRICK STAR HA FAME!</h3>
        <p>🍔 🍕 🌭 🍟 🍩</p>
        <p>Patrick sta cercando disperatamente del cibo...</p>
    </div>

    <script>
        function showPage(pageId) {
            // Nascondi tutte le pagine
            const pages = document.querySelectorAll('.page');
            pages.forEach(p => p.classList.remove('active'));
            
            // Mostra quella selezionata
            document.getElementById(pageId).classList.add('active');
        }
    </script>

</body>
</html>
</html>
