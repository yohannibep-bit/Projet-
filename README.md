<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>INTERGOSPORT - Programme Fidélité</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: linear-gradient(135deg, #0b1220, #1e3a8a);
      color: white;
    }

    header {
      text-align: center;
      padding: 40px 20px;
      background: rgba(0,0,0,0.4);
    }

    header h1 {
      font-size: 40px;
      color: #22c55e;
      letter-spacing: 2px;
    }

    header p {
      margin-top: 10px;
      font-size: 16px;
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
      padding: 50px 20px;
    }

    .hero h2 {
      font-size: 28px;
      color: #facc15;
      margin-bottom: 10px;
    }

    .hero p {
      max-width: 800px;
      margin: auto;
      font-size: 15px;
      color: #e5e7eb;
      line-height: 1.5;
    }

    .container {
      max-width: 1000px;
      margin: auto;
      padding: 20px;
    }

    .card {
      background: rgba(255,255,255,0.1);
      padding: 20px;
      border-radius: 15px;
      margin-bottom: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    }

    .points {
      font-size: 42px;
      font-weight: bold;
      color: #22c55e;
      text-align: center;
      margin: 15px 0;
    }

    button {
      padding: 12px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      margin: 5px;
      font-weight: bold;
      transition: 0.2s;
    }

    button:hover {
      transform: scale(1.05);
    }

    .btn-blue { background: #3b82f6; color: white; }
    .btn-red { background: #ef4444; color: white; }
    .btn-green { background: #22c55e; color: black; }

    ul {
      margin-top: 10px;
      padding-left: 20px;
    }

    li {
      margin-bottom: 6px;
    }

    .promo {
      background: linear-gradient(90deg, #22c55e, #3b82f6);
      padding: 20px;
      border-radius: 15px;
      text-align: center;
      margin-top: 20px;
    }

    footer {
      text-align: center;
      padding: 30px;
      font-size: 12px;
      color: #cbd5e1;
    }

    @media (max-width: 600px) {
      header h1 { font-size: 28px; }
      .hero h2 { font-size: 22px; }
    }
  </style>
</head>
<body>

<header>
  <h1>INTERGOSPORT</h1>
  <p>Programme de fidélité officiel - Gagnez des récompenses sportives</p>
</header>

<nav>
  <a href="#accueil">Accueil</a>
  <a href="#points">Points</a>
  <a href="#recompenses">Récompenses</a>
  <a href="#promo">Promo</a>
</nav>

<section class="hero" id="accueil">
  <h2>🏆 Achetez, cumulez, gagnez !</h2>
  <p>
    Avec INTERGOSPORT, chaque achat vous rapproche de récompenses exclusives.
    Transformez vos achats en avantages sportifs.
  </p>
</section>

<div class="container">

  <div class="card" id="points">
    <h3>💳 Votre cagnotte</h3>
    <div class="points" id="pointsDisplay">0 points</div>

    <div style="text-align:center;">
      <button class="btn-blue" onclick="addPurchase()">Ajouter achat</button>
      <button class="btn-red" onclick="resetPoints()">Réinitialiser</button>
    </div>
  </div>

  <div class="card" id="recompenses">
    <h3>🎁 Récompenses</h3>
    <ul>
      <li>200 points : -10% sur un achat</li>
      <
