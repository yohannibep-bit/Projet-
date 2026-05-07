<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>INTERGOSPORT - Expérience Fidélité</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: linear-gradient(135deg, #0b1220, #1e40af);
      color: white;
    }

    header {
      text-align: center;
      padding: 40px 20px;
      background: rgba(0,0,0,0.4);
    }

    header h1 {
      font-size: 45px;
      color: #22c55e;
      letter-spacing: 3px;
    }

    header p {
      margin-top: 10px;
      font-size: 18px;
      color: #e5e7eb;
    }

    nav {
      display: flex;
      justify-content: center;
      gap: 20px;
      padding: 15px;
      background: rgba(255,255,255,0.05);
      position: sticky;
      top: 0;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }

    nav a:hover {
      color: #22c55e;
    }

    .hero {
      text-align: center;
      padding: 60px 20px;
    }

    .hero h2 {
      font-size: 32px;
      color: #facc15;
      margin-bottom: 10px;
    }

    .hero p {
      max-width: 800px;
      margin: auto;
      color: #e5e7eb;
      font-size: 16px;
      line-height: 1.5;
    }

    .container {
      max-width: 1000px;
      margin: auto;
      padding: 20px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 30px;
    }

    .card {
      background: rgba(255,255,255,0.1);
      padding: 20px;
      border-radius: 15px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    }

    .card h3 {
      margin-bottom: 10px;
      color: #22c55e;
    }

    .points {
      font-size: 40px;
      text-align: center;
      color: #22c55e;
      margin: 20px 0;
      font-weight: bold;
    }

    button {
      padding: 12px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      margin: 5px;
      font-weight: bold;
    }

    .btn-blue { background: #3b82f6; color: white; }
    .btn-green { background: #22c55e; color: black; }
    .btn-red { background: #ef4444; color: white; }

    button:hover { transform: scale(1.05); }

    ul {
      margin-top: 10px;
      padding-left: 20px;
    }

    .section {
      margin-top: 50px;
    }

    .promo {
      background: linear-gradient(90deg, #22c55e, #3b82f6);
      padding: 20px;
      border-radius: 15px;
      text-align: center;
      margin-top: 30px;
    }

    footer {
      text-align: center;
      padding: 30px;
      color: #cbd5e1;
      font-size: 12px;
      margin-top: 40px;
    }

    @media (max-width: 600px) {
      header h1 { font-size: 30px; }
      .hero h2 { font-size: 24px; }
    }
  </style>
</head>
<body>

<header>
  <h1>INTERGOSPORT</h1>
  <p>Le programme fidélité nouvelle génération</p>
</header>

<nav>
  <a href="#accueil">Accueil</a>
  <a href="#points">Points</a>
  <a href="#recompenses">Récompenses</a>
  <a href="#promo">Promotions</a>
</nav>

<section class="hero" id="accueil">
  <h2>🏆 Gagnez, achetez, soyez récompensé !</h2>
  <p>
    INTERGOSPORT vous propose un programme de fidélité simple et puissant.
    Cumulez des points à chaque achat et profitez d’avantages exclusifs en magasin.
  </p>
</section>

<div class="container">

  <div class="section" id="points">
    <div class="card">
      <h3>💳 Votre cagnotte</h3>
      <div class="points" id="pointsDisplay">0</div>

      <div style="text-align:center;">
        <button class="btn-blue" onclick="addPurchase()">Ajouter achat</button>
        <button class="btn-red" onclick="resetPoints()">Reset</button>
      </div>
    </div>
  </div>

  <div class="section" id="recompenses">
    <div class="grid">
      <div class="card">
        <h3>🎁 Récompenses</h3>
        <ul>
          <li>200 pts : -10%</li>
          <li>500 pts : 20€ bon d’achat</li>
          <li>1000 pts : équipement sport</li>
        </ul>
      </div>

      <div class="card">
        <h3>🔥 Bonus</h3>
        <ul>
          <li>Achats produits sportifs = x2 points</li>
          <li>Parrainage = +100 points</li>
          <li>Événements = cadeaux exclusifs</li>
        </ul>
      </div>

      <div class="card">
        <h3>📱 Avantages</h3>
        <ul>
          <li>Offres personnalisées</li>
          <li>Notifications promos</li>
          <li>Accès ventes privées</li>
        </ul>
      </div>
    </div>
  </div>

  <div class="section promo" id="promo">
    <h2>⚡ OFFRE DU MOMENT</h2>
    <p>Doublez vos points sur toute la collection running cette semaine !</p>
  </div>

</div>

<footer>
  © INTERGOSPORT - Site officiel fidélité
</footer>

<script>
  let points = 0;

  function addPurchase() {
    let val = prompt("Montant achat (€):");
    val = parseInt(val);
    if (!isNaN(val)) {
      points += val;
      update();
    }
  }

  function resetPoints() {
    points = 0;
    update();
  }

  function update() {
    document.getElementById("pointsDisplay").innerText = points;
  }
</script>

</body>
</html>
