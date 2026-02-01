<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HB IMMERSIVE – Hologrammes 3D AR</title>
  <meta name="description" content="HB IMMERSIVE transforme votre smartphone en projecteur holographique interactif. Manipulez, enregistrez et partagez vos hologrammes 3D en AR.">
  
  <!-- Open Graph pour réseaux sociaux -->
  <meta property="og:title" content="HB IMMERSIVE – Hologrammes 3D AR">
  <meta property="og:description" content="Manipulez des hologrammes 3D sur votre smartphone avec HB IMMERSIVE.">
  <meta property="og:image" content="assets/banner.png">
  <meta property="og:url" content="https://hbimmersive.netlify.app">

  <link rel="stylesheet" href="css/style.css">
  <link rel="icon" href="assets/favicon.ico">
</head>
<body>

<header>
  <div class="container">
    <img src="assets/logo.png" alt="HB IMMERSIVE" class="logo">
    <nav>
      <a href="#hero">Accueil</a>
      <a href="#features">Fonctionnalités</a>
      <a href="#demo">Démonstration</a>
      <a href="#download">Télécharger</a>
      <a href="#contact">Contact</a>
    </nav>
  </div>
</header>

<section id="hero" class="hero">
  <div class="container">
    <h1>HB IMMERSIVE</h1>
    <p>Manipulez des hologrammes 3D avec votre smartphone, en AR, <strong>sans casque ni matériel coûteux</strong>.</p>
    <div class="cta-buttons">
      <a href="https://play.google.com/store/apps/details?id=com.hb.immersive.pro" class="btn-primary">Télécharger</a>
      <a href="#demo" class="btn-secondary">Voir la démo</a>
    </div>
  </div>
</section>

<section id="features" class="features">
  <div class="container">
    <h2>Fonctionnalités Clés</h2>
    <div class="feature-grid">
      <div class="feature-card">
        <img src="assets/icons/ar-icon.png" alt="AR">
        <h3>Réalité Augmentée</h3>
        <p>Manipulez des hologrammes avec vos mains ou via l’écran tactile.</p>
      </div>
      <div class="feature-card">
        <img src="assets/icons/record-icon.png" alt="Vidéo">
        <h3>Enregistrement Vidéo</h3>
        <p>Capturez vos créations en 720p et partagez-les instantanément.</p>
      </div>
      <div class="feature-card">
        <img src="assets/icons/premium-icon.png" alt="Premium">
        <h3>Mode Premium</h3>
        <p>Accédez à des modèles 3D exclusifs et supprimez les publicités.</p>
      </div>
    </div>
  </div>
</section>

<section id="demo" class="demo">
  <div class="container">
    <h2>Démonstration</h2>
    <video controls class="demo-video">
      <source src="assets/videos/demo_fr.mp4" type="video/mp4">
      Votre navigateur ne supporte pas la vidéo HTML5.
    </video>
  </div>
</section>

<section id="download" class="download">
  <div class="container">
    <h2>Téléchargez HB IMMERSIVE</h2>
    <a href="https://play.google.com/store/apps/details?id=com.hb.immersive.pro">
      <img src="assets/google-play-badge.png" alt="Google Play">
    </a>
  </div>
</section>

<section id="contact" class="contact">
  <div class="container">
    <h2>Contactez-nous</h2>
    <form id="contact-form">
      <input type="text" id="name" placeholder="Nom" required>
      <input type="email" id="email" placeholder="Email" required>
      <textarea id="message" placeholder="Message" rows="5" required></textarea>
      <button type="submit">Envoyer</button>
    </form>
  </div>
</section>

<footer>
  <div class="container">
    <p>&copy; 2026 HB IMMERSIVE – Tous droits réservés.</p>
    <div class="social-links">
      <a href="https://twitter.com/HBImmersive">Twitter</a>
      <a href="https://instagram.com/hbimmersive">Instagram</a>
      <a href="https://linkedin.com/company/hbimmersive">LinkedIn</a>
    </div>
  </div>
</footer>

<script src="js/main.js"></script>
</body>
</html>/* Reset */
* { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Roboto', sans-serif; }

/* Layout */
body { background: #0b0f1a; color: #e0e0e0; line-height: 1.6; }
.container { width: 90%; max-width: 1200px; margin: auto; }

/* Header */
header { display: flex; justify-content: space-between; align-items: center; padding: 1rem 0; position: fixed; width: 100%; top: 0; background: rgba(11,15,26,0.95); z-index: 100; }
header nav a { margin-left: 1.5rem; color: #00f0ff; text-decoration: none; transition: 0.3s; }
header nav a:hover { color: #ff00ff; }

/* Hero */
.hero { height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; background: linear-gradient(120deg, #0b0f1a, #1a1f35); position: relative; overflow: hidden; }
.hero h1 { font-size: 3rem; color: #00f0ff; text-shadow: 0 0 20px #00f0ff; animation: glow 2s infinite alternate; }
.hero p { margin: 1rem 0; font-size: 1.2rem; }
.btn-primary { background: #00f0ff; color: #0b0f1a; padding: 0.8rem 1.5rem; margin-right: 1rem; border-radius: 5px; font-weight: bold; text-decoration: none; transition: 0.3s; }
.btn-primary:hover { background: #ff00ff; color: #fff; }
.btn-secondary { border: 2px solid #00f0ff; padding: 0.8rem 1.5rem; border-radius: 5px; color: #00f0ff; text-decoration: none; transition: 0.3s; }
.btn-secondary:hover { border-color: #ff00ff; color: #ff00ff; }

@keyframes glow { from { text-shadow: 0 0 10px #00f0ff; } to { text-shadow: 0 0 30px #ff00ff; } }

/* Features */
.features { padding: 6rem 0 3rem; text-align: center; }
.feature-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 2rem; }
.feature-card { background: rgba(255,255,255,0.05); padding: 2rem; border-radius: 10px; transition: transform 0.3s, background 0.3s; }
.feature-card:hover { transform: translateY(-10px); background: rgba(255,255,255,0.1); }
.feature-card img { width: 60px; margin-bottom: 1rem; }

/* Demo Video */
.demo { text-align: center; padding: 3rem 0; }
.demo-video { width: 90%; max-width: 800px; border-radius: 10px; }

/* Download */
.download { text-align: center; padding: 3rem 0; }
.download img { width: 200px; transition: transform 0.3s; }
.download img:hover { transform: scale(1.05); }

/* Contact */
.contact { text-align: center; padding: 3rem 0; }
.contact input, .contact textarea { width: 90%; max-width: 500px; padding: 0.8rem; margin: 0.5rem 0; border-radius: 5px; border: none; }
.contact button { background: #00f0ff; padding: 0.8rem 2rem; border: none; border-radius: 5px; font-weight: bold; cursor: pointer; transition: 0.3s; }
.contact button:hover { background: #ff00ff; color: #fff; }

/* Footer */
footer { background: #0b0f1a; text-align: center; padding: 2rem 0; }
footer a { color: #00f0ff; margin: 0 0.5rem; text-decoration: none; transition: 0.3s; }
footer a:hover { color: #ff00ff; }// Smooth scroll for navigation
document.querySelectorAll('header nav a').forEach(link => {
  link.addEventListener('click', e => {
    e.preventDefault();
    document.querySelector(link.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
  });
});

// Contact form alert
document.getElementById('contact-form').addEventListener('submit', e => {
  e.preventDefault();
  alert('Merci pour votre message ! Nous vous répondrons rapidement.');
  e.target.reset();
});
