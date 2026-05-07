<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Pulse Club</title>

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: #000;
      color: white;
    }

    header {
      width: 100%;
      position: fixed;
      top: 0;
      left: 0;
      background: rgba(0,0,0,0.95);
      padding: 20px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
      border-bottom: 1px solid #b7ff00;
    }

    .logo {
      font-size: 2rem;
      font-weight: 800;
      color: #b7ff00;
    }

    .logo span {
      color: white;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 30px;
      font-weight: 500;
      transition: 0.3s;
    }

    nav a:hover {
      color: #b7ff00;
    }

    section {
      padding: 120px 8% 80px;
    }

    .hero {
      min-height: 100vh;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 60px;
      background: linear-gradient(to right, #000000, #111111, #b7ff00);
    }

    .hero-text {
      width: 50%;
    }

    .hero-text h1 {
      font-size: 5rem;
      font-weight: 800;
      line-height: 1.1;
      margin-bottom: 25px;
    }

    .hero-text h1 span {
      color: #b7ff00;
    }

    .hero-text p {
      font-size: 1.3rem;
      color: #ddd;
      margin-bottom: 40px;
      line-height: 1.8;
    }

    .buttons {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }

    .btn {
      padding: 16px 35px;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 700;
      transition: 0.3s;
      display: inline-block;
    }

    .btn-primary {
      background: #b7ff00;
      color: black;
    }

    .btn-primary:hover {
      background: white;
    }

    .btn-secondary {
      border: 2px solid #b7ff00;
      color: #b7ff00;
    }

    .btn-secondary:hover {
      background: #b7ff00;
      color: black;
    }

    .card-points {
      width: 400px;
      background: #111;
      border-radius: 30px;
      padding: 40px;
      border: 2px solid #b7ff00;
      box-shadow: 0 0 40px rgba(183,255,0,0.3);
    }

    .card-points h2 {
      color: #b7ff00;
      margin-bottom: 30px;
      font-size: 2rem;
    }

    .point-box {
      background: #1b1b1b;
      padding: 20px;
      border-radius: 20px;
      margin-bottom: 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .point-box strong {
      font-size: 1.6rem;
    }

    .section-title {
      text-align: center;
      margin-bottom: 60px;
    }

    .section-title h2 {
      font-size: 3.5rem;
      margin-bottom: 20px;
    }

    .section-title span {
      color: #b7ff00;
    }

    .section-title p {
      color: #aaa;
      max-width: 700px;
      margin: auto;
      line-height: 1.8;
      font-size: 1.1rem;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
    }

    .card {
      background: #111;
      border-radius: 25px;
      padding: 40px;
      transition: 0.3s;
      border: 1px solid #222;
    }

    .card:hover {
      transform: translateY(-10px);
      border-color: #b7ff00;
    }

    .card h3 {
      font-size: 2rem;
      margin-bottom: 20px;
      color: #b7ff00;
    }

    .card p,
    .card li {
      color: #ccc;
      line-height: 1.8;
    }

    .levels {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 30px;
    }

    .level {
      border-radius: 30px;
      padding: 45px;
      color: white;
    }

    .bronze {
      background: linear-gradient(to bottom, #b87333, #111);
    }

    .silver {
      background: linear-gradient(to bottom, #9e9e9e, #111);
    }

    .gold {
      background: linear-gradient(to bottom, #ffd700, #111);
    }

    .level h3 {
      font-size: 2.5rem;
      margin-bottom: 30px;
    }

    .level ul {
      list-style: none;
    }

    .level ul li {
      margin-bottom: 15px;
      font-size: 1.1rem;
    }

    .activity-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 30px;
    }

    .activity-card {
      background: #111;
      border-radius: 25px;
      padding: 40px;
    }

    .activity {
      display: flex;
      justify-content: space-between;
      margin-bottom: 25px;
      padding-bottom: 20px;
      border-bottom: 1px solid #222;
      font-size: 1.1rem;
    }

    .bonus {
      background: #b7ff00;
      color: black;
    }

    .bonus h3 {
      color: black;
    }

    .app-section {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
      gap: 50px;
      align-items: center;
    }

    .app-text h2 {
      font-size: 4rem;
      margin-bottom: 30px;
    }

    .app-text h2 span {
      color: #b7ff00;
    }

    .app-text p {
      color: #bbb;
      line-height: 1.8;
      margin-bottom: 40px;
      font-size: 1.1rem;
    }

    .features {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 25px;
    }

    .feature-box {
      background: #111;
      padding: 35px;
      border-radius: 25px;
      text-align: center;
      border: 1px solid #222;
    }

    .feature-box h4 {
      margin: 20px 0;
      color: #b7ff00;
      font-size: 1.5rem;
    }

    footer {
      background: #b7ff00;
      color: black;
      padding: 60px 8%;
    }

    .footer-content {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 30px;
      align-items: center;
    }

    .footer-content h3 {
      font-size: 2.5rem;
      margin-bottom: 10px;
    }

    .socials a {
      display: inline-block;
      margin-left: 15px;
      text-decoration: none;
      color: white;
      background: black;
      padding: 12px 25px;
      border-radius: 40px;
      transition: 0.3s;
    }

    .socials a:hover {
      background: #222;
    }

    @media(max-width: 1000px) {
      .hero {
        flex-direction: column;
        text-align: center;
      }

      .hero-text {
        width: 100%;
      }

      .card-points {
        width: 100%;
      }

      nav {
        display: none;
      }

      .hero-text h1 {
        font-size: 3.5rem;
      }

      .section-title h2,
      .app-text h2 {
        font-size: 2.8rem;
      }
    }
  </style>
</head>
<body>

  <header>
    <div class="logo">PULSE <span>CLUB</span></div>

    <nav>
      <a href="#home">Accueil</a>
      <a href="#services">Services</a>
      <a href="#rewards">Récompenses</a>
      <a href="#activities">Activités</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- HERO -->
  <section class="hero" id="home">
    <div class="hero-text">
      <h1>BOUGEZ PLUS <span>GAGNEZ PLUS</span></h1>

      <p>
        Le programme sportif nouvelle génération.
        Cumulez des points à chaque activité,
        débloquez des récompenses exclusives et rejoignez
        une communauté de passionnés.
      </p>

      <div class="buttons">
        <a href="#" class="btn btn-primary">Rejoindre</a>
        <a href="#services" class="btn btn-secondary">Découvrir</a>
      </div>
    </div>

    <div class="card-points">
      <h2>Vos Récompenses</h2>

      <div class="point-box">
        <span>Points</span>
        <strong>12 450</strong>
      </div>

      <div class="point-box">
        <span>Niveau</span>
        <strong>GOLD</strong>
      </div>

      <div class="point-box">
        <span>Objectif</span>
        <strong>15 000</strong>
      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section id="services">
    <div class="section-title">
      <h2>Comment ça <span>fonctionne</span> ?</h2>

      <p>
        Faites du sport, gagnez des points et profitez de récompenses exclusives.
        Une expérience premium pensée pour tous les sportifs.
      </p>
    </div>

    <div class="cards">
      <div class="card">
        <h3>Achetez</h3>
        <p>
          Achetez des équipements sportifs et cumulez automatiquement des points fidélité.
        </p>
      </div>

      <div class="card">
        <h3>Bougez</h3>
        <p>
          Courez, pédalez, entraînez-vous et transformez vos performances en récompenses.
        </p>
      </div>

      <div class="card">
        <h3>Profitez</h3>
        <p>
          Échangez vos points contre des réductions, événements VIP et cadeaux exclusifs.
        </p>
      </div>
    </div>
  </section>

  <!-- REWARDS -->
  <section id="rewards">
    <div class="section-title">
      <h2>Les niveaux <span>VIP</span></h2>

      <p>
        Plus vous êtes actif, plus vous débloquez des avantages premium.
      </p>
    </div>

    <div class="levels">
      <div class="level bronze">
        <h3>BRONZE</h3>

        <ul>
          <li>✔ Promotions exclusives</li>
          <li>✔ Accès ventes privées</li>
          <li>✔ Cadeau anniversaire</li>
          <li>✔ Réductions sportives</li>
        </ul>
      </div>

      <div class="level silver">
        <h3>SILVER</h3>

        <ul>
          <li>✔ Livraison gratuite</li>
          <li>✔ Coaching personnalisé</li>
          <li>✔ Réductions premium</li>
          <li>✔ Accès anticipé</li>
        </ul>
      </div>

      <div class="level gold">
        <h3>GOLD</h3>

        <ul>
          <li>✔ Invitations VIP</li>
          <li>✔ Produits exclusifs</li>
          <li>✔ Service prioritaire</li>
          <li>✔ Événements privés</li>
        </ul>
      </div>
    </div>
  </section>

  <!-- ACTIVITIES -->
  <section id="activities">
    <div class="section-title">
      <h2>Activités & <span>Points</span></h2>

      <p>
        Chaque activité sportive vous rapporte des récompenses.
      </p>
    </div>

    <div class="activity-grid">
      <div class="activity-card">
        <div class="activity">
          <span>🏃 Running</span>
          <strong>+80 pts</strong>
        </div>

        <div class="activity">
          <span>🚴 Vélo</span>
          <strong>+100 pts</strong>
        </div>

        <div class="activity">
          <span>🏋 Fitness</span>
          <strong>+90 pts</strong>
        </div>

        <div class="activity">
          <span>🏆 Challenge</span>
          <strong>+150 pts</strong>
        </div>
      </div>

      <div class="activity-card bonus">
        <h3>Bonus Écologiques</h3>

        <div class="activity">
          <span>♻ Recycler vos produits</span>
          <strong>+300 pts</strong>
        </div>

        <div class="activity">
          <span>🌱 Achat responsable</span>
          <strong>x2 pts</strong>
        </div>

        <div class="activity">
          <span>🚚 Livraison verte</span>
          <strong>+100 pts</strong>
        </div>
      </div>
    </div>
  </section>

  <!-- APP SECTION -->
  <section>
    <div class="app-section">
      <div class="app-text">
        <h2>Votre passion mérite <span>PLUS</span></h2>

        <p>
          Rejoignez des milliers de sportifs passionnés.
          Suivez vos performances, participez à des défis,
          gagnez des récompenses et profitez d'une expérience unique.
        </p>

        <div class="buttons">
          <a href="#" class="btn btn-primary">Télécharger</a>
          <a href="#" class="btn btn-secondary">Voir les défis</a>
        </div>
      </div>

      <div class="features">
        <div class="feature-box">
          <h4>Communauté</h4>
          <p>Des milliers de sportifs connectés.</p>
        </div>

        <div class="feature-box">
          <h4>Application</h4>
          <p>Suivi des points en temps réel.</p>
        </div>

        <div class="feature-box">
          <h4>Challenges</h4>
          <p>Défis sportifs chaque semaine.</p>
        </div>

        <div class="feature-box">
          <h4>Récompenses</h4>
          <p>Des cadeaux exclusifs toute l'année.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer id="contact">
    <div class="footer-content">
      <div>
        <h3>PULSE CLUB</h3>
        <p>Bien plus qu'un programme sportif.</p>
      </div>

      <div>
        <p><strong>Email :</strong> contact@pulseclub.fr</p>
        <p><strong>Site :</strong> www.pulseclub.fr</p>
      </div>

      <div class="socials">
        <a href="#">Instagram</a>
        <a href="#">TikTok</a>
        <a href="#">YouTube</a>
      </div>
    </div>
  </footer>

</body>
</html>
