<script>
function askManbobobo() {
    const inputField = document.getElementById('user-input');
    const input = inputField.value.trim();
    const chatBox = document.getElementById('chat-box');

    if (input === "") return;

    // Mostra la tua domanda nella chat
    chatBox.innerHTML += `<p style="margin: 5px 0;"><strong>Tu:</strong> ${input}</p>`;

    let risposta = "";

    // LOGICA DI MANBOBOBO
    // 1. La domanda specifica sul pane
    if (input === "你把我的面包藏哪了") {
        risposta = "嘎嘎嘎嘎嘎嘎不知道嘿嘿";
    } 
    // 2. Reazione agli spaghetti o panini
    else if (input.toLowerCase().includes("spaghetti") || input.toLowerCase().includes("panini") || input.toLowerCase().includes("pasta")) {
        risposta = "Manbobobo: *Gnam gnam*... Erano squisiti! Ne vuoi un po'? No, scherzavo, sono tutti miei!";
    }
    // 3. Reazione a Roblox
    else if (input.toLowerCase().includes("roblox")) {
        risposta = "Manbobobo: Sto cercando di glitchare nel sistema per avere spaghetti infiniti!";
    }
    // 4. RISPOSTA DI DEFAULT (Se non capisce o non sa rispondere)
    else {
        risposta = "曼波?";
    }

    // Effetto "caricamento" della risposta
    setTimeout(() => {
        chatBox.innerHTML += `<p style="color: #f1c40f; margin: 5px 0;"><strong>Manbobobo:</strong> ${risposta}</p>`;
        
        // Scroll automatico verso il basso per vedere l'ultima risposta
        chatBox.scrollTop = chatBox.scrollHeight;
    }, 400);

    // Pulisce il campo di testo
    inputField.value = "";
}

// Funzione per inviare con il tasto Invio
document.getElementById("user-input").addEventListener("keypress", function(event) {
    if (event.key === "Enter") {
        askManbobobo();
    }
});
</script>
}
</script>
</html>
</html>
