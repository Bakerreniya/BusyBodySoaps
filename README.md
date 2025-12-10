
<html lang="en" class="no-js">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0">
    <title>Busy Body Soaps - Handcrafted Soap Art</title>
    
    <!-- SIMPLIFIED STYLES - NO EXTERNAL DEPENDENCIES -->
    <style>
        /* === BASIC RESET === */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; }
        body { 
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
            background-color: #0A0E2A;
            color: #FFFFFF;
            line-height: 1.6;
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        /* === COLOR VARIABLES === */
        :root {
            --neon-orange: #FF4A24;
            --electric-blue: #46B8FF;
            --aqua-blue: #00D4FF;
            --deep-navy: #0A0E2A;
            --navy-card: #111535;
        }
        
        /* === FLOATING PARTICLES === */
        .particles-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
            overflow: hidden;
        }
        
        .particle {
            position: absolute;
            border-radius: 50%;
            background: var(--aqua-blue);
            opacity: 0.3;
            animation: floatParticle 20s infinite linear;
        }
        
        @keyframes floatParticle {
            0% { transform: translateY(100vh) rotate(0deg); }
            100% { transform: translateY(-100px) rotate(360deg); }
        }
        
        /* === LOADING SCREEN === */
        .loading {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: var(--deep-navy);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 99999;
            transition: opacity 0.5s ease;
        }
        
        .cyber-loader {
            width: 60px;
            height: 60px;
            border: 3px solid transparent;
            border-top-color: var(--neon-orange);
            border-radius: 50%;
            animation: spin 1s linear infinite;
            position: relative;
        }
        
        .cyber-loader::before {
            content: '';
            position: absolute;
            top: -5px;
            left: -5px;
            right: -5px;
            bottom: -5px;
            border: 2px solid transparent;
            border-top-color: var(--aqua-blue);
            border-radius: 50%;
            animation: spin 1.5s linear infinite reverse;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        .loading-text {
            margin-top: 20px;
            color: var(--aqua-blue);
            font-family: monospace;
            text-transform: uppercase;
            letter-spacing: 3px;
            font-size: 14px;
            animation: textGlow 2s infinite alternate;
        }
        
        @keyframes textGlow {
            0% { opacity: 0.7; text-shadow: 0 0 5px var(--aqua-blue); }
            100% { opacity: 1; text-shadow: 0 0 15px var(--aqua-blue), 0 0 20px var(--aqua-blue); }
        }
        
        /* === EXTRAVAGANT HEADER === */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 9999;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            overflow: hidden;
            background: linear-gradient(180deg, 
                rgba(10, 14, 42, 0.95) 0%,
                rgba(10, 14, 42, 0.85) 50%,
                rgba(10, 14, 42, 0.7) 100%);
            backdrop-filter: blur(15px);
            padding: 10px 0;
        }
        
        /* Header holographic effect */
        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg,
                transparent,
                rgba(255, 74, 36, 0.1),
                rgba(0, 212, 255, 0.1),
                rgba(255, 74, 36, 0.1),
                transparent);
            animation: hologramSweep 8s infinite linear;
            pointer-events: none;
            z-index: 1;
        }
        
        @keyframes hologramSweep {
            0% { left: -100%; }
            100% { left: 100%; }
        }
        
        /* Header bottom light effect */
        header::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg,
                transparent,
                var(--neon-orange),
                var(--aqua-blue),
                var(--neon-orange),
                transparent);
            box-shadow: 
                0 0 10px var(--neon-orange),
                0 0 20px var(--aqua-blue),
                0 0 30px rgba(255, 74, 36, 0.5);
            z-index: 2;
        }
        
        header.scrolled {
            padding: 5px 0;
            background: rgba(10, 14, 42, 0.98);
            box-shadow: 
                0 5px 30px rgba(0, 212, 255, 0.3),
                0 10px 60px rgba(255, 74, 36, 0.2);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
            z-index: 3;
        }
        
        /* === LOGO EXTRAVAGANCE === */
        .logo-text {
            font-family: 'Courier New', monospace;
            font-size: 32px;
            font-weight: 900;
            color: var(--neon-orange);
            text-transform: uppercase;
            letter-spacing: 4px;
            position: relative;
            padding: 10px 20px;
            text-shadow: 
                0 0 10px var(--neon-orange),
                0 0 20px rgba(255, 74, 36, 0.8),
                0 0 30px rgba(255, 74, 36, 0.6);
            animation: logoPulse 4s infinite alternate;
            background: linear-gradient(45deg, 
                transparent 0%,
                rgba(255, 74, 36, 0.1) 50%,
                transparent 100%);
            border: 2px solid transparent;
            border-image: linear-gradient(45deg, var(--neon-orange), var(--aqua-blue), var(--neon-orange)) 1;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .logo-text::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, 
                var(--neon-orange), 
                var(--aqua-blue), 
                var(--neon-orange),
                var(--aqua-blue),
                var(--neon-orange));
            z-index: -1;
            border-radius: 5px;
            opacity: 0.3;
            animation: borderRotate 6s linear infinite;
        }
        
        .logo-text::after {
            content: 'BUSY BODY SOAPS';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: transparent;
            background: linear-gradient(45deg, var(--aqua-blue), var(--neon-orange));
            -webkit-background-clip: text;
            background-clip: text;
            opacity: 0.7;
            animation: logoGlitch 5s infinite;
        }
        
        @keyframes logoPulse {
            0% { 
                text-shadow: 
                    0 0 10px var(--neon-orange),
                    0 0 20px rgba(255, 74, 36, 0.8),
                    0 0 30px rgba(255, 74, 36, 0.6);
            }
            100% { 
                text-shadow: 
                    0 0 20px var(--neon-orange),
                    0 0 40px rgba(255, 74, 36, 0.9),
                    0 0 60px rgba(255, 74, 36, 0.7);
            }
        }
        
        @keyframes borderRotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        @keyframes logoGlitch {
            0%, 100% { 
                clip-path: inset(0 0 0 0);
                transform: translate(0);
            }
            10% { 
                clip-path: inset(10% 0 20% 0);
                transform: translate(-2px, 2px);
            }
            20% { 
                clip-path: inset(20% 0 10% 0);
                transform: translate(2px, -2px);
            }
            30% { 
                clip-path: inset(10% 0 20% 0);
                transform: translate(-1px, 1px);
            }
            40% { 
                clip-path: inset(20% 0 10% 0);
                transform: translate(1px, -1px);
            }
            50% { 
                clip-path: inset(10% 0 20% 0);
                transform: translate(-2px, 2px);
            }
        }
        
        /* === NAVIGATION EXTRAVAGANCE === */
        .mobile-menu-btn {
            display: none;
            background: linear-gradient(45deg, var(--neon-orange), var(--aqua-blue));
            border: none;
            color: white;
            width: 60px;
            height: 60px;
            font-size: 24px;
            cursor: pointer;
            transition: all 0.3s;
            border-radius: 50%;
            position: relative;
            overflow: hidden;
            z-index: 1000;
            box-shadow: 
                0 0 10px var(--neon-orange),
                0 0 20px var(--aqua-blue),
                inset 0 0 10px rgba(255, 255, 255, 0.2);
        }
        
        .mobile-menu-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transform: translateX(-100%);
            transition: transform 0.6s;
        }
        
        .mobile-menu-btn:hover::before {
            transform: translateX(100%);
        }
        
        .mobile-menu-btn:hover {
            transform: rotate(90deg) scale(1.1);
            box-shadow: 
                0 0 20px var(--neon-orange),
                0 0 40px var(--aqua-blue);
        }
        
        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
            padding: 10px 20px;
            background: rgba(17, 21, 53, 0.7);
            border-radius: 50px;
            border: 2px solid transparent;
            border-image: linear-gradient(45deg, var(--neon-orange), var(--aqua-blue)) 1;
            position: relative;
            overflow: hidden;
        }
        
        nav ul::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, 
                transparent, 
                rgba(255, 74, 36, 0.2), 
                transparent);
            transition: left 0.7s;
            z-index: 0;
        }
        
        nav ul:hover::before {
            left: 100%;
        }
        
        nav a {
            color: #FFFFFF;
            text-decoration: none;
            text-transform: uppercase;
            font-size: 14px;
            letter-spacing: 2px;
            font-weight: 600;
            transition: all 0.3s;
            position: relative;
            padding: 10px 15px;
            z-index: 1;
            text-shadow: 0 0 5px rgba(255, 255, 255, 0.5);
        }
        
        nav a::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, var(--neon-orange), var(--aqua-blue));
            opacity: 0;
            transition: opacity 0.3s;
            border-radius: 5px;
            z-index: -1;
        }
        
        nav a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--neon-orange), var(--aqua-blue));
            transition: width 0.3s;
            box-shadow: 0 0 10px var(--aqua-blue);
        }
        
        nav a:hover {
            color: white;
            transform: translateY(-3px);
        }
        
        nav a:hover::before {
            opacity: 1;
        }
        
        nav a:hover::after {
            width: 80%;
        }
        
        /* === HEADER FLOATING SOAPS === */
        .floating-soaps {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }
        
        .floating-soap {
            position: absolute;
            width: 30px;
            height: 30px;
            border-radius: 5px;
            opacity: 0.2;
            animation: floatSoap 15s infinite linear;
        }
        
        .floating-soap:nth-child(1) {
            background: var(--neon-orange);
            top: 20%;
            left: 5%;
            animation-delay: 0s;
        }
        
        .floating-soap:nth-child(2) {
            background: var(--aqua-blue);
            top: 40%;
            left: 15%;
            animation-delay: 3s;
        }
        
        .floating-soap:nth-child(3) {
            background: var(--electric-blue);
            top: 60%;
            left: 10%;
            animation-delay: 6s;
        }
        
        .floating-soap:nth-child(4) {
            background: var(--neon-orange);
            top: 30%;
            right: 10%;
            animation-delay: 2s;
        }
        
        .floating-soap:nth-child(5) {
            background: var(--aqua-blue);
            top: 70%;
            right: 5%;
            animation-delay: 5s;
        }
        
        @keyframes floatSoap {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0.2;
            }
            25% {
                transform: translateY(-20px) rotate(90deg);
                opacity: 0.4;
            }
            50% {
                transform: translateY(-40px) rotate(180deg);
                opacity: 0.2;
            }
            75% {
                transform: translateY(-20px) rotate(270deg);
                opacity: 0.1;
            }
            100% {
                transform: translateY(0) rotate(360deg);
                opacity: 0.2;
            }
        }
        
        /* === HERO SECTION === */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 100px 20px;
            position: relative;
            background: linear-gradient(45deg, rgba(255, 74, 36, 0.1), rgba(70, 184, 255, 0.1));
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 50%, rgba(255, 74, 36, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 20%, rgba(70, 184, 255, 0.1) 0%, transparent 50%);
            z-index: -1;
        }
        
        .hero-content {
            max-width: 800px;
            padding: 40px;
            background-color: rgba(10, 14, 42, 0.7);
            backdrop-filter: blur(10px);
            border: 2px solid var(--aqua-blue);
            border-radius: 10px;
            position: relative;
            z-index: 1;
            animation: heroFloat 6s ease-in-out infinite;
        }
        
        @keyframes heroFloat {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        .hero h1 {
            font-size: 3.5rem;
            color: var(--neon-orange);
            margin-bottom: 20px;
            text-transform: uppercase;
            letter-spacing: 3px;
            animation: neonPulse 4s infinite alternate;
        }
        
        @keyframes neonPulse {
            0% { text-shadow: 0 0 10px var(--neon-orange), 0 0 20px rgba(255, 74, 36, 0.5); }
            100% { text-shadow: 0 0 20px var(--neon-orange), 0 0 40px rgba(255, 74, 36, 0.8), 0 0 60px rgba(255, 74, 36, 0.4); }
        }
        
        .hero p {
            font-size: 1.2rem;
            color: #E8EAFF;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--neon-orange);
            color: white;
            padding: 15px 30px;
            text-decoration: none;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-weight: bold;
            border: 2px solid var(--neon-orange);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
            border-radius: 5px;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.7s;
        }
        
        .btn:hover::before {
            left: 100%;
        }
        
        .btn:hover {
            background-color: transparent;
            color: var(--neon-orange);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(255, 74, 36, 0.3);
        }
        
        /* === PRODUCTS === */
        .products {
            padding: 80px 20px;
            position: relative;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--electric-blue);
            margin-bottom: 50px;
            text-transform: uppercase;
            letter-spacing: 2px;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--aqua-blue), transparent);
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .product-card {
            background-color: var(--navy-card);
            border: 2px solid var(--aqua-blue);
            border-radius: 10px;
            overflow: hidden;
            transition: all 0.4s;
            position: relative;
        }
        
        .product-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(0, 212, 255, 0.1), transparent);
            opacity: 0;
            transition: opacity 0.4s;
        }
        
        .product-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: var(--neon-orange);
            box-shadow: 0 15px 30px rgba(255, 74, 36, 0.2);
        }
        
        .product-card:hover::before {
            opacity: 1;
        }
        
        .product-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .product-card:hover .product-img {
            transform: scale(1.05);
        }
        
        .product-info {
            padding: 20px;
            position: relative;
            z-index: 1;
        }
        
        .product-name {
            font-size: 1.5rem;
            color: var(--aqua-blue);
            margin-bottom: 10px;
            transition: color 0.3s;
        }
        
        .product-card:hover .product-name {
            color: var(--neon-orange);
        }
        
        .product-desc {
            color: #B0B5D0;
            margin-bottom: 20px;
        }
        
        /* === MOBILE RESPONSIVE === */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            nav ul {
                display: none;
                position: fixed;
                top: 0;
                left: 0;
                width: 100%;
                height: 100vh;
                background-color: rgba(10, 14, 42, 0.98);
                flex-direction: column;
                justify-content: center;
                align-items: center;
                gap: 30px;
                z-index: 9998;
                border-radius: 0;
                padding: 40px 20px;
                border: none;
            }
            
            nav ul::before {
                display: none;
            }
            
            nav ul.active {
                display: flex;
            }
            
            .mobile-menu-btn {
                display: flex;
                align-items: center;
                justify-content: center;
                z-index: 9999;
            }
            
            .logo-text {
                font-size: 24px;
                letter-spacing: 2px;
                padding: 8px 15px;
            }
            
            .floating-soaps {
                display: none;
            }
        }
        
        /* === FADE-IN ANIMATIONS === */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }
        
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        /* === KEEPING REST OF STYLES FROM BEFORE === */
        /* ... (All the other styles for products, about, values, gallery, footer remain exactly the same as in your original) */
        
        /* === ABOUT === */
        .about {
            padding: 80px 20px;
            background-color: #0C112E;
            position: relative;
            overflow: hidden;
        }
        
        .about::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 10% 90%, rgba(255, 74, 36, 0.05) 0%, transparent 50%),
                radial-gradient(circle at 90% 10%, rgba(70, 184, 255, 0.05) 0%, transparent 50%);
        }
        
        .about-content {
            display: flex;
            flex-direction: column;
            gap: 40px;
            align-items: center;
            position: relative;
            z-index: 1;
        }
        
        @media (min-width: 992px) {
            .about-content {
                flex-direction: row;
            }
        }
        
        .about-img {
            flex: 1;
            min-height: 300px;
            background-color: var(--navy-card);
            border: 2px solid var(--aqua-blue);
            border-radius: 10px;
            position: relative;
            overflow: hidden;
        }
        
        .about-img::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, var(--aqua-blue), var(--neon-orange));
            opacity: 0.1;
            animation: gradientShift 10s infinite alternate;
        }
        
        @keyframes gradientShift {
            0% { opacity: 0.1; }
            100% { opacity: 0.2; }
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h2 {
            font-size: 2rem;
            color: var(--neon-orange);
            margin-bottom: 20px;
        }
        
        .about-text p {
            color: #E8EAFF;
            margin-bottom: 15px;
        }
        
        /* === VALUES === */
        .values {
            padding: 80px 20px;
            position: relative;
        }
        
        .values-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .value-card {
            background-color: var(--navy-card);
            padding: 30px;
            text-align: center;
            border: 2px solid #1A1F44;
            border-radius: 10px;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .value-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--aqua-blue), var(--neon-orange));
            transform: scaleX(0);
            transition: transform 0.3s;
        }
        
        .value-card:hover {
            border-color: var(--neon-orange);
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(255, 74, 36, 0.1);
        }
        
        .value-card:hover::before {
            transform: scaleX(1);
        }
        
        .value-icon {
            font-size: 2.5rem;
            color: var(--neon-orange);
            margin-bottom: 20px;
            display: inline-block;
            animation: iconFloat 3s infinite ease-in-out;
        }
        
        @keyframes iconFloat {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-5px); }
        }
        
        .value-card h3 {
            font-size: 1.3rem;
            color: var(--aqua-blue);
            margin-bottom: 15px;
        }
        
        .value-card p {
            color: #B0B5D0;
        }
        
        /* === GALLERY === */
        .gallery-section {
            padding: 80px 20px;
            background-color: #0C112E;
        }
        
        .slide-gallery {
            max-width: 1000px;
            margin: 0 auto;
            border: 2px solid var(--electric-blue);
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }
        
        .slides-container {
            display: flex;
            transition: transform 0.5s;
            height: 400px;
        }
        
        .slide {
            min-width: 100%;
            position: relative;
        }
        
        .slide::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, transparent 70%, rgba(10, 14, 42, 0.8) 100%);
        }
        
        .slide-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .gallery-controls {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .prev-btn, .next-btn {
            background-color: transparent;
            border: 2px solid var(--aqua-blue);
            color: var(--aqua-blue);
            width: 50px;
            height: 50px;
            font-size: 20px;
            cursor: pointer;
            transition: all 0.3s;
            border-radius: 50%;
            position: relative;
            overflow: hidden;
        }
        
        .prev-btn::before, .next-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: var(--aqua-blue);
            opacity: 0;
            transition: opacity 0.3s;
            border-radius: 50%;
        }
        
        .prev-btn:hover::before, .next-btn:hover::before {
            opacity: 0.1;
        }
        
        .prev-btn:hover, .next-btn:hover {
            border-color: var(--neon-orange);
            color: var(--neon-orange);
            transform: scale(1.1);
        }
        
        /* === FOOTER === */
        footer {
            padding: 60px 20px 30px;
            background-color: var(--deep-navy);
            border-top: 3px solid var(--neon-orange);
            position: relative;
            overflow: hidden;
        }
        
        footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 80%, rgba(255, 74, 36, 0.05) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(0, 212, 255, 0.05) 0%, transparent 50%);
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            max-width: 1400px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }
        
        .footer-logo {
            font-size: 2rem;
            color: var(--neon-orange);
            margin-bottom: 20px;
            font-family: monospace;
        }
        
        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border: 2px solid var(--aqua-blue);
            color: var(--aqua-blue);
            text-decoration: none;
            transition: all 0.3s;
            border-radius: 50%;
            position: relative;
            overflow: hidden;
        }
        
        .social-icons a::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: var(--aqua-blue);
            opacity: 0;
            transition: opacity 0.3s;
            border-radius: 50%;
        }
        
        .social-icons a:hover::before {
            opacity: 0.1;
        }
        
        .social-icons a:hover {
            border-color: var(--neon-orange);
            color: var(--neon-orange);
            transform: translateY(-3px);
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 10px;
        }
        
        .footer-links a {
            color: #B0B5D0;
            text-decoration: none;
            transition: all 0.3s;
            position: relative;
            padding-left: 0;
            transition: padding-left 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--aqua-blue);
            padding-left: 10px;
        }
        
        .footer-links a::before {
            content: '→';
            position: absolute;
            left: -15px;
            opacity: 0;
            transition: all 0.3s;
        }
        
        .footer-links a:hover::before {
            left: 0;
            opacity: 1;
        }
        
        .contact-info div {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
            color: #B0B5D0;
        }
        
        .copyright {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #1A1F44;
            color: #B0B5D0;
            position: relative;
            z-index: 1;
        }
        
        .btn-outline {
            display: inline-block;
            background-color: transparent;
            color: var(--aqua-blue);
            padding: 10px 20px;
            text-decoration: none;
            text-transform: uppercase;
            letter-spacing: 2px;
            border: 2px solid var(--aqua-blue);
            transition: all 0.3s;
            border-radius: 5px;
            position: relative;
            overflow: hidden;
        }
        
        .btn-outline::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 212, 255, 0.2), transparent);
            transition: left 0.7s;
        }
        
        .btn-outline:hover::before {
            left: 100%;
        }
        
        .btn-outline:hover {
            background-color: var(--aqua-blue);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 212, 255, 0.3);
        }
    </style>
