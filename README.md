<meta name="viewport" content="width=device-width, initial-scale=1.0" />
    .btn-red {
      background: #ef4444;
      color: white;
    }

    ul {
      padding-left: 20px;
    }

    footer {
      text-align: center;
      margin: 30px 0;
      color: gray;
      font-size: 12px;
    }

    @media (max-width: 600px) {
      .container {
        margin: 15px;
      }

      button {
        width: 100%;
        margin-bottom: 10px;
      }
    }
  </style>
</head>
<body>

<header>
  <h1>INTERGOSPORT</h1>
  <p>Programme de fidélité - Challenge Sport</p>
</header>

<div class="container">
  <h2>Votre cagnotte de points</h2>
  <div class="points" id="points">0 points</div>

  <button class="btn-blue" onclick="addPurchase()">Ajouter un achat</button>
  <button class="btn-red" onclick="resetPoints()">Réinitialiser</button>

  <h3>Récompenses :</h3>
  <ul>
    <li>200 points : -10% sur un achat</li>
    <li>500 points : bon d’achat 20€</li>
    <li>1000 points : cadeau sportif</li>
  </ul>
</div>

<footer>
  © INTERGOSPORT - Programme fidélité
</footer>

<script>
  let points = 0;

  function addPurchase() {
    let euros = prompt("Montant de l'achat (€) :");
    euros = parseInt(euros);
    if (!isNaN(euros)) {
      points += euros;
      updateDisplay();
    }
  }

  function resetPoints() {
    points = 0;
    updateDisplay();
  }

  function updateDisplay() {
    document.getElementById("points").innerText = points + " points";
  }
</script>

</body>
</html>
