<!-- Inizio Chatbot -->
<div style="max-width:400px;margin:20px auto;padding:15px;border:1px solid #ccc;border-radius:8px;background:#f9f9f9;">
  <h3 style="text-align:center;color:#007bff;">Chat con noi</h3>
  <input id="input" placeholder="Scrivi la tua domanda..." 
         style="width:100%;padding:10px;margin-bottom:10px;border:1px solid #ccc;border-radius:5px;">
  <button onclick="invia()" 
          style="width:100%;padding:10px;background:#007bff;color:white;border:none;border-radius:5px;cursor:pointer;">
    Invia
  </button>
  <p id="risposta" style="margin-top:10px;background:#eef2f7;padding:10px;border-radius:5px;min-height:50px;"></p>
</div>

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
<!-- Fine Chatbot -->
