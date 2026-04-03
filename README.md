<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pase Giovanni - Centro Servizi Auto</title>
    <style>
        :root {
            --primary-blue: #003366;
            --accent-red: #d32f2f;
            --light-gray: #f4f4f4;
            --dark-text: #333;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--dark-text);
            margin: 0;
            padding: 0;
            background-color: white;
        }

        header {
            background-color: var(--primary-blue);
            color: white;
            padding: 60px 20px;
            text-align: center;
        }

        header h1 {
            margin: 0;
            font-size: 2.5rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        header p {
            font-size: 1.2rem;
            opacity: 0.9;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .section {
            margin-bottom: 40px;
        }

        h2 {
            color: var(--primary-blue);
            border-bottom: 3px solid var(--accent-red);
            display: inline-block;
            padding-bottom: 5px;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .service-card {
            background: var(--light-gray);
            padding: 20px;
            border-radius: 8px;
            border-top: 4px solid var(--primary-blue);
            transition: transform 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }

        .history-box {
            background: #eef2f7;
            padding: 30px;
            border-radius: 15px;
            font-style: italic;
        }

        .footer {
            background: #222;
            color: white;
            text-align: center;
            padding: 30px;
            margin-top: 50px;
        }

        .contact-info {
            font-weight: bold;
            color: var(--accent-red);
        }

        /* Bottone per tornare a Manbobobo */
        .back-btn {
            display: inline-block;
            margin-top: 20px;
            padding: 10px 20px;
            background: var(--accent-red);
            color: white;
            text-decoration: none;
            border-radius: 5px;
        }
    </style>
</head>
<body>

    <header>
        <h1>PASE GIOVANNI</h1>
        <p>Centro Servizi Auto a Conegliano dal 1949</p>
        <a href="index.html" class="back-btn">← Torna al sito principale</a>
    </header>

    <div class="container">
        
        <section class="section">
            <h2>La Nostra Storia</h2>
            <div class="history-box">
                <p>"Fondata nel 1949, l'azienda Pase Giovanni vanta oltre 75 anni di esperienza. Siamo nati quando i pezzi di ricambio si costruivano a mano, e oggi utilizziamo le tecnologie diagnostiche più avanzate per garantire la tua sicurezza."</p>
            </div>
        </section>

        <section class="section">
            <h2>I Nostri Servizi</h2>
            <div class="grid">
                <div class="service-card">
                    <h3>Meccanica & Tagliandi</h3>
                    <p>Manutenzione ordinaria e straordinaria su vetture di ogni marca con protocolli certificati.</p>
                </div>
                <div class="service-card">
                    <h3>Centro Revisioni</h3>
                    <p>Partner ufficiale Dekra per controlli ministeriali rapidi e professionali.</p>
                </div>
                <div class="service-card">
                    <h3>Carrozzeria</h3>
                    <p>Riparazioni strutturali, verniciatura a forno e gestione completa dei sinistri.</p>
                </div>
                <div class="service-card">
                    <h3>Soccorso Stradale</h3>
                    <p>Servizio H24 con mezzi attrezzati per il recupero di veicoli leggeri e pesanti.</p>
                </div>
                <div class="service-card">
                    <h3>Noleggio (Rent)</h3>
                    <p>Soluzioni di noleggio a breve e lungo termine per privati e aziende.</p>
                </div>
                <div class="service-card">
                    <h3>Allestimenti Speciali</h3>
                    <p>Adattamento veicoli per la guida e il trasporto di persone con disabilità.</p>
                </div>
            </div>
        </section>

        <section class="section">
            <h2>Dove Siamo</h2>
            <p>Ci trovi a Conegliano, pronti ad assisterti con la massima trasparenza.</p>
            <p class="contact-info">📍 Via dei Zoppas, 24 – 31015 Conegliano (TV)</p>
            <p>📞 Telefono: 0438 XXXXXX (Inserisci numero reale)</p>
            <p>🌐 Sito ufficiale: <a href="https://www.pasegiovanni.it" target="_blank">www.pasegiovanni.it</a></p>
        </section>

    </div>

    <div class="footer">
        <p>&copy; 2024 Pase Giovanni Centro Servizi Auto | Professionisti del Movimento</p>
    </div>

</body>
</html>
