HBIMMERSIVE-PORTFOLIO/
├── index.html          # Page d'accueil complète
├── docs/
│   ├── ARCHITECTURE.md
│   ├── FEATURES.md
│   └── MARKETING.md
├── screenshots/
│   ├── fr/
│   │   ├── home.jpg
│   │   ├── ar_mode.jpg
│   │   ├── premium.jpg
│   │   └── share.jpg
│   └── en/
│       ├── home.jpg
│       ├── ar_mode.jpg
│       ├── premium.jpg
│       └── share.jpg
├── assets/
│   ├── logo.png
│   └── favicon.ico
└── videos/
    └── demo_fr.mp4<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HB IMMERSIVE – Hologrammes 3D en Réalité Augmentée</title>
    <meta name="description" content="Transformez votre smartphone en projecteur holographique avec HB IMMERSIVE. Découvrez notre portfolio complet et téléchargez l'application.">
    <meta property="og:title" content="HB IMMERSIVE – Portfolio Officiel">
    <meta property="og:description" content="Application de réalité augmentée pour créer et partager des hologrammes 3D.">
    <meta property="og:image" content="assets/logo.png">
    <meta property="og:url" content="https://hbimmersive.netlify.app">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link rel="icon" href="assets/favicon.ico">
    <style>
        /* Reset et variables */
        :root {
            --primary: #6a4c93;
            --secondary: #8e44ad;
            --dark: #2c3e50;
            --light: #ecf0f1;
            --accent: #3498db;
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
        }
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px 0;
        }
        /* Header */
        header {
            background-color: var(--dark);
            color: var(--light);
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .logo {
            height: 50px;
        }
        nav a {
            color: var(--light);
            text-decoration: none;
            margin-left: 20px;
            font-weight: 500;
            transition: color 0.3s;
        }
        nav a:hover {
            color: var(--accent);
        }
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: var(--light);
            text-align: center;
            padding: 150px 0 100px;
            margin-top: 80px;
        }
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 30px;
        }
        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        .btn {
            padding: 12px 25px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        .btn-primary {
            background-color: var(--accent);
            color: white;
        }
        .btn-secondary {
            background-color: transparent;
            color: var(--light);
            border: 2px solid var(--light);
        }
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        /* Features Section */
        .features {
            padding: 80px 0;
            background-color: white;
        }
        .features h2 {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2rem;
            color: var(--dark);
        }
        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        .feature-card {
            background-color: var(--light);
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        .feature-card:hover {
            transform: translateY(-10px);
        }
        .feature-card img {
            width: 100%;
            max-width: 200px;
            height: auto;
            margin-bottom: 20px;
            border-radius: 5px;
        }
        .feature-card h3 {
            margin-bottom: 15px;
            color: var(--primary);
        }
        /* Screenshots Section */
        .screenshots {
            padding: 80px 0;
            background-color: #f9f9f9;
        }
        .screenshots h2 {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2rem;
            color: var(--dark);
        }
        .screenshot-table {
            width: 100%;
            margin: 0 auto;
            text-align: center;
        }
        .screenshot-table img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 10px;
        }
        /* Video Section */
        .video-section {
            padding: 80px 0;
            background-color: white;
            text-align: center;
        }
        .video-section h2 {
            margin-bottom: 30px;
            font-size: 2rem;
            color: var(--dark);
        }
        .video-container {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        /* Contact Section */
        .contact {
            padding: 80px 0;
            background-color: var(--dark);
            color: var(--light);
            text-align: center;
        }
        .contact h2 {
            margin-bottom: 30px;
            font-size: 2rem;
        }
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        .social-links a {
            color: var(--light);
            font-size: 1.5rem;
            transition: color 0.3s;
        }
        .social-links a:hover {
            color: var(--accent);
        }
        /* Footer */
        footer {
            background-color: var(--primary);
            color: var(--light);
            text-align: center;
            padding: 20px 0;
        }
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            .hero p {
                font-size: 1rem;
            }
            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }
            .feature-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <img src="assets/logo.png" alt="HB IMMERSIVE Logo" class="logo">
                <div>
                    <a href="#features">Fonctionnalités</a>
                    <a href="#screenshots">Captures</a>
                    <a href="#video">Démonstration</a>
                    <a href="#contact">Contact</a>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>HB IMMERSIVE – Hologrammes 3D en Réalité Augmentée</h1>
            <p>Transformez votre smartphone en projecteur holographique interactif. Créez, manipulez et partagez des objets 3D en réalité augmentée, sans matériel coûteux.</p>
            <div class="cta-buttons">
                <a href="https://play.google.com/store/apps/details?id=com.hb.immersive.pro" class="btn btn-primary">Télécharger sur Google Play</a>
                <a href="#video" class="btn btn-secondary">Voir la démo</a>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
        <div class="container">
            <h2>Fonctionnalités Clés</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <img src="screenshots/fr/ar_mode.jpg" alt="Mode AR">
                    <h3>Réalité Augmentée Interactive</h3>
                    <p>Manipulez des hologrammes avec vos mains ou via l’écran tactile.</p>
                </div>
                <div class="feature-card">
                    <img src="screenshots/fr/share.jpg" alt="Partage">
                    <h3>Enregistrement et Partage</h3>
                    <p>Capturez vos créations en 720p et partagez-les sur les réseaux sociaux.</p>
                </div>
                <div class="feature-card">
                    <img src="screenshots/fr/premium.jpg" alt="Premium">
                    <h3>Mode Premium</h3>
                    <p>Accédez à des modèles 3D exclusifs et supprimez les publicités.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Screenshots Section -->
    <section id="screenshots" class="screenshots">
        <div class="container">
            <h2>Captures d'Écran</h2>
            <h3>Version Française</h3>
            <table class="screenshot-table">
                <tr>
                    <td><img src="screenshots/fr/home.jpg" alt="Accueil" width="250"></td>
                    <td><img src="screenshots/fr/ar_mode.jpg" alt="Mode AR" width="250"></td>
                    <td><img src="screenshots/fr/premium.jpg" alt="Premium" width="250"></td>
                    <td><img src="screenshots/fr/share.jpg" alt="Partager" width="250"></td>
                </tr>
                <tr>
                    <td>Accueil</td>
                    <td>Mode AR</td>
                    <td>Premium</td>
                    <td>Partager</td>
                </tr>
            </table>
            <h3 style="margin-top: 50px;">Version Anglaise</h3>
            <table class="screenshot-table">
                <tr>
                    <td><img src="screenshots/en/home.jpg" alt="Home" width="250"></td>
                    <td><img src="screenshots/en/ar_mode.jpg" alt="AR Mode" width="250"></td>
                    <td><img src="screenshots/en/premium.jpg" alt="Premium" width="250"></td>
                    <td><img src="screenshots/en/share.jpg" alt="Share" width="250"></td>
                </tr>
                <tr>
                    <td>Home</td>
                    <td>AR Mode</td>
                    <td>Premium</td>
                    <td>Share</td>
                </tr>
            </table>
        </div>
    </section>

    <!-- Video Section -->
    <section id="video" class="video-section">
        <div class="container">
            <h2>Démonstration Vidéo</h2>
            <div class="video-container">
                <!-- Remplace l'URL par celle de ta vidéo YouTube -->
                <iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" allowfullscreen></iframe>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2>Contactez-nous</h2>
            <p>Pour toute question, partenariat ou support, n'hésitez pas à nous contacter.</p>
            <div class="social-links">
                <a href="mailto:heritier.baguma@hbimmersive.com" title="Email"><i class="fas fa-envelope"></i></a>
                <a href="https://twitter.com/HBImmersive" title="Twitter"><i class="fab fa-twitter"></i></a>
                <a href="https://instagram.com/hbimmersive" title="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="https://linkedin.com/company/hbimmersive" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2026 HB IMMERSIVE. Tous droits réservés.</p>
        </div>
    </footer>
</body>
</html>
