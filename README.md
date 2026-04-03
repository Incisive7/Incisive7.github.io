<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Manbobobo AI</title>
    <style>
        body { background: #121212; color: white; font-family: sans-serif; text-align: center; }
        .box { border: 2px solid white; padding: 20px; margin: 20px auto; max-width: 400px; border-radius: 10px; }
        #chat { height: 200px; overflow-y: auto; background: #000; padding: 10px; text-align: left; margin-bottom: 10px; }
        input { width: 70%; padding: 10px; }
        button { padding: 10px; cursor: pointer; }
        .hidden { display: none; }
        .visible { display: block; }
    </style>
</head>
<body>

    <h1>Manbobobo World</h1>

    <nav>
        <button onclick="cambia('roblox')">ROBLOX</button>
        <button onclick="cambia('sabi')">SABIHAOZI</button>
    </nav>

    <div id="roblox" class="visible">
        <h2>Manbobobo Roblox 🐾</h2>
        <p>Sto nascondendo spaghetti e panini... 🍝🥪</p>
        
        <div class="box">
            <div id="chat">
                <p style="color:yellow">Manbobobo: 曼波?</p>
            </div>
            <input type="text" id="domanda" placeholder="Scrivi qui...">
            <button onclick="parla()">Invia</button>
        </div>
    </div>

    <div id="sabi" class="hidden">
        <h2>Manbobobo Sabihaozi ⭐</h2>
        <p>PATRICK STAR HA FAME!! 🍕🍔🍟</p>
    </div>

    <script>
        // Funzione per cambiare sezione
        function cambia(id) {
            document.getElementById('roblox').className = 'hidden';
            document.getElementById('sabi').className = 'hidden';
            document.getElementById(id).className = 'visible';
        }

        // Funzione per la chat
        function parla() {
            var box = document.getElementById('chat');
            var input = document.getElementById('domanda');
            var testo = input.value.trim();

            if(testo === "") return;

            // Aggiungi testo utente
            box.innerHTML += "<div><b>Tu:</b> " + testo + "</div>";

            var risposta = "曼波?";

            // Controllo cinese
            if(testo === "你把我的面包藏哪了") {
                risposta = "嘎嘎嘎嘎嘎嘎不知道嘿嘿";
            } 
            // Controllo spaghetti
            else if(testo.toLowerCase().includes("spaghetti")) {
                risposta = "Manbobobo: Sono nella scatola segreta! 📦";
            }

            // Risposta del gatto
            setTimeout(function() {
                box.innerHTML += "<div style='color:yellow'><b>Manbobobo:</b> " + risposta + "</div>";
                box.scrollTop = box.scrollHeight;
            }, 300);

            input.value = "";
        }
    </script>
</body>
</html>
