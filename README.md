<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pase Giovanni - Chat AI e Servizi Auto</title>
<style>
body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; margin:0; padding:0; color:#333; background:white; }
header { background:#007bff; color:white; padding:40px 20px; text-align:center; }
header h1 { margin:0; font-size:2.2rem; letter-spacing:2px; }
.container { max-width:1000px; margin:0 auto; padding:40px 20px; }
h2 { color:#007bff; border-bottom:3px solid #e63946; display:inline-block; padding-bottom:5px; }
.service-list { margin-top:20px; list-style:none; padding:0; }
.service-list li { background:#eef2f7; margin:8px 0; padding:12px; border-radius:8px; }
.contact-info { font-weight:bold; color:#e63946; }
.footer { background:#222; color:white; text-align:center; padding:20px; margin-top:40px; }
/* Chat AI */
.chat-container { max-width:500px; margin:30px auto; padding:15px; border:2px solid #007bff; border-radius:10px; background:#f9f9f9; }
.chat-container h3 { text-align:center; color:#007bff; margin-bottom:15px; }
.chat-container input { width:100%; padding:10px; margin-bottom:10px; border:1px solid #ccc; border-radius:5px; }
.chat-container button { width:100%; padding:10px; background:#007bff; color:white; border:none; border-radius:5px; cursor:pointer; }
.chat-container button:hover { background:#0056b3; }
.chat-container p { margin-top:10px; background:#eef2f7; padding:10px; border-radius:5px; min-height:60px; }
</style>
</head>
<body>

<!-- Chat AI -->
<div class="chat-container">
  <h3>Chat con l’AI di Pase Giovanni</h3>
  <input id="input" placeholder="Scrivi la tua domanda...">
  <button id="sendBtn">Invia</button>
  <p id="risposta"></p>
</div>

<header>
  <h1>Pase Giovanni - Officina e Centro Servizi Auto</h1>
  <p>La tua officina di fiducia dal 1949</p>
</header>

<div class="container">
<section>
<h2>Chi Siamo</h2>
<p>La storia della nostra officina inizia con la passione per i motori e l’esperienza di Giovanni Pase. Fondata oltre 70 anni fa, oggi continuiamo l’eredità del fondatore mettendo la soddisfazione dei clienti al primo posto.</p>
</section>

<section>
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
</section>

<section>
<h2>Contatti</h2>
<p class="contact-info">Tel: +39 0438 35562</p>
<p class="contact-info">Email: info@pasegiovanni.it</p>
<p>Indirizzo: Via dei Zoppas, 24, 31015 Conegliano (TV), Italia</p>
<p>Orari: Lun–Ven 08:00–12:00 / 12:00–18:00</p>
</section>
</div>

<footer class="footer">
<p>&copy; Pase Giovanni 2024 · Tutti i diritti riservati</p>
</footer>

<script>
const sendBtn = document.getElementById("sendBtn");
sendBtn.addEventListener("click", async () => {
  const msg = document.getElementById("input").value.trim();
  if(msg === "") return;
  const res = await fetch("https://gklhufvqtufghurhscqo.supabase.co/functions/v1/chat", {
    method:"POST",
    headers:{"Content-Type":"application/json"},
    body: JSON.stringify({message: msg})
  });
  const data = await res.json();
  document.getElementById("risposta").innerText = data.reply;
  document.getElementById("input").value = "";
});
</script>

</body>
</html>
