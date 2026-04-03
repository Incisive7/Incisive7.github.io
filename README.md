<div id="chat-container" style="background: #000; border: 2px solid white; padding: 10px; margin-top: 20px;">
    <div id="chat-box" style="height: 100px; overflow-y: auto; color: #0f0; font-family: monospace;">
        Manbobobo: Ciao! Vuoi sapere dove nascondo gli spaghetti?
    </div>
    <input type="text" id="user-input" placeholder="Chiedi a Manbobobo..." style="width: 70%;">
    <button onclick="askManbobobo()">Invia</button>
</div>

<script>
function askManbobobo() {
    const input = document.getElementById('user-input').value.toLowerCase();
    const chatBox = document.getElementById('chat-box');
    let risposta = "Miao? (Manbobobo ti guarda confuso)";

    if(input.includes("spaghetti")) {
        risposta = "Manbobobo: Non li troverai mai! Sono nella mia pancia cicciotta!";
    } else if(input.includes("ciao")) {
        risposta = "Manbobobo: Ciao umano! Hai portato dei panini?";
    } else if(input.includes("roblox")) {
        risposta = "Manbobobo: Oof! Sto camminando su due gambe nel metaverso!";
    }

    chatBox.innerHTML += "<div>Tu: " + input + "</div>";
    chatBox.innerHTML += "<div>" + risposta + "</div>";
    document.getElementById('user-input').value = ""; // Pulisce l'input
}
</script>
</html>
</html>
