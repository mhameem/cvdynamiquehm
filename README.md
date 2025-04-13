<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CV Hameem Mohammed</title>
  <style>
    @keyframes fadeInUp {
      0% {
        opacity: 0;
        transform: translateY(30px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes rotateTitle {
      0% { transform: rotate(0deg); }
      50% { transform: rotate(2deg); }
      100% { transform: rotate(0deg); }
    }

    @keyframes colorPulse {
      0% { color: #005678; }
      50% { color: #00bcd4; }
      100% { color: #005678; }
    }

    @keyframes bounceIn {
      0% { transform: scale(0.5); opacity: 0; }
      60% { transform: scale(1.2); opacity: 1; }
      100% { transform: scale(1); }
    }

    body {
      font-family: 'Comic Sans MS', cursive, sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(120deg, #f0f8ff, #ffe0f0);
      color: #333;
      overflow-x: hidden;
    }
    .container {
      max-width: 900px;
      margin: 50px auto;
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0,0,0,0.2);
      animation: fadeInUp 1.2s ease forwards;
    }
    h1 {
      font-size: 3em;
      text-align: center;
      animation: rotateTitle 3s infinite ease-in-out, colorPulse 2s infinite;
    }
    h2, h3 {
      color: #005678;
      animation: colorPulse 4s infinite;
    }
    .section {
      margin-bottom: 25px;
      opacity: 0;
      transform: translateX(-50px);
      transition: all 0.8s ease;
      animation: bounceIn 1s ease forwards;
    }
    .section.visible {
      opacity: 1;
      transform: translateX(0);
    }
    .contact p, .about p, .skills p, .languages p {
      margin: 5px 0;
    }
    ul {
      padding-left: 20px;
    }
    .job-title {
      font-weight: bold;
    }
    .job-info {
      font-style: italic;
      color: #666;
    }
    ul li:hover {
      background-color: #fce4ec;
      transition: background 0.3s ease;
      transform: scale(1.02);
    }
  </style>
</head>
<body>
  <div class="container" id="main-container">
    <h1>HAMEEM MOHAMMED</h1>
    <h2 style="text-align:center">Réseaux et Cybersécurité</h2>

    <div class="section contact">
      <h3>Coordonnées</h3>
      <p><strong>Portable :</strong> 06 05 89 43 20</p>
      <p><strong>Email :</strong> Hameem880@gmail.com</p>
      <p><strong>Adresse :</strong> 25 rue Louis Savoie, 95120 Ermont</p>
    </div>

    <div class="section about">
      <h3>À propos</h3>
      <p>Âgé de 21 ans, je suis quelqu'un de très motivé, ponctuel, rigoureux, à l’aise en équipe comme en autonomie, et prêt à m’investir pleinement dans une formation en alternance.</p>
    </div>

    <div class="section education">
      <h3>Parcours scolaire</h3>
      <ul>
        <li><strong>BTS SIO SISR</strong> | IRIS Paris 17e | 2023 - 2025</li>
        <li><strong>BAC STI2D SIN</strong> | Lycée Louis Jouvet, Taverny | 2020 - 2021</li>
      </ul>
    </div>

    <div class="section experience">
      <h3>Expériences professionnelles</h3>
      <ul>
        <li>
          <span class="job-title">Technicien Support Informatique</span>
          <span class="job-info">| UNIFIEDPOST, Nanterre | Août 2023 - Aujourd’hui</span>
          <ul>
            <li>Gestion de tickets et support technique</li>
            <li>Suivi des incidents et des demandes</li>
            <li>Collaboration avec les équipes internes</li>
            <li>Assistance aux utilisateurs</li>
          </ul>
        </li>
        <li>
          <span class="job-title">Assistant Comptable</span>
          <span class="job-info">| FLAT EXPERTISE, Gennevilliers | Fév 2022 - Juil 2023</span>
          <ul>
            <li>Enregistrement et suivi des écritures comptables</li>
            <li>Réalisation des rapprochements bancaires</li>
            <li>Traitement des factures</li>
          </ul>
        </li>
        <li>
          <span class="job-title">Employé Polyvalent</span>
          <span class="job-info">| Burger King, Argenteuil | Avril 2022 - Janv 2023</span>
        </li>
        <li>
          <span class="job-title">Vendeur (Stage)</span>
          <span class="job-info">| Intersport, Herblay | Déc 2017</span>
        </li>
      </ul>
    </div>

    <div class="section skills">
      <h3>Compétences</h3>
      <ul>
        <li><strong>Réseaux :</strong> WAN, LAN, VLAN, TCP/IP, DHCP, Firewall</li>
        <li><strong>Systèmes :</strong> Windows, Linux</li>
        <li><strong>Virtualisation :</strong> VMware</li>
        <li><strong>Outils :</strong> Cisco Packet Tracer, Active Directory, GLPI, Cegid</li>
        <li><strong>Scripting :</strong> PowerShell</li>
        <li><strong>Sécurité :</strong> Notions de pare-feu, gestion des accès utilisateurs</li>
        <li><strong>BDD & Web :</strong> MySQL, HTML/CSS</li>
      </ul>
    </div>

    <div class="section languages">
      <h3>Langues</h3>
      <p>Anglais : B2</p>
      <p>Espagnol : A2</p>
    </div>
  </div>

  <script>
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    }, {
      threshold: 0.1
    });

    document.querySelectorAll('.section').forEach(section => {
      observer.observe(section);
    });
  </script>
</body>
</html>
