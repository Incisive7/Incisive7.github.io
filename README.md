<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pase Giovanni - Officina e Servizi Auto</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            margin: 0;
            padding: 0;
            background-color: white;
        }
        header {
            background-color: #007bff;
            color: white;
            padding: 60px 20px;
            text-align: center;
        }
        header h1 {
            margin: 0;
            font-size: 2.5rem;
            letter-spacing: 2px;
        }
        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 40px 20px;
        }
        h2 {
            color: #007bff;
            border-bottom: 3px solid #e63946;
            display: inline-block;
            padding-bottom: 5px;
        }
        .service-list {
            margin-top: 20px;
            list-style-type: none;
            padding: 0;
        }
        .service-list li {
            background: #eef2f7;
            margin: 8px 0;
            padding: 12px;
            border-radius: 8px;
        }
        .contact-info {
            font-weight: bold;
            color: #e63946;
        }
        .footer {
            background: #222;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
        }
        .chat-container {
            max-width: 400px;
            margin: 30px auto;
            padding: 15px;
            border: 1px solid #ccc;
            border-radius: 8px;
            background: #f9f9f9;
        }
        .chat-container input {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .chat-container button {
            width: 100%;
            padding: 10px;
            background: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .chat-container p {
            margin-top: 10px;
            background: #eef2f7;
            padding: 10px;
            border-radius: 5px;
            min-height: 60px;
        }
    </style>
</head>
<body>

<header>
    <h1>Pase Giovanni - Officina e Centro Servizi Auto</h1>
    <p>La tua officina di fiducia dal 1949</p>
</header>

<div class="container">

    <section class="section">
        <h2>Chi Siamo</h2>
        <p>
            La storia della nostra officina inizia con la passione per i motori e l’esperienza di Giovanni Pase.
            Fondata oltre 70 anni fa, oggi l’azienda continua l’eredità del fondatore mettendo la soddisfazione
            dei clienti al primo posto e unendo tradizione e tecnologia moderna. :contentReference[oaicite:2]{index=2}
        </p>
    </section>

    <section class="section">
        <h2>Servizi</h2>
        <ul class="service-list">
            <li>Officina e manutenzione meccanica certificata Pase & Relax</li>
            <li>Revisione auto con controllo elettronico veloce e sicuro</li>
            <li>Carrozzeria completa: raddrizzatura e verniciatura a forno</li>
            <li>Noleggio auto a breve e lungo termine</li>
            <li>Soccorso stradale leggero e pesante</li>
            <li>Servizio gommista e assistenza tecnica</li>
            <li>Pulizia strade e gestione sicurezza su strada</li>
        </ul>
        <p>Questi servizi professionali sono progettati per rispondere a tutte le esigenze di mobilità del cliente. :contentReference[oaicite:3]{index=3}</p>
    </section>

    <section class="section">
        <h2>Informazioni di Contatto</h2>
        <p class="contact-info">Tel: +39 0438 35562</p>
        <p class="contact-info">Email: info@pasegiovanni.it</p>
        <p>Indirizzo: Via dei Zoppas, 24, 31015 Conegliano (TV), Italia</p>
        <p>Orari: Lun–Ven 08:00–12:00 / 12:00–18:00</p> :contentReference[oaicite:4]{index=4}
    </section>

    <section class="section">
        <h2>Chat con l’AI</h2>
        <div class="chat-container">
            <input id="input" placeholder="Scrivi qui la tua domanda...">
            <button onclick="invia()">Invia</button>
            <p id="risposta"></p>
        </div>
    </section>

</div>

<footer class="footer">
    <p>&copy; Pase Giovanni 2024 · Tutti i diritti riservati</p>
</footer>

<script>
async function invia() {
    const msg = document.getElementById("input").value;
    if(msg.trim() === "") return;

    const res = await fetch("https://gklhufvqtufghurhscqo.supabase.co/functions/v1/chat", {
        method: "POST",
        headers: {"Content-Type": "application/json"},
        body: JSON.stringify({message: msg})
    });

    const data = await res.json();
    document.getElementById("risposta").innerText = data.reply;
}
</script>

</body>
</html>
