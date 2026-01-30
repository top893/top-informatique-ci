<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TOP INFORMATIQUE - Votre boutique tech</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f5f5f5;
            color: #333;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #ff6b00, #ff3d00);
            color: white;
            padding: 15px 20px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            font-size: 28px;
            font-weight: bold;
            display: flex;
            align-items: center;
        }

        .logo span {
            color: #003366;
            background: white;
            padding: 5px 10px;
            border-radius: 5px;
            margin-left: 8px;
        }

        .search-bar {
            flex-grow: 1;
            max-width: 600px;
            margin: 0 20px;
        }

        .search-bar input {
            width: 100%;
            padding: 12px 20px;
            border: none;
            border-radius: 30px;
            font-size: 16px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        .user-actions a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 5px;
        }

        /* Navigation */
        nav {
            background-color: #003366;
            padding: 10px 0;
        }

        .nav-links {
            display: flex;
            justify-content: center;
            list-style: none;
            flex-wrap: wrap;
        }

        .nav-links li {
            margin: 0 15px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 8px 15px;
            border-radius: 4px;
            transition: background 0.3s;
        }

        .nav-links a:hover {
            background: rgba(255,255,255,0.2);
        }

        /* Banner */
        .banner {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), url('https://images.unsplash.com/photo-1518709268805-4e9042af2176?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 80px 20px;
            margin-bottom: 30px;
        }

        .banner h1 {
            font-size: 3rem;
            margin-bottom: 15px;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
        }

        .banner p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 25px;
        }

        .cta-button {
            display: inline-block;
            background: #ff6b00;
            color: white;
            padding: 15px 40px;
            text-decoration: none;
            font-weight: bold;
            border-radius: 30px;
            font-size: 1.1rem;
            transition: transform 0.3s, background 0.3s;
        }

        .cta-button:hover {
            background: #ff3d00;
            transform: scale(1.05);
        }

        /* Products Section */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-title {
            font-size: 2rem;
            margin: 40px 0 20px;
            color: #003366;
            border-left: 5px solid #ff6b00;
            padding-left: 15px;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 50px;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }

        .product-image {
            height: 200px;
            background-color: #f0f0f0;
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            position: relative;
        }

        .image-placeholder {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100%;
            font-size: 40px;
            color: #003366;
            background: linear-gradient(135deg, #f0f0f0, #e0e0e0);
        }

        .product-info {
            padding: 20px;
        }

        .product-brand {
            color: #ff6b00;
            font-weight: bold;
            font-size: 0.9rem;
            text-transform: uppercase;
            margin-bottom: 5px;
        }

        .product-name {
            font-weight: bold;
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: #003366;
        }

        .product-description {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 15px;
            line-height: 1.4;
        }

        .product-price {
            font-weight: bold;
            font-size: 1.4rem;
            color: #003366;
            margin-bottom: 15px;
        }

        .whatsapp-btn {
            width: 100%;
            padding: 12px;
            background: linear-gradient(135deg, #25D366, #128C7E);
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            transition: all 0.3s;
        }

        .whatsapp-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(37, 211, 102, 0.3);
        }

        /* Marques Section */
        .marques-section {
            background: white;
            padding: 30px;
            border-radius: 10px;
            margin-bottom: 40px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .marques-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
            justify-content: center;
        }

        .marque-btn {
            padding: 10px 20px;
            background: #f0f0f0;
            border: none;
            border-radius: 20px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }

        .marque-btn:hover {
            background: #003366;
            color: white;
            transform: translateY(-2px);
        }

        .marque-btn.active {
            background: #ff6b00;
            color: white;
        }

        /* Filtres */
        .filters {
            display: flex;
            gap: 15px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .filter-btn {
            padding: 10px 20px;
            background: white;
            border: 2px solid #003366;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s;
        }

        .filter-btn:hover {
            background: #003366;
            color: white;
        }

        .filter-btn.active {
            background: #003366;
            color: white;
        }

        /* Footer */
        footer {
            background: #003366;
            color: white;
            padding: 40px 20px;
            margin-top: 60px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-section h3 {
            color: #ff6b00;
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 10px;
        }

        .footer-section a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-section a:hover {
            color: #ff6b00;
        }

        .copyright {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #aaa;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-top {
                flex-direction: column;
                text-align: center;
            }
            .search-bar {
                margin: 15px 0;
                width: 100%;
            }
            .banner h1 {
                font-size: 2.2rem;
            }
            .nav-links {
                justify-content: flex-start;
                overflow-x: auto;
                padding-bottom: 10px;
            }
            .user-actions {
                margin-top: 10px;
            }
            .filters {
                overflow-x: auto;
                padding-bottom: 10px;
            }
            .filter-btn {
                flex-shrink: 0;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-top">
            <div class="logo">
                TOP <span>INFORMATIQUE</span>
            </div>
            <div class="search-bar">
                <input type="text" id="searchInput" placeholder="🔍 Rechercher un produit, une marque...">
            </div>
           
        </div>
    </header>

   

    <!-- Banner -->
    <section class="banner">
        <h1>Bienvenue sur notre boutique en ligne</h1>
        <p>Découvrez nos produits TP-Link, HP, Dell, Lenovo, Canon, Epson et toutes les grandes marques au meilleur prix</p>
        <a href="#products" class="cta-button">Voir les offres</a>
    </section>

    <!-- Products -->
    <div class="container">
        <!-- Filtres par catégorie -->
        <div class="filters">
            <button class="filter-btn active" data-category="">Tous les produits</button>
            <button class="filter-btn" data-category="Ordinateurs Portables">Ordinateurs Portables</button>
            <button class="filter-btn" data-category="Ordinateurs de Bureau">Ordinateurs Bureau</button>
            <button class="filter-btn" data-category="Imprimantes">Imprimantes</button>
            <button class="filter-btn" data-category="Écrans">Écrans</button>
            <button class="filter-btn" data-category="Serveurs">Serveurs</button>
            <button class="filter-btn" data-category="Switchs">Switchs</button>
            <button class="filter-btn" data-category="Scanners">Scanners</button>
            <button class="filter-btn" data-category="Projecteurs">Projecteurs</button>
            <button class="filter-btn" data-category="Routeurs">Routeurs</button>
            <button class="filter-btn" data-category="Point d'accés">Point d'accés</button>
            <button class="filter-btn" data-category="Contrôleur WiFi">Contrôleur WiFi</button>
            <button class="filter-btn" data-category="Téléphonie IP">Téléphonie IP</button>
            <button class="filter-btn" data-category="Autocom">Autocom</button>
            <button class="filter-btn" data-category="Consommables">Consommables</button>
            <button class="filter-btn" data-category="Accessoires Informatique">Accessoires</button>
        </div>

        <h2 class="section-title" id="products">NOS PRODUITS</h2>
        <div class="products-grid" id="productsGrid">
            <!-- Les produits seront ajoutés dynamiquement -->
        </div>

        <!-- Marques -->
        <div class="marques-section">
            <h2 class="section-title">FILTRER PAR MARQUE</h2>
            <div class="marques-grid" id="marquesGrid">
                <!-- Les boutons de marque seront ajoutés dynamiquement -->
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-section">
                <h3>TOP INFORMATIQUE</h3>
                <p>Votre partenaire technologique de confiance. Produits neufs garantis, livraison rapide, support technique.</p>
            </div>
            <div class="footer-section">
                <h3>Contact WhatsApp</h3>
                 <div class="user-actions">
                <a href="https://wa.me/2250160435955" target="_blank">
                    <i class="fab fa-whatsapp"></i> WhatsApp
                </a>
            </div>
            
            </div>
            <div class="footer-section">
                <h3>Horaires</h3>
                <p>Lun-Sam: 8h-18h</p>
                <p>Dimanche: Fermé</p>
            </div>
        </div>
        
    </footer>

    <script>
        // DONNÉES DES PRODUITS
        const produits = [
            {
                id: 68,
                nom: "Yealink T31P",
                description: "Téléphone IP Yealink T31P, écran LCD 2.4\", PoE, supporte 3 lignes SIP, audio HD",
                prix: 30000,
                categorie: "Téléphonie IP",
                marque: "Yealink",
                modele: "T31P",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.PUJcTAwwrJt1Tanefj-ZEAHaEK?w=284&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 64,
                nom: "TP-Link Amoda EAP110-Outdoor",
                description: "Point d'accès WiFi extérieur TP-Link EAP110-Outdoor, IP65, 300 Mbps, PoE",
                prix: 30000,
                categorie: "Point d'accés",
                marque: "TP-Link",
                modele: "EAP110-Outdoor",
                etat: "Neuf",
                image: "https://static.tp-link.com/upload/image-line/EAP225-Outdoor_normal_20230821084232j.png"
            },
            {
                id: 65,
                nom: "TP-Link Amoda Hardware Controller OC220",
                description: "Contrôleur WiFi matériel TP-Link OC220, gestion centralisée des points d'accès",
                prix: 55000,
                categorie: "Contrôleur WiFi",
                marque: "TP-Link",
                modele: "OC220",
                etat: "Neuf",
                image: "https://static.tp-link.com/upload/image-line/OC200_overview_01_normal_20250126022212n.jpg"
            },
            {
                id: 66,
                nom: "TP-Link Deco AX1500",
                description: "Système WiFi Mesh TP-Link Deco AX1500, couverture jusqu'à 130 m², 3 unités",
                prix: 80000,
                categorie: "Point d'accés",
                marque: "TP-Link",
                modele: "Deco AX1500",
                etat: "Neuf",
                image: "https://needy.shop/cdn/shop/files/61_ab0ec889-2459-4a84-87b4-70c2a63f70c9_700x700.jpg?v=1716881745"
            },
            {
                id: 67,
                nom: "Toplink TL-POS80W",
                description: "Imprimante de caisse thermique Toplink TL-POS80W, 80mm, USB/Ethernet, impression rapide",
                prix: 55000,
                categorie: "Imprimantes",
                marque: "Toplink",
                modele: "TL-POS80W",
                etat: "Neuf",
                image: "https://ci.jumia.is/unsafe/fit-in/500x500/filters:fill(white)/product/12/758662/1.jpg?7659"
            },
            {
                id: 59,
                nom: "Grandstream GXP1625",
                description: "Téléphone IP Grandstream GXP1625, 2 lignes SIP, écran LCD, PoE, HD audio",
                prix: 30000,
                categorie: "Téléphonie IP",
                marque: "Grandstream",
                modele: "GXP1625",
                etat: "Neuf",
                image: "https://www.grandstream.com/hubfs/Product%20Images/GXP/gxp1620_25_front_web.png"
            },
            {
                id: 60,
                nom: "Fanvil X303P",
                description: "Téléphone IP Fanvil X303P, 2 lignes SIP, écran LCD, PoE, HD audio",
                prix: 30000,
                categorie: "Téléphonie IP",
                marque: "Fanvil",
                modele: "X303P",
                etat: "Neuf",
                image: "https://cdn.store-assets.com/s/337542/i/70618265.png"
            },
            {
                id: 61,
                nom: "Yeastar S20",
                description: "Autocom Yeastar S20, 20 utilisateurs, 8 lignes simultanées, Gateway FXS/FXO",
                prix: 180000,
                categorie: "Autocom",
                marque: "Yeastar",
                modele: "S20",
                etat: "Neuf",
                image:"https://www.icttech.net/images/thumbs/0001325_yeastar-s20-voip-pbx-20-user-10-voip-open-box.png"
            },
            {
                id: 62,
                nom: "Grandstream UCM6302",
                description: "Autocom Grandstream UCM6302, 50 utilisateurs, 4 ports FXS, intégration VoIP avancée",
                prix: 250000,
                categorie: "Autocom",
                marque: "Grandstream",
                modele: "UCM6302",
                etat: "Neuf",
                image: "https://1genieur.ci/551-large_default/grandstream-ucm6302a.jpg"
            },
            {
                id: 63,
                nom: "Toner HP 207A",
                description: "Toner HP 207A Noir, compatible imprimantes LaserJet Pro MFP M282-M282",
                prix: 47000,
                categorie: "Consommables",
                marque: "HP",
                modele: "207A",
                etat: "Neuf",
                image: "https://digistar.ma/wp-content/webp-express/webp-images/uploads/2023/08/HP-207A-Noir-W2210A-Toner-HP-LaserJet-dorigine-1.jpg.webp"
            },
            {
                id: 1,
                nom: "Canon PIXMA G3410 - Imprimante Multifonction",
                description: "Imprimante multifonction réservoir d'encre, impression/scanner/copie, Wi-Fi, résolution 4800x1200 dpi",
                prix: 80000,
                categorie: "Imprimantes",
                marque: "Canon",
                modele: "PIXMA G3410",
                etat: "Neuf",
                image: "https://cdn.idealo.com/folder/Product/202783/8/202783887/s4_produktbild_gross_2/canon-pixma-g3410.jpg"
            },
            {
                id: 2,
                nom: "Lenovo Laptop Ultra 7-155H 8GB 512GB SSD",
                description: "Portable Lenovo ThinkBook 14 G7, processeur Ultra 7-155H, 8GB RAM, 512GB SSD",
                prix: 480000,
                categorie: "Ordinateurs Portables",
                marque: "Lenovo",
                modele: "ThinkBook 14 G7",
                etat: "Neuf",
                image: "https://media.rueducommerce.fr/r1200/ld/products/00/06/07/70/LD0006077061_0006143814_0006145415.jpg"
            },
            {
                id: 3,
                nom: "Lenovo Laptop i5-13420H 8GB 512GB SSD",
                description: "Portable Lenovo ThinkPad E16 G1, processeur i5-13420H, 8GB RAM, 512GB SSD",
                prix: 430000,
                categorie: "Ordinateurs Portables",
                marque: "Lenovo",
                modele: "ThinkPad E16 G1",
                etat: "Neuf",
                image: "https://www.voomstore.ci/65237-large_default/portable-lenovo-thinkpad-e16-g1-i5-1335u-8g-512gb-ssd-nos-2y-cci-20w1s55500.jpg"
            },
            {
                id: 4,
                nom: "HP Laptop i7-1355U 8GB 512GB SSD",
                description: "Portable HP 15, processeur i7-1355U, 8GB RAM, 512GB SSD, écran 15.6\" Full HD",
                prix: 370000,
                categorie: "Ordinateurs Portables",
                marque: "HP",
                modele: "15fd0229nia",
                etat: "Neuf",
                image: "https://puresolutions.ma/wp-content/uploads/2024/01/Nouveau-projet-2024-01-30T161809.321-510x510.webp"
            },
            {
                id: 5,
                nom: "Acer Projector 4800LM – X1329WHP",
                description: "Projecteur Acer X1329WHP, 4800 lumens, résolution WXGA, compatible Full HD",
                prix: 230000,
                categorie: "Projecteurs",
                marque: "Acer",
                modele: "X1329WHP",
                etat: "Neuf",
                image: "https://www.bigbaazaaru.mv/wp-content/uploads/2024/07/IkKTyMBb1658825526-480x380.png"
            },
            {
                id: 6,
                nom: "Zebra Desktop Label Printer ZD621T",
                description: "Imprimante d'étiquettes de bureau Zebra ZD621T, impression thermique transfert",
                prix: 280000,
                categorie: "Imprimantes",
                marque: "Zebra",
                modele: "ZD621T",
                etat: "Neuf",
                image: "https://www.printerbase.co.uk/media/catalog/product/cache/da0d4b41a2735aaf1e00b4dd4990980e/z/e/zebra-zd420a_2_1_9_3.jpg"
            },
            {
                id: 7,
                nom: "Canon Image RUNNER Copier 3326i",
                description: "Copieur multifonction Canon ImageRUNNER 3326i, impression/copie/numérisation",
                prix: 1900000,
                categorie: "Imprimantes",
                marque: "Canon",
                modele: "imageRUNNER 3326i",
                etat: "Neuf",
                image: "https://www.tic.ci/storage/ca2.jpg"
            },
            {
                id: 8,
                nom: "HP Scanner Pro 3600 F1",
                description: "Scanner professionnel HP Pro 3600 F1, numérisation recto-verso automatique",
                prix: 230000,
                categorie: "Scanners",
                marque: "HP",
                modele: "Pro 3600 F1",
                etat: "Neuf",
                image: "https://hp.widen.net/content/udktz8twhi/png/udktz8twhi.png?w=800&h=600&dpi=72&color=ffffff00"
            },
            {
                id: 9,
                nom: "HP Scanner Pro N4600 Fnw1",
                description: "Scanner réseau HP Pro N4600 Fnw1, haute vitesse, alimentation automatique",
                prix: 390000,
                categorie: "Scanners",
                marque: "HP",
                modele: "Pro N4600 Fnw1",
                etat: "Neuf",
                image: "https://hp.widen.net/content/ndzhonakz8/png/ndzhonakz8.png?w=800&h=600&dpi=72&color=ffffff00"
            },
            {
                id: 10,
                nom: "HP Scanner Pro 2600 F1",
                description: "Scanner professionnel HP Pro 2600 F1, compact, recto-verso automatique",
                prix: 150000,
                categorie: "Scanners",
                marque: "HP",
                modele: "Pro 2600 F1",
                etat: "Neuf",
                image: "https://hp.widen.net/content/zijsar8amq/png/zijsar8amq.png?w=800&h=600&dpi=72&color=ffffff00"
            },
            {
                id: 11,
                nom: "Epson Scanner Workforce DS-1630",
                description: "Scanner de documents Epson WorkForce DS-1630, alimentation automatique",
                prix: 135000,
                categorie: "Scanners",
                marque: "Epson",
                modele: "WorkForce DS-1630",
                etat: "Neuf",
                image: "https://www.tic.ci/storage/sc1-3.jpg"
            },
            {
                id: 12,
                nom: "Epson Scanner DS530",
                description: "Scanner compact Epson DS530, portable, alimentation automatique",
                prix: 50000,
                categorie: "Scanners",
                marque: "Epson",
                modele: "DS530",
                etat: "Neuf",
                image: "https://www.ntc-tech.com/cdn/shop/products/vZtU2UWFg8TKgGv79xPe0oqNZpuqljSEdwgwrud5i3SY8pglihidv6s6wMMe4KIFJsQhPd3ODEPN03Xiv_8ffhgC1pQL6rs_s4470.jpg?v=1707849215&width=1445"
            },
            {
                id: 13,
                nom: "Epson Scanner Workforce DS870",
                description: "Scanner haut de gamme Epson Workforce DS870, vitesse élevée",
                prix: 280000,
                categorie: "Scanners",
                marque: "Epson",
                modele: "Workforce DS870",
                etat: "Neuf",
                image: "https://www.startech.com.bd/image/cache/catalog/scanner/epson/ds-870/ds-870-01-500x500.webp"
            },
            {
                id: 14,
                nom: "Epson Scanner Perfection V39II",
                description: "Scanner à plat Epson Perfection V39II, haute résolution 4800 dpi",
                prix: 60000,
                categorie: "Scanners",
                marque: "Epson",
                modele: "Perfection V39II",
                etat: "Neuf",
                image: "https://mediaserver.goepson.com/ImConvServlet/imconv/ec4242888a461054d142031212949d640bac3412/1200Wx1200H?use=banner&hybrisId=B2C&assetDescr=V39II-%281%29"
            },
            {
                id: 15,
                nom: "Cisco 24 Port PoE Switch C9200L-24P-4G-E",
                description: "Switch Cisco Catalyst 9200L 24 ports PoE, 4 ports SFP",
                prix: 950000,
                categorie: "Switchs",
                marque: "Cisco",
                modele: "C9200L-24P-4G-E",
                etat: "Neuf",
                image: "https://media.router-switch.com/media/catalog/product/cache/b90fceee6a5fa7acd36a04c7b968181c/c/i/cisco-c9200l-24p-4g-e.jpg"
            },
            {
                id: 16,
                nom: "Cisco Catalyst 24 Port Switches C9200L-24P-4G-A",
                description: "Switch Cisco Catalyst 9200L 24 ports PoE+, stackable",
                prix: 1200000,
                categorie: "Switchs",
                marque: "Cisco",
                modele: "C9300L-24P-4G-A",
                etat: "Neuf",
                image: "https://www.telquestintl.com/site/images/products/C9200L-24P-4G-A-WS.Media-1.jpg?resizeid=5&resizeh=1200&resizew=1200"
            },
            {
                id: 17,
                nom: "Cisco Business 24-Port Gigabit PoE+ Switch CBS350-24P-4G",
                description: "Switch Cisco Business 24 ports Gigabit PoE+, 4 ports SFP",
                prix: 360000,
                categorie: "Switchs",
                marque: "Cisco",
                modele: "CBS350-24P-4G",
                etat: "Neuf",
                image: "https://ci.jumia.is/unsafe/fit-in/500x500/filters:fill(white)/product/87/576422/1.jpg?2323"
            },
            {
                id: 18,
                nom: "HP Server Xeon Silver 4210R 32GB",
                description: "Serveur rack HP ProLiant DL380 Gen10, Xeon Silver 4210R, 32GB RAM",
                prix: 2200000,
                categorie: "Serveurs",
                marque: "HP",
                modele: "ProLiant DL380 Gen10",
                etat: "Neuf",
                image: "https://gfx3.senetic.com/akeneo-catalog/4/8/b/0/48b0bfd109e903c71d234a0fb690246f89b48884_1042669_P24841_B21_image2.jpg"
            },
            {
                id: 19,
                nom: "Dell Server Xeon E-2324G 16GB",
                description: "Serveur tour Dell PowerEdge T150, Xeon E-2324G, 16GB RAM",
                prix: 700000,
                categorie: "Serveurs",
                marque: "Dell",
                modele: "PowerEdge T150",
                etat: "Neuf",
                image: "https://ticou.ci/storage/media/SxYFIiKZL1qqyurjrqZaj7zu7PZ2xgiVRYa8MEz7.jpg"
            },
            {
                id: 20,
                nom: "Dell Server Xeon E-2314G 16GB",
                description: "Serveur rack Dell PowerEdge R250, Xeon E-2314G, 16GB RAM",
                prix: 1000000,
                categorie: "Serveurs",
                marque: "Dell",
                modele: "PowerEdge R250",
                etat: "Neuf",
                image: "https://thumb.pccomponentes.com/w-530-530/articles/1088/10888768/1600-servidor-dell-intel-xeon-e-2314-16gb-2tb-bastidor-4u-idrac9-no-os.jpg"
            },
            {
                id: 21,
                nom: "UC HP Desktop i3-12100 8GB 256GB",
                description: "Tour bureau HP 290 G9, i3-12100, 8GB RAM, 256GB SSD",
                prix: 230000,
                categorie: "Ordinateurs de Bureau",
                marque: "HP",
                modele: "290 G9 MT",
                etat: "Neuf",
                image: "https://dariacomputer.com/wp-content/uploads/2023/12/HP-Pro-Tower-290-G9-Desktop-PC-Intel-Core-I3-12100-8GB-DDR4-256GB-M.2-SSD-Windows-11-Pro-left-view-no-barcode.png"
            },
            {
                id: 22,
                nom: "UC HP Desktop i5-13500 8GB 512GB",
                description: "Tour bureau HP 290 G9, i5-13500, 8GB RAM, 512GB SSD",
                prix: 280000,
                categorie: "Ordinateurs de Bureau",
                marque: "HP",
                modele: "290 G9 MT",
                etat: "Neuf",
                image: "https://dariacomputer.com/wp-content/uploads/2023/12/HP-Pro-Tower-290-G9-Desktop-PC-Intel-Core-I3-12100-8GB-DDR4-256GB-M.2-SSD-Windows-11-Pro-left-view-no-barcode.png"
            },
            {
                id: 23,
                nom: "HP Aio i3-N300 8GB 512GB SSD 22\"",
                description: "PC All-in-One HP 22-dg0012, i3-N300, 8GB RAM, 512GB SSD",
                prix: 290000,
                categorie: "Ordinateurs de Bureau",
                marque: "HP",
                modele: "22-dg0012",
                etat: "Neuf",
                image: "https://www.hp.com/gb-en/shop/Html/Merch/Images/c08879690_1750x1285.jpg?imwidth=869"
            },
            {
                id: 24,
                nom: "HP Aio i3-N300 8GB 512GB SSD 24\"",
                description: "PC All-in-One HP 24-cr0012L, i3-N300, 8GB RAM, 512GB SSD",
                prix: 300000,
                categorie: "Ordinateurs de Bureau",
                marque: "HP",
                modele: "24-cr0012L",
                etat: "Neuf",
                image: "https://www.firstshop.co.za/cdn/shop/files/998k7et-all-in-one-desktops-45790917132452.png?v=1722900694&width=1214"
            },
            {
                id: 25,
                nom: "UC Dell Desktop i3-14100 8GB 512GB",
                description: "Tour bureau Dell Vostro 3030, i3-14100, 8GB RAM, 512GB SSD",
                prix: 230000,
                categorie: "Ordinateurs de Bureau",
                marque: "Dell",
                modele: "Vostro 3030",
                etat: "Neuf",
                image: "https://www.crenova.ma/37382-superlarge_default_2x/dell-vostro-3030-mt-i3-14100---8go-ram-512go-ssd-ubuntu-garantie-12m-vostrodt3030-i3-fd.jpg"
            },
            {
                id: 26,
                nom: "UC Dell Desktop i5-12500 8GB 512GB",
                description: "Tour bureau Dell Optiplex 7020MT, i5-12500, 8GB RAM, 512GB SSD",
                prix: 290000,
                categorie: "Ordinateurs de Bureau",
                marque: "Dell",
                modele: "Optiplex 7020MT",
                etat: "Neuf",
                image: "https://www.eit.com.bd/storage/images/80ozdesktop-optiplex-7020-mt-no-odd-black-gallery-2.png"
            },
            {
                id: 27,
                nom: "HP Desktop Mini i5-13th 16GB 512GB",
                description: "Mini bureau HP 260 G9, i5 13ème génération, 16GB RAM, 512GB SSD",
                prix: 300000,
                categorie: "Ordinateurs de Bureau",
                marque: "HP",
                modele: "260 G9",
                etat: "Neuf",
                image: "https://www.tic.ci/storage/mini1.png"
            },
            {
                id: 28,
                nom: "LED Monitor Lenovo 23.8\" FHD",
                description: "Écran LED Lenovo L24e-40 23.8\" Full HD, dalle IPS",
                prix: 75000,
                categorie: "Écrans",
                marque: "Lenovo",
                modele: "L24e-40",
                etat: "Neuf",
                image: "https://kotech.ci/wp-content/uploads/2025/04/81Roxm4z3L.jpg"
            },
            {
                id: 29,
                nom: "LED Monitor Lenovo 27.0\" IPS",
                description: "Écran LED Lenovo L27i-4A 27\" Full HD, dalle IPS",
                prix: 100000,
                categorie: "Écrans",
                marque: "Lenovo",
                modele: "L27i-4A",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.4S-JU5b-DfOb5a4yH8lINAHaHa?w=207&h=207&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 30,
                nom: "LED Monitor HP 22.0\" P22v G5",
                description: "Écran LED HP P22v G5 22\" Full HD, dalle IPS",
                prix: 65000,
                categorie: "Écrans",
                marque: "HP",
                modele: "P22v G5",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.MW1ujLEyVkCv5I0ECWbscAHaHa?w=215&h=215&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 31,
                nom: "LED Monitor Dell 27.0\" S2725H",
                description: "Écran LED Dell S2725H 27\" Full HD, dalle IPS",
                prix: 110000,
                categorie: "Écrans",
                marque: "Dell",
                modele: "S2725H",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.weH7EDe0RQgUVk59t_h1RgHaEK?w=303&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 32,
                nom: "LED Monitor HP 32.0\" 532SF",
                description: "Écran LED HP 32\" 532SF, résolution QHD, dalle IPS",
                prix: 145000,
                categorie: "Écrans",
                marque: "HP",
                modele: "32\" 532SF",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.MW1ujLEyVkCv5I0ECWbscAHaHa?w=215&h=215&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 33,
                nom: "Panasonic hybrid system KX-TES824CE",
                description: "Système téléphonique hybride Panasonic KX-TES824CE, 8 lignes",
                prix: 190000,
                categorie: "Accessoires Informatique",
                marque: "Panasonic",
                modele: "KX-TES824CE",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.sduapn3ptQYzRPhMq80s4gHaHa?w=211&h=211&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 34,
                nom: "HP Keyboard Wireless CS10 French",
                description: "Clavier sans fil HP CS10, disposition française",
                prix: 15000,
                categorie: "Accessoires Informatique",
                marque: "HP",
                modele: "CS10 French",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.8qUiwGk_9Q9CbVJz6bSUlgHaHa?w=212&h=212&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 35,
                nom: "MI TV Box S",
                description: "Boîtier TV Mi Box S, Android TV, 4K HDR",
                prix: 35000,
                categorie: "Accessoires Informatique",
                marque: "Xiaomi",
                modele: "Mi Box S",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.N6fV-6P3aYSpA_hVU-PZ0QHaEK?w=298&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 36,
                nom: "HP Laptop Core-7 16GB 512GB SSD 14.0\" Touch W11 Omnibook 5 Flip",
                description: "HP Omnibook 5 Flip 14-fp0023dx (B86Q7UA#ABA), écran tactile 14\", Windows 11",
                prix: 435000,
                categorie: "Ordinateurs Portables",
                marque: "HP",
                modele: "Omnibook 5 Flip 14-fp0023dx",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.YW7GNPUAYjfEeBOcw9fJDAHaEK?w=324&h=182&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 37,
                nom: "HP Laptop Ultra 7 32GB 2TB SSD W11 13.3\" Touch OLED",
                description: "HP Spectre x360 14t-eu000 avec stylet 7K635AV-3, écran OLED 13.3\" tactile",
                prix: 1200000,
                categorie: "Ordinateurs Portables",
                marque: "HP",
                modele: "Spectre x360 14t-eu000",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.YW7GNPUAYjfEeBOcw9fJDAHaEK?w=324&h=182&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 38,
                nom: "HP Laptop Ultra 7-155U 16GB 512GB SSD W11 Pro 13.3\" IPS WQXGA",
                description: "HP EliteBook 830 G11 (9G0D4ET#BH5), écran IPS WQXGA 13.3\", Windows 11 Pro",
                prix: 700000,
                categorie: "Ordinateurs Portables",
                marque: "HP",
                modele: "EliteBook 830 G11",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.YW7GNPUAYjfEeBOcw9fJDAHaEK?w=324&h=182&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 39,
                nom: "HP Laptop Core Ultra 7-256V 16GB 1TB SSD 14.0\" OLED Touch",
                description: "HP Omnibook X Flip 14-fm0023dx (B5UJ2UA#ABA), écran OLED tactile 14\"",
                prix: 560000,
                categorie: "Ordinateurs Portables",
                marque: "HP",
                modele: "Omnibook X Flip 14-fm0023dx",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.YW7GNPUAYjfEeBOcw9fJDAHaEK?w=324&h=182&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 40,
                nom: "HP Laptop i5-13420H 16GB 512GB SSD 6GB RTX4050 15.6\" FHD",
                description: "HP Victus 15-FA2701WM (B8LN4UA#ABA), RTX 4050 6GB, rétroéclairage, Windows 11",
                prix: 470000,
                categorie: "Ordinateurs Portables",
                marque: "HP",
                modele: "Victus 15-FA2701WM",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.YW7GNPUAYjfEeBOcw9fJDAHaEK?w=324&h=182&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 41,
                nom: "Dell Laptop i5-13th 16GB 512GB SSD 15.6\" DOS Latitude 5540",
                description: "Dell Latitude 5540, processeur i5 13ème génération, 6 mois de garantie",
                prix: 520000,
                categorie: "Ordinateurs Portables",
                marque: "Dell",
                modele: "Latitude 5540",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Q6fK1iqWrggIBIY8DUxr7QHaE8?w=266&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 42,
                nom: "Dell Laptop i5-13th 8GB 256GB SSD 13.3\" W11 Pro Latitude 13 5340",
                description: "Dell Latitude 13 5340, écran 13.3\", Windows 11 Professionnel",
                prix: 430000,
                categorie: "Ordinateurs Portables",
                marque: "Dell",
                modele: "Latitude 13 5340",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Q6fK1iqWrggIBIY8DUxr7QHaE8?w=266&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 43,
                nom: "Dell Laptop i7-1355U 16GB 512GB SSD 14.0\" DOS Backlit Latitude 3450",
                description: "Dell Latitude 3450, rétroéclairage, écran 14\", processeur i7-1355U",
                prix: 520000,
                categorie: "Ordinateurs Portables",
                marque: "Dell",
                modele: "Latitude 3450",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Q6fK1iqWrggIBIY8DUxr7QHaE8?w=266&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 44,
                nom: "Dell Laptop i7-1355U 8GB 512GB SSD 15.6\" FHD DOS Vostro 3530",
                description: "Dell Vostro 3530, écran Full HD 15.6\", processeur i7-1355U",
                prix: 360000,
                categorie: "Ordinateurs Portables",
                marque: "Dell",
                modele: "Vostro 3530",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Q6fK1iqWrggIBIY8DUxr7QHaE8?w=266&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 45,
                nom: "Asus Laptop i7-1355U 8GB 512GB SSD 15.6\" FHD DOS Backlit VivoBook",
                description: "Asus VivoBook X1504VA (90NB10J2-M00H50), rétroéclairage, écran Full HD 15.6\"",
                prix: 370000,
                categorie: "Ordinateurs Portables",
                marque: "Asus",
                modele: "VivoBook X1504VA",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.e0okXp35vapA23FCS6U_pAHaEK?w=315&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 46,
                nom: "Asus Laptop i7-13620H 16GB 1TB SSD 8GB RTX 4060 15.6\" FHD W11 TUF",
                description: "Asus TUF Gaming FX507VV, RTX 4060 8GB, écran Full HD 15.6\", Windows 11",
                prix: 760000,
                categorie: "Ordinateurs Portables",
                marque: "Asus",
                modele: "TUF FX507VV",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.e0okXp35vapA23FCS6U_pAHaEK?w=315&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 47,
                nom: "Acer Laptop i5-13500H 8GB 512GB SSD 15.6\" IPS FHD DOS Aspire Lite",
                description: "Acer Aspire Lite (NX.D5JEM.002), écran IPS Full HD 15.6\", couleur argent",
                prix: 300000,
                categorie: "Ordinateurs Portables",
                marque: "Acer",
                modele: "Aspire Lite",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Q6fK1iqWrggIBIY8DUxr7QHaE8?w=266&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 48,
                nom: "Acer Laptop i9-13900H 16GB 512GB SSD 8GB RTX5060 15.6\" DOS Nitro V15 Gaming",
                description: "Acer Nitro V15 Gaming - NH.QZ8EM.001, RTX 5060 8GB, processeur i9-13900H",
                prix: 780000,
                categorie: "Ordinateurs Portables",
                marque: "Acer",
                modele: "Nitro V15 Gaming",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Q6fK1iqWrggIBIY8DUxr7QHaE8?w=266&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 49,
                nom: "HP All-in-One i5-1235U 8GB 512GB SSD 21.5\" DOS 200 G4",
                description: "HP All-in-One 200 G4 (B6YN4ET#BH5), écran 21.5\", processeur i5-1235U",
                prix: 360000,
                categorie: "Ordinateurs de Bureau",
                marque: "HP",
                modele: "200 G4",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Zl28XMPOX51U7zTqQX-jIAHaE8?w=247&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 50,
                nom: "HP All-in-One i5-1334U 8GB 1TB SSD 23.8\" Touch DOS Shell White",
                description: "HP 24-CR0039L (B7FV2PA#UUF), écran tactile 23.8\", coque blanche",
                prix: 430000,
                categorie: "Ordinateurs de Bureau",
                marque: "HP",
                modele: "24-CR0039L",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Zl28XMPOX51U7zTqQX-jIAHaE8?w=247&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 51,
                nom: "HP All-in-One Core i5-1334U 16GB 512GB SSD 27.0\" DOS Shell White",
                description: "HP 27-CR0068NY, écran 27\", coque blanche, processeur i5-1334U",
                prix: 450000,
                categorie: "Ordinateurs de Bureau",
                marque: "HP",
                modele: "27-CR0068NY",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Zl28XMPOX51U7zTqQX-jIAHaE8?w=247&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 52,
                nom: "HP All-in-One i5-1334 8GB 512GB SSD 24.0\" FHD DOS 24 cr0049nh Black",
                description: "HP 24-CR0049NH (BJ9Y8PA#UUF), écran Full HD 24\", couleur noire",
                prix: 380000,
                categorie: "Ordinateurs de Bureau",
                marque: "HP",
                modele: "24-CR0049NH",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.Zl28XMPOX51U7zTqQX-jIAHaE8?w=247&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 53,
                nom: "Epson Printer Eco Tank Inkjet L18050 (Ex)",
                description: "Imprimante Epson EcoTank L18050, système à réservoir d'encre, format extra large",
                prix: 350000,
                categorie: "Imprimantes",
                marque: "Epson",
                modele: "EcoTank L18050",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.dCmg64e-kPgs7F8v_QNQRQHaHa?w=218&h=218&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 54,
                nom: "Epson Receipt Printer TMT20II",
                description: "Imprimante de tickets Epson TMT20II, thermique, impression rapide",
                prix: 95000,
                categorie: "Imprimantes",
                marque: "Epson",
                modele: "TMT20II",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.dCmg64e-kPgs7F8v_QNQRQHaHa?w=218&h=218&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 55,
                nom: "Canon Printer i-SENSYS LBP6030B",
                description: "Imprimante laser Canon i-SENSYS LBP6030B, monochrome, compacte",
                prix: 85000,
                categorie: "Imprimantes",
                marque: "Canon",
                modele: "i-SENSYS LBP6030B",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.dCmg64e-kPgs7F8v_QNQRQHaHa?w=218&h=218&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 56,
                nom: "Canon Printer i-SENSYS MF275dw",
                description: "Imprimante multifonction Canon i-SENSYS MF275dw, laser, WiFi, recto-verso automatique",
                prix: 170000,
                categorie: "Imprimantes",
                marque: "Canon",
                modele: "i-SENSYS MF275dw",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.dCmg64e-kPgs7F8v_QNQRQHaHa?w=218&h=218&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 57,
                nom: "Mikrotik Router RB951 UI 2HND",
                description: "Routeur Mikrotik RB951Ui-2HnD, 5 ports Gigabit, WiFi N, RouterOS",
                prix: 40000,
                categorie: "Routeurs",
                marque: "Mikrotik",
                modele: "RB951Ui-2HnD",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.-9sWev3e7C58-aUYDbIAvwHaE7?w=290&h=193&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            },
            {
                id: 58,
                nom: "Logitech Headset H390 USB",
                description: "Casque audio Logitech H390 (981-000406), microphone intégré, connexion USB",
                prix: 25000,
                categorie: "Accessoires Informatique",
                marque: "Logitech",
                modele: "H390",
                etat: "Neuf",
                image: "https://th.bing.com/th/id/OIP.4S-JU5b-DfOb5a4yH8lINAHaHa?w=207&h=207&c=7&r=0&o=5&dpr=1.3&pid=1.7"
            }
        ];

        // Variables globales
        let filteredProducts = [...produits];
        let currentCategory = "";
        let currentMarque = "";
        let currentSearch = "";

        // Fonction pour formater le prix
        function formatPrice(price) {
            return price.toString().replace(/\B(?=(\d{3})+(?!\d))/g, " ");
        }

        // Fonction pour afficher les produits
        function displayProducts() {
            const productsGrid = document.getElementById('productsGrid');
            productsGrid.innerHTML = '';
            
            if (filteredProducts.length === 0) {
                productsGrid.innerHTML = '<p style="text-align: center; padding: 40px; color: #666; grid-column: 1 / -1;">Aucun produit ne correspond à vos critères.</p>';
                return;
            }
            
            filteredProducts.forEach(product => {
                const productCard = document.createElement('div');
                productCard.className = 'product-card';
                
                // Choisir une icône selon la catégorie (pour placeholder)
                let icon = '💻';
                if (product.categorie.includes('Imprimante')) icon = '🖨️';
                if (product.categorie.includes('Scanner')) icon = '📄';
                if (product.categorie.includes('Switch')) icon = '🔌';
                if (product.categorie.includes('Serveur')) icon = '🖥️';
                if (product.categorie.includes('Écran')) icon = '🖥️';
                if (product.categorie.includes('Projecteur')) icon = '📽️';
                if (product.categorie.includes('Routeur')) icon = '📡';
                if (product.categorie.includes('Accessoire')) icon = '🎧';
                if (product.categorie.includes('Téléphonie')) icon = '📞';
                if (product.categorie.includes('PBX')) icon = '🏢';
                if (product.categorie.includes('Consommable')) icon = '🖨️';
                if (product.categorie.includes('WiFi')) icon = '📶';
                if (product.categorie.includes('Contrôleur')) icon = '🎛️';
                
                productCard.innerHTML = `
                    <div class="product-image" data-image="${product.image}" data-icon="${icon}">
                        <div class="image-placeholder">${icon}</div>
                    </div>
                    <div class="product-info">
                        <div class="product-brand">${product.marque}</div>
                        <div class="product-name">${product.nom}</div>
                        <div class="product-description">${product.description.substring(0, 80)}...</div>
                        <div class="product-price">${formatPrice(product.prix)} FCFA</div>
                        <button class="whatsapp-btn" onclick="contactWhatsApp(${product.id})">
                            <i class="fab fa-whatsapp"></i> Contact WhatsApp
                        </button>
                    </div>
                `;
                
                // Charger l'image en arrière-plan
                const imgDiv = productCard.querySelector('.product-image');
                const img = new Image();
                img.onload = function() {
                    imgDiv.style.backgroundImage = `url('${product.image}')`;
                    imgDiv.querySelector('.image-placeholder').style.display = 'none';
                };
                img.onerror = function() {
                    // Garder l'icône si l'image ne se charge pas
                    imgDiv.style.backgroundColor = '#f0f0f0';
                };
                img.src = product.image;
                
                productsGrid.appendChild(productCard);
            });
        }

        // Fonction pour filtrer les produits
        function filterProducts() {
            filteredProducts = produits.filter(product => {
                // Filtre par catégorie
                const matchesCategory = !currentCategory || product.categorie === currentCategory;
                
                // Filtre par marque
                const matchesMarque = !currentMarque || product.marque === currentMarque;
                
                // Filtre par recherche
                const matchesSearch = !currentSearch || 
                    product.nom.toLowerCase().includes(currentSearch) ||
                    product.description.toLowerCase().includes(currentSearch) ||
                    product.marque.toLowerCase().includes(currentSearch) ||
                    product.categorie.toLowerCase().includes(currentSearch) ||
                    product.modele.toLowerCase().includes(currentSearch);
                
                return matchesCategory && matchesMarque && matchesSearch;
            });
            
            displayProducts();
        }

        // Fonction pour créer les boutons de marque
        function createMarqueButtons() {
            const marquesGrid = document.getElementById('marquesGrid');
            marquesGrid.innerHTML = '';
            
            // Récupérer toutes les marques uniques
            const marques = [...new Set(produits.map(p => p.marque))].sort();
            
            // Ajouter un bouton "Toutes les marques"
            const allMarquesBtn = document.createElement('button');
            allMarquesBtn.className = 'marque-btn active';
            allMarquesBtn.textContent = 'Toutes';
            allMarquesBtn.onclick = () => {
                currentMarque = '';
                document.querySelectorAll('.marque-btn').forEach(btn => btn.classList.remove('active'));
                allMarquesBtn.classList.add('active');
                filterProducts();
            };
            marquesGrid.appendChild(allMarquesBtn);
            
            // Ajouter les boutons pour chaque marque
            marques.forEach(marque => {
                const marqueBtn = document.createElement('button');
                marqueBtn.className = 'marque-btn';
                marqueBtn.textContent = marque;
                marqueBtn.onclick = () => {
                    currentMarque = marque;
                    document.querySelectorAll('.marque-btn').forEach(btn => btn.classList.remove('active'));
                    marqueBtn.classList.add('active');
                    filterProducts();
                };
                marquesGrid.appendChild(marqueBtn);
            });
        }

        // Fonction pour contacter via WhatsApp
        function contactWhatsApp(productId) {
            const product = produits.find(p => p.id === productId);
            if (!product) return;
            
            const phoneNumber = "2250160435955";
            
            const message = `Bonjour TOP INFORMATIQUE! Je suis intéressé par ce produit:

🏷️ Produit: ${product.nom}
💰 Prix: ${formatPrice(product.prix)} FCFA
📂 Catégorie: ${product.categorie}
🏷️ Marque: ${product.marque}
🔧 Modèle: ${product.modele}
🆕 État: ${product.etat}

Est-il disponible?`;
            
            const encodedMessage = encodeURIComponent(message);
            const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodedMessage}`;
            
            window.open(whatsappUrl, '_blank', 'noopener,noreferrer');
        }

        // Initialisation
        document.addEventListener('DOMContentLoaded', () => {
            // Afficher tous les produits au départ
            displayProducts();
            
            // Créer les boutons de marque
            createMarqueButtons();
            
            // Configuration des filtres par catégorie
            document.querySelectorAll('.filter-btn').forEach(btn => {
                btn.addEventListener('click', () => {
                    currentCategory = btn.dataset.category;
                    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
                    btn.classList.add('active');
                    filterProducts();
                });
            });
            
            // Configuration des liens de navigation
            document.querySelectorAll('.nav-link').forEach(link => {
                link.addEventListener('click', (e) => {
                    e.preventDefault();
                    currentCategory = link.dataset.category;
                    document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
                    link.classList.add('active');
                    
                    // Mettre à jour aussi les boutons de filtre
                    document.querySelectorAll('.filter-btn').forEach(btn => {
                        btn.classList.toggle('active', btn.dataset.category === currentCategory);
                    });
                    
                    filterProducts();
                    window.scrollTo({ top: 0, behavior: 'smooth' });
                });
            });
            
            // Configuration de la recherche
            const searchInput = document.getElementById('searchInput');
            searchInput.addEventListener('input', (e) => {
                currentSearch = e.target.value.toLowerCase();
                filterProducts();
            });
            
            // Faire défiler jusqu'à la section produits quand on clique sur le CTA
            document.querySelector('.cta-button').addEventListener('click', (e) => {
                e.preventDefault();
                document.querySelector('#products').scrollIntoView({ 
                    behavior: 'smooth' 
                });
            });
        });
    </script>
</body>
</html>
