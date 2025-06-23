<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Benvenuto · Il tuo sito</title>

  <!-- Font Google opzionale -->
  <link rel="preconnect" href="https://fonts.gstatic.com" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet" />

  <style>
    :root {
      --accent: #0066ff;
      --dark: #0c0d11;
      --light: #f7f9fc;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: "Poppins", sans-serif;
      background: var(--dark);
      color: var(--light);
      line-height: 1.6;
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    header,
    footer {
      padding: 1rem 2rem;
      text-align: center;
      background: rgba(255,255,255,0.03);
      backdrop-filter: blur(4px);
    }

    header h1 {
      font-size: 2.5rem;
      font-weight: 600;
      letter-spacing: 0.5px;
      margin-bottom: 0.5rem;
    }

    header p {
      opacity: 0.8;
      max-width: 700px;
      margin: 0 auto;
    }

    .hero {
      flex: 1;
      display: grid;
      place-items: center;
      padding: 4rem 2rem;
      text-align: center;
    }

    .hero-content {
      max-width: 700px;
      animation: fadeInUp 800ms ease-out forwards;
      opacity: 0;
      transform: translateY(30px);
    }

    .hero h2 {
      font-size: clamp(2rem, 5vw, 3.5rem);
      margin-bottom: 0.75rem;
      line-height: 1.2;
    }

    .hero p {
      font-size: 1.125rem;
      margin-bottom: 1.5rem;
      opacity: 0.85;
    }

    .btn-primary {
      display: inline-block;
      padding: 0.75rem 2rem;
      background: var(--accent);
      color: var(--light);
      border-radius: 100vmax;
      font-size: 1rem;
      text-decoration: none;
      transition: transform 0.2s;
    }

    .btn-primary:hover {
      transform: translateY(-2px);
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(30px); }
      to   { opacity: 1; transform: translateY(0);  }
    }
  </style>
</head>

<body>
  <header>
    <h1>Il Tuo Logo</h1>
    <p>Una breve tagline che racconta la tua mission — ispira, informa, coinvolgi.</p>
  </header>

  <section class="hero">
    <div class="hero-content">
      <h2>Benvenuto nel nostro spazio digitale</h2>
      <p>Scopri come trasformiamo le tue idee in realtà: design su misura, sviluppo agile e supporto costante.</p>
      <a href="#inizia" class="btn-primary">Inizia ora</a>
    </div>
  </section>

  <footer>
    © <span id="anno"></span> · Tutti i diritti riservati
  </footer>

  <script>
    // Aggiorna automaticamente l'anno nel footer
    document.getElementById("anno").textContent = new Date().getFullYear();
  </script>
</body>
</html>