</head>
<body>
    <!-- FLOATING PARTICLES -->
    <div class="particles-container" id="particlesContainer"></div>
    
    <!-- LOADING SCREEN -->
    <div class="loading" id="loading">
        <div class="cyber-loader"></div>
        <div class="loading-text">LOADING</div>
    </div>
    
    <!-- EXTRAVAGANT HEADER -->
    <header id="mainHeader">
        <!-- Floating soap bubbles -->
        <div class="floating-soaps">
            <div class="floating-soap"></div>
            <div class="floating-soap"></div>
            <div class="floating-soap"></div>
            <div class="floating-soap"></div>
            <div class="floating-soap"></div>
        </div>
        
        <div class="header-container">
            <div class="logo-text">BUSY BODY SOAPS</div>
            
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                ☰
            </button>
            
            <nav>
                <ul id="navMenu">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#values">Values</a></li>
                    <li><a href="#gallery">Gallery</a></li>
                </ul>
            </nav>
        </div>
    </header>
    
    <!-- HERO -->
    <section class="hero" id="home">
        <div class="hero-content fade-in">
            <h1>Handcrafted Soap Art</h1>
            <p>Natural, clean, and thoughtfully crafted soaps made with only the finest ingredients. Each bar is a unique creation designed to elevate your daily routine.</p>
            <a href="#products" class="btn">Shop Collection</a>
        </div>
    </section>
    
    <!-- PRODUCTS -->
    <section class="products" id="products">
        <div class="container">
            <h2 class="section-title fade-in">Our Collection</h2>
            <div class="products-grid">
                <div class="product-card fade-in">
                    <img src="https://i.postimg.cc/mDgxM5Cs/IMG_7110.jpg" alt="Aloe Vera and Turmeric Soap" class="product-img">
                    <div class="product-info">
                        <h3 class="product-name">Aloe Vera & Turmeric</h3>
                        <p class="product-desc">Soothing aloe vera combined with anti-inflammatory turmeric for calm, radiant skin.</p>
                        <a href="#" class="btn-outline">View Details</a>
                    </div>
                </div>
                
                <div class="product-card fade-in">
                    <img src="https://i.postimg.cc/B6nWDVDm/IMG_7116.jpg" alt="Lavender and Honey Soap" class="product-img">
                    <div class="product-info">
                        <h3 class="product-name">Lavender & Honey</h3>
                        <p class="product-desc">Calming lavender essential oil paired with moisturizing raw honey.</p>
                        <a href="#" class="btn-outline">View Details</a>
                    </div>
                </div>
                
                <div class="product-card fade-in">
                    <img src="https://i.postimg.cc/pTLN868S/IMG_7108.jpg" alt="Bamboo Charcoal and Turmeric Soap" class="product-img">
                    <div class="product-info">
                        <h3 class="product-name">Bamboo Charcoal & Turmeric</h3>
                        <p class="product-desc">Detoxifying bamboo charcoal combined with brightening turmeric.</p>
                        <a href="#" class="btn-outline">View Details</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- ABOUT -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title fade-in">About Us</h2>
            <div class="about-content">
                <div class="about-img fade-in"></div>
                <div class="about-text fade-in">
                    <h2>Crafting with Purpose</h2>
                    <p>Busy Body Soaps was born from a passion for creating beautiful, functional products that honor both artistry and simplicity.</p>
                    <p>Each soap is handcrafted with intention, using only natural ingredients that nourish the skin.</p>
                    <p>From selecting sustainable ingredients to designing each bar's aesthetic, every step is done with care.</p>
                    <a href="#gallery" class="btn">View Gallery</a>
                </div>
            </div>
        </div>
    </section>
    
    <!-- VALUES -->
    <section class="values" id="values">
        <div class="container">
            <h2 class="section-title fade-in">Our Values</h2>
            <div class="values-grid">
                <div class="value-card fade-in">
                    <div class="value-icon">🌿</div>
                    <h3>Natural Ingredients</h3>
                    <p>We use only plant-based oils, butters, and botanicals in our formulations.</p>
                </div>
                
                <div class="value-card fade-in">
                    <div class="value-icon">✋</div>
                    <h3>Handcrafted</h3>
                    <p>Every bar is made by hand in small batches for quality and attention to detail.</p>
                </div>
                
                <div class="value-card fade-in">
                    <div class="value-icon">🎨</div>
                    <h3>Artistic Design</h3>
                    <p>We believe everyday products should be beautiful as well as functional.</p>
                </div>
                
                <div class="value-card fade-in">
                    <div class="value-icon">♻️</div>
                    <h3>Sustainable</h3>
                    <p>Eco-friendly packaging and responsible sourcing are central to our practice.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- GALLERY -->
    <section class="gallery-section" id="gallery">
        <div class="container">
            <h2 class="section-title fade-in">Gallery</h2>
            
            <div class="slide-gallery fade-in">
                <div class="slides-container" id="slidesContainer">
                    <div class="slide">
                        <img src="https://i.postimg.cc/mDgxM5Cs/IMG_7110.jpg" alt="Aloe Vera Soap" class="slide-img">
                    </div>
                    <div class="slide">
                        <img src="https://i.postimg.cc/B6nWDVDm/IMG_7116.jpg" alt="Lavender Soap" class="slide-img">
                    </div>
                    <div class="slide">
                        <img src="https://i.postimg.cc/pTLN868S/IMG_7108.jpg" alt="Bamboo Charcoal Soap" class="slide-img">
                    </div>
                </div>
                
                <div class="gallery-controls">
                    <button class="prev-btn" id="prevBtn">←</button>
                    <button class="next-btn" id="nextBtn">→</button>
                </div>
            </div>
        </div>
    </section>
    
    <!-- FOOTER -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="fade-in">
                    <div class="footer-logo">BUSY BODY SOAPS</div>
                    <p>Handcrafted soap creations where natural ingredients meet artistic design.</p>
                    <div class="social-icons">
                        <a href="#"><i>📷</i></a>
                        <a href="#"><i>🛍️</i></a>
                        <a href="#"><i>✉️</i></a>
                    </div>
                </div>
                
                <div class="fade-in">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#products">Products</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#values">Values</a></li>
                        <li><a href="#gallery">Gallery</a></li>
                    </ul>
                </div>
                
                <div class="fade-in">
                    <h3>Contact</h3>
                    <div class="contact-info">
                        <div><span>📍</span> <span>Mebi Kli Lopera Rd</span></div>
                        <div><span>📞</span> <span>(215) 651-3763</span></div>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Busy Body Soaps. All rights reserved. CLEAN</p>
            </div>
        </div>
    </footer>
    
    <script>
        // ENHANCED JAVASCRIPT WITH EXTRAVAGANT HEADER EFFECTS
        
        // DOM Ready
        document.addEventListener('DOMContentLoaded', function() {
            // Initialize floating particles
            initParticles();
            
            // Hide loading screen
            setTimeout(function() {
                const loading = document.getElementById('loading');
                if (loading) {
                    loading.style.opacity = '0';
                    setTimeout(function() {
                        loading.style.display = 'none';
                    }, 500);
                }
            }, 1000);
            
            // Initialize mobile menu
            initMobileMenu();
            
            // Initialize gallery
            initGallery();
            
            // Initialize smooth scroll
            initSmoothScroll();
            
            // Initialize scroll effects
            initScrollEffects();
            
            // Initialize fade-in animations
            initFadeIn();
            
            // Initialize header effects
            initHeaderEffects();
        });
        
        // FLOATING PARTICLES
        function initParticles() {
            const particlesContainer = document.getElementById('particlesContainer');
            if (!particlesContainer) return;
            
            const particleCount = 30;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.classList.add('particle');
                
                const size = Math.random() * 4 + 2;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                
                particle.style.left = `${Math.random() * 100}%`;
                particle.style.top = `${Math.random() * 100}%`;
                
                particle.style.backgroundColor = Math.random() > 0.5 ? 'var(--aqua-blue)' : 'var(--neon-orange)';
                
                const duration = Math.random() * 20 + 15;
                particle.style.animationDuration = `${duration}s`;
                
                particle.style.animationDelay = `${Math.random() * 5}s`;
                
                particlesContainer.appendChild(particle);
            }
        }
        
        // MOBILE MENU
        function initMobileMenu() {
            const mobileMenuBtn = document.getElementById('mobileMenuBtn');
            const navMenu = document.getElementById('navMenu');
            const header = document.getElementById('mainHeader');
            
            if (!mobileMenuBtn || !navMenu || !header) return;
            
            mobileMenuBtn.addEventListener('click', function() {
                navMenu.classList.toggle('active');
                document.body.style.overflow = navMenu.classList.contains('active') ? 'hidden' : 'auto';
                
                // Change button icon with animation
                this.innerHTML = navMenu.classList.contains('active') ? '✕' : '☰';
                this.style.transform = navMenu.classList.contains('active') ? 'rotate(180deg)' : 'rotate(0deg)';
            });
            
            // Close menu when clicking links
            document.querySelectorAll('nav a').forEach(link => {
                link.addEventListener('click', function() {
                    navMenu.classList.remove('active');
                    document.body.style.overflow = 'auto';
                    mobileMenuBtn.innerHTML = '☰';
                    mobileMenuBtn.style.transform = 'rotate(0deg)';
                });
            });
        }
        
        // GALLERY
        function initGallery() {
            const slidesContainer = document.getElementById('slidesContainer');
            const prevBtn = document.getElementById('prevBtn');
            const nextBtn = document.getElementById('nextBtn');
            
            if (!slidesContainer || !prevBtn || !nextBtn) return;
            
            let currentSlide = 0;
            const slides = document.querySelectorAll('.slide');
            const totalSlides = slides.length;
            
            if (totalSlides === 0) return;
            
            function updateSlide() {
                slidesContainer.style.transform = `translateX(-${currentSlide * 100}%)`;
                
                // Add a subtle zoom effect on slide change
                slides.forEach((slide, index) => {
                    if (index === currentSlide) {
                        slide.style.transform = 'scale(1.05)';
                        setTimeout(() => {
                            slide.style.transform = 'scale(1)';
                        }, 500);
                    }
                });
            }
            
            prevBtn.addEventListener('click', function() {
                currentSlide = (currentSlide - 1 + totalSlides) % totalSlides;
                updateSlide();
                
                // Button click effect
                this.style.transform = 'scale(0.9)';
                setTimeout(() => {
                    this.style.transform = 'scale(1)';
                }, 200);
            });
            
            nextBtn.addEventListener('click', function() {
                currentSlide = (currentSlide + 1) % totalSlides;
                updateSlide();
                
                // Button click effect
                this.style.transform = 'scale(0.9)';
                setTimeout(() => {
                    this.style.transform = 'scale(1)';
                }, 200);
            });
            
            // Auto slide every 5 seconds
            setInterval(function() {
                currentSlide = (currentSlide + 1) % totalSlides;
                updateSlide();
            }, 5000);
        }
        
        // SMOOTH SCROLL
        function initSmoothScroll() {
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    if (targetId === '#') return;
                    
                    const targetElement = document.querySelector(targetId);
                    if (targetElement) {
                        const headerHeight = document.querySelector('header').offsetHeight;
                        const targetPosition = targetElement.getBoundingClientRect().top + window.pageYOffset;
                        
                        window.scrollTo({
                            top: targetPosition - headerHeight,
                            behavior: 'smooth'
                        });
                    }
                });
            });
        }
        
        // SCROLL EFFECTS
        function initScrollEffects() {
            const header = document.getElementById('mainHeader');
            
            window.addEventListener('scroll', function() {
                // Header effect on scroll
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }
            });
        }
        
        // FADE-IN ANIMATIONS
        function initFadeIn() {
            const fadeElements = document.querySelectorAll('.fade-in');
            
            function checkFade() {
                fadeElements.forEach(element => {
                    const elementTop = element.getBoundingClientRect().top;
                    const elementVisible = 150;
                    
                    if (elementTop < window.innerHeight - elementVisible) {
                        element.classList.add('visible');
                    }
                });
            }
            
            // Check on load
            checkFade();
            
            // Check on scroll
            window.addEventListener('scroll', checkFade);
        }
        
        // HEADER EFFECTS
        function initHeaderEffects() {
            const header = document.getElementById('mainHeader');
            const logo = document.querySelector('.logo-text');
            
            if (!logo) return;
            
            // Logo interactive effect on mouse move
            document.addEventListener('mousemove', function(e) {
                const x = (e.clientX / window.innerWidth) * 100;
                const y = (e.clientY / window.innerHeight) * 100;
                
                // Move gradient background
                logo.style.background = `linear-gradient(${x}deg, 
                    transparent 0%,
                    rgba(255, 74, 36, 0.1) 50%,
                    transparent 100%)`;
            });
            
            // Header parallax effect
            window.addEventListener('scroll', function() {
                const scrolled = window.pageYOffset;
                const rate = scrolled * -0.5;
                
                // Subtle parallax for the floating soaps
                const floatingSoaps = document.querySelector('.floating-soaps');
                if (floatingSoaps) {
                    floatingSoaps.style.transform = `translateY(${rate}px)`;
                }
            });
        }
    </script>
</body>
</html>
