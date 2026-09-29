<?php
$current_page = basename($_SERVER['PHP_SELF']);
$whatsapp_num = "256777990562";
$whatsapp_link = "https://wa.me/" . $whatsapp_num . "?text=" . urlencode("Hello! I would like to inquire about a luxury expedition with REN Gorilla Expeditions.");
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>REN Gorilla Expeditions | Luxury African Safaris</title>
    <link rel="stylesheet" href="style.css">
    <!-- Google Fonts for Luxury Typography -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Montserrat:wght@300;400;500;600&display=swap" rel="stylesheet">
</head>
<body>
    <a href="#main-content" class="skip-link">Skip to main content</a>
    
    <header class="site-header">
        <div class="header-container">
            <a href="index.php" class="brand-logo" aria-label="REN Gorilla Expeditions Homepage">
                <span class="logo-ren">REN</span>
                <span class="logo-sub">GORILLA EXPEDITIONS</span>
            </a>
            
            <nav class="main-nav" aria-label="Main Navigation">
                <ul>
                    <li><a href="index.php" class="<?php echo ($current_page == 'index.php') ? 'active' : ''; ?>">Home</a></li>
                    <li><a href="about.php" class="<?php echo ($current_page == 'about.php') ? 'active' : ''; ?>">About REN</a></li>
                    <li><a href="expeditions.php" class="<?php echo ($current_page == 'expeditions.php') ? 'active' : ''; ?>">Expeditions</a></li>
                    <li><a href="contact.php" class="<?php echo ($current_page == 'contact.php') ? 'active' : ''; ?>">Contact</a></li>
                </ul>
            </nav>

            <a href="<?php echo $whatsapp_link; ?>" class="btn-whatsapp-header" target="_blank" rel="noopener noreferrer" aria-label="Book via WhatsApp">
                Book on WhatsApp
            </a>
        </div>
    </header>
    <main id="main-content">
</main>
    <footer class="site-footer">
        <div class="footer-container">
            <div class="footer-brand">
                <span class="logo-ren">REN</span>
                <span class="logo-sub">GORILLA EXPEDITIONS</span>
                <p>Purposeful journeys through Africa's extraordinary wilderness. Built around Respect, Exploration, and Nature.</p>
            </div>
            
            <div class="footer-links">
                <h2>Navigation</h2>
                <ul>
                    <li><a href="index.php">Home</a></li>
                    <li><a href="about.php">About Us</a></li>
                    <li><a href="expeditions.php">Curated Expeditions</a></li>
                    <li><a href="contact.php">Contact & Reservations</a></li>
                </ul>
            </div>

            <div class="footer-contact">
                <h2>Direct Inquiries</h2>
                <p>Kampala & Bwindi, Uganda</p>
                <p>Phone / WhatsApp: <a href="https://wa.me/256777990562" class="footer-phone">+256 777 990 562</a></p>
                <p>Email: reservations@rengorillaexpeditions.com</p>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; <?php echo date("Y"); ?> REN Gorilla Expeditions. All Rights Reserved.</p>
        </div>
    </footer>

    <!-- Floating Accessibility-Compliant WhatsApp Button -->
    <a href="<?php echo $whatsapp_link; ?>" class="whatsapp-float" target="_blank" rel="noopener noreferrer" aria-label="Chat with us on WhatsApp">
        <svg viewBox="0 0 32 32" class="whatsapp-icon" aria-hidden="true" focusable="false">
            <path fill="currentColor" d="M16 2a13 13 0 0 0-11 20L3 29l7-2a13 13 0 1 0 6-25zm0 24a11 11 0 0 1-5.5-1.5l-.4-.2-4.1 1.1 1.1-4-.3-.4A11 11 0 1 1 16 26zm6-8c-.3-.2-1.9-1-2.2-1.1-.3-.1-.5-.2-.7.2s-.8 1.1-1 1.3c-.2.2-.4.2-.7 0a9 9 0 0 1-2.6-1.6 10 10 0 0 1-1.8-2.3c-.2-.3 0-.5.1-.6l.5-.6c.1-.2.2-.4.3-.5 0-.2 0-.4 0-.5s-.7-1.7-1-2.3c-.3-.6-.5-.5-.7-.5h-.6c-.2 0-.6.1-.9.4s-1.2 1.2-1.2 2.9 1.2 3.4 1.4 3.6c.2.2 2.4 3.7 5.9 5.2.8.3 1.5.6 2 .7 1 .3 1.8.3 2.5.2.8-.1 2.4-1 2.7-2 .3-1 .3-1.8.2-1.9-.1-.1-.3-.2-.6-.4z"/>
        </svg>
        <span class="float-text">Chat with Us</span>
    </a>
</body>
</html>
/* ==========================================================================
   REN GORILLA EXPEDITIONS - Accessible Luxury Styling
   ========================================================================== */

:root {
    --color-bg-dark: #0d110e;
    --color-surface: #161c18;
    --color-surface-light: #212924;
    --color-gold-accent: #d4af37;
    --color-gold-hover: #f3e5ab;
    --color-text-light: #f5f5f7;
    --color-text-muted: #c5c8c6;
    --color-focus: #268bd2;
    --font-heading: 'Cinzel', serif;
    --font-body: 'Montserrat', sans-serif;
}

/* Accessibility Core */
*, *::before, *::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    background-color: var(--color-bg-dark);
    color: var(--color-text-light);
    font-family: var(--font-body);
    line-height: 1.7;
    font-size: 1rem;
}

a {
    color: var(--color-gold-accent);
    text-decoration: none;
    transition: color 0.3s ease;
}

a:hover, a:focus {
    color: var(--color-gold-hover);
}

a:focus-visible, button:focus-visible {
    outline: 3px solid var(--color-focus);
    outline-offset: 4px;
}

.skip-link {
    position: absolute;
    top: -40px;
    left: 10px;
    background: var(--color-gold-accent);
    color: #000;
    padding: 8px 16px;
    z-index: 1000;
    font-weight: 600;
}

.skip-link:focus {
    top: 10px;
}

/* Header & Navigation */
.site-header {
    background-color: rgba(13, 17, 14, 0.95);
    border-bottom: 1px solid rgba(212, 175, 55, 0.2);
    position: sticky;
    top: 0;
    z-index: 100;
    backdrop-filter: blur(8px);
}

.header-container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 1.2rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.brand-logo {
    display: flex;
    flex-direction: column;
}

.logo-ren {
    font-family: var(--font-heading);
    font-size: 1.8rem;
    font-weight: 700;
    letter-spacing: 4px;
    color: var(--color-gold-accent);
    line-height: 1;
}

.logo-sub {
    font-size: 0.65rem;
    letter-spacing: 3px;
    color: var(--color-text-light);
    margin-top: 4px;
}

.main-nav ul {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.main-nav a {
    color: var(--color-text-light);
    font-size: 0.9rem;
    text-transform: uppercase;
    letter-spacing: 1.5px;
    font-weight: 400;
}

.main-nav a.active, .main-nav a:hover {
    color: var(--color-gold-accent);
    border-bottom: 2px solid var(--color-gold-accent);
    padding-bottom: 4px;
}

.btn-whatsapp-header {
    border: 1px solid var(--color-gold-accent);
    color: var(--color-gold-accent);
    padding: 0.6rem 1.2rem;
    font-size: 0.85rem;
    letter-spacing: 1px;
    text-transform: uppercase;
    border-radius: 2px;
}

.btn-whatsapp-header:hover {
    background-color: var(--color-gold-accent);
    color: var(--color-bg-dark);
}

/* Hero Section */
.hero {
    position: relative;
    height: 80vh;
    min-height: 500px;
    background: linear-gradient(rgba(13, 17, 14, 0.4), rgba(13, 17, 14, 0.8)), 
                url('https://images.unsplash.com/photo-1516426122078-c23e76319801?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: 0 1.5rem;
}

.hero-content {
    max-width: 900px;
}

.hero h1 {
    font-family: var(--font-heading);
    font-size: 3.2rem;
    letter-spacing: 2px;
    margin-bottom: 1rem;
    color: #ffffff;
}

.hero p {
    font-size: 1.25rem;
    color: var(--color-text-muted);
    margin-bottom: 2rem;
    font-weight: 300;
}

/* Buttons */
.btn-gold {
    display: inline-block;
    background-color: var(--color-gold-accent);
    color: var(--color-bg-dark);
    padding: 0.9rem 2rem;
    font-size: 0.9rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 2px;
    border-radius: 2px;
    border: none;
    cursor: pointer;
}

.btn-gold:hover {
    background-color: var(--color-gold-hover);
    color: var(--color-bg-dark);
}

/* Layout Modules */
.section {
    padding: 5rem 2rem;
    max-width: 1200px;
    margin: 0 auto;
}

.section-title {
    font-family: var(--font-heading);
    font-size: 2.2rem;
    text-align: center;
    color: var(--color-gold-accent);
    margin-bottom: 1rem;
}

.section-subtitle {
    text-align: center;
    color: var(--color-text-muted);
    margin-bottom: 3rem;
    max-width: 700px;
    margin-left: auto;
    margin-right: auto;
}

/* REN Values Grid */
.values-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 2rem;
    margin-top: 3rem;
}

.value-card {
    background-color: var(--color-surface);
    padding: 2.5rem 2rem;
    border-left: 3px solid var(--color-gold-accent);
    border-radius: 2px;
}

.value-card h3 {
    font-family: var(--font-heading);
    font-size: 1.5rem;
    color: var(--color-gold-accent);
    margin-bottom: 1rem;
}

/* Visual Gallery Cards */
.gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 2rem;
}

.expedition-card {
    background-color: var(--color-surface);
    border-radius: 4px;
    overflow: hidden;
    border: 1px solid rgba(212, 175, 55, 0.1);
}

.expedition-card img {
    width: 100%;
    height: 260px;
    object-fit: cover;
    display: block;
}

.expedition-info {
    padding: 1.8rem;
}

.expedition-info h3 {
    font-family: var(--font-heading);
    font-size: 1.4rem;
    margin-bottom: 0.5rem;
    color: #ffffff;
}

/* Contact Page Form */
.contact-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 3rem;
}

.form-group {
    margin-bottom: 1.5rem;
}

.form-group label {
    display: block;
    margin-bottom: 0.5rem;
    color: var(--color-text-light);
    font-size: 0.9rem;
}

.form-group input, .form-group textarea {
    width: 100%;
    padding: 0.8rem;
    background-color: var(--color-surface-light);
    border: 1px solid rgba(212, 175, 55, 0.3);
    color: #ffffff;
    border-radius: 2px;
    font-family: var(--font-body);
}

.form-group input:focus, .form-group textarea:focus {
    outline: 2px solid var(--color-gold-accent);
}

/* Footer */
.site-footer {
    background-color: #080a08;
    border-top: 1px solid rgba(212, 175, 55, 0.2);
    padding: 4rem 2rem 2rem 2rem;
}

.footer-container {
    max-width: 1200px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2.5rem;
}

.footer-links h2, .footer-contact h2 {
    font-family: var(--font-heading);
    font-size: 1.1rem;
    color: var(--color-gold-accent);
    margin-bottom: 1.2rem;
}

.footer-links ul {
    list-style: none;
}

.footer-links li {
    margin-bottom: 0.6rem;
}

.footer-phone {
    font-weight: 600;
    font-size: 1.1rem;
}

.footer-bottom {
    max-width: 1200px;
    margin: 3rem auto 0 auto;
    padding-top: 1.5rem;
    border-top: 1px solid rgba(255, 255, 255, 0.05);
    text-align: center;
    font-size: 0.85rem;
    color: var(--color-text-muted);
}

/* Floating WhatsApp Button */
.whatsapp-float {
    position: fixed;
    bottom: 25px;
    right: 25px;
    background-color: #25D366;
    color: #ffffff;
    padding: 12px 20px;
    border-radius: 50px;
    display: flex;
    align-items: center;
    gap: 10px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.4);
    z-index: 1000;
    font-weight: 600;
}

.whatsapp-float:hover {
    background-color: #20ba5a;
    color: #ffffff;
}

.whatsapp-icon {
    width: 24px;
    height: 24px;
}

/* Responsive adjustments */
@media (max-width: 768px) {
    .header-container {
        flex-direction: column;
        gap: 1rem;
    }
    .main-nav ul {
        gap: 1rem;
    }
    .hero h1 {
        font-size: 2.2rem;
    }
    .contact-container {
        grid-template-columns: 1fr;
    }
}
<?php include('header.php'); ?>

<section class="hero" aria-label="Introduction Image">
    <div class="hero-content">
        <h1>REN GORILLA EXPEDITIONS</h1>
        <p>Purposeful Journeys | Rare Wildlife Encounters | Uncompromising Luxury</p>
        <a href="<?php echo $whatsapp_link; ?>" class="btn-gold" target="_blank" rel="noopener noreferrer">Inquire via WhatsApp</a>
    </div>
</section>

<section class="section">
    <h2 class="section-title">The REN Brand Identity</h2>
    <p class="section-subtitle">Defining luxury safari travel through core values that safeguard Africa’s rarest ecosystems.</p>
    
    <div class="values-grid">
        <article class="value-card">
            <h3>R — Respect</h3>
            <p>We respect the pristine places and cultures we encounter, partnering with indigenous communities and strictly supporting sustainable conservation initiatives.</p>
        </article>
        
        <article class="value-card">
            <h3>E — Explore</h3>
            <p>We craft tailored journeys into extraordinary, untouched landscapes—taking you beyond standard travel into deeply memorable discoveries.</p>
        </article>
        
        <article class="value-card">
            <h3>N — Nature</h3>
            <p>We protect the natural world that makes every expedition possible, maintaining low-impact, eco-luxury practices across all wilderness safaris.</p>
        </article>
    </div>
</section>

<section class="section" style="background-color: var(--color-surface);">
    <h2 class="section-title">Icons of the African Wilderness</h2>
    <p class="section-subtitle">Experience curated encounters with world-renowned species in their natural habitats.</p>
    
    <div class="gallery-grid">
        <article class="expedition-card">
            <img src="https://images.unsplash.com/photo-1546182990-dffeafbe841d?auto=format&fit=crop&w=800&q=80" alt="Majestic male lion resting on the African savanna">
            <div class="expedition-info">
                <h3>Savanna Predators</h3>
                <p>Private game drives tracking tree-climbing lions and leopards across Queen Elizabeth and Murchison Falls National Parks.</p>
            </div>
        </article>

        <article class="expedition-card">
            <img src="https://images.unsplash.com/photo-1516426122078-c23e76319801?auto=format&fit=crop&w=800&q=80" alt="Mountain gorilla in the dense forest of Bwindi Impenetrable National Park">
            <div class="expedition-info">
                <h3>Mountain Gorilla Trekking</h3>
                <p>Exclusive gorilla habituation and tracking experiences in Uganda's ancient Bwindi Impenetrable Forest.</p>
            </div>
        </article>

        <article class="expedition-card">
            <img src="https://images.unsplash.com/photo-1557050543-4d5f4e07ef46?auto=format&fit=crop&w=800&q=80" alt="African elephant herd moving together at sunset">
            <div class="expedition-info">
                <h3>Gentle Giants</h3>
                <p>Guided, immersive encounters with wild African elephant herds along the Kazinga Channel and savanna corridors.</p>
            </div>
        </article>
    </div>
</section>

<?php include('footer.php'); ?>
<?php include('header.php'); ?>

<section class="section">
    <h2 class="section-title">Our Philosophy & Heritage</h2>
    <p class="section-subtitle">Understanding the true ethos behind REN Gorilla Expeditions.</p>
    
    <div style="max-width: 800px; margin: 0 auto; font-size: 1.1rem; line-height: 1.9;">
        <p style="margin-bottom: 1.5rem;">
            <strong>REN</strong> is the distinctive identity at the heart of our brand. For our clients and conservation partners, REN represents three non-negotiable principles: <strong>Respect, Explore, and Nature.</strong>
        </p>
        <p style="margin-bottom: 1.5rem;">
            These core ideas provide a simple but powerful framework: to respect the places and native communities we encounter, to explore the extraordinary landscapes and wildlife of Africa, and to protect the natural world that makes every single expedition possible.
        </p>
        <p style="margin-bottom: 1.5rem;">
            <strong>Gorilla</strong> represents our company's deep, ancestral connection to Uganda’s iconic mountain-gorilla experience and the broader world of wildlife conservation.
        </p>
        <p style="margin-bottom: 1.5rem;">
            Finally, <strong>Expeditions</strong> communicates something far deeper than ordinary travel. It signals purposeful, bespoke journeys, immersive discovery, high adventure, and meticulously planned luxury experiences.
        </p>
    </div>
</section>

<?php include('footer.php'); ?>
<?php include('header.php'); ?>

<section class="section">
    <h2 class="section-title">Curated Expeditions</h2>
    <p class="section-subtitle">Luxury itineraries tailored to offer intimate, respectful encounters with wild Africa.</p>

    <div class="gallery-grid">
        <article class="expedition-card">
            <img src="https://images.unsplash.com/photo-1516426122078-c23e76319801?auto=format&fit=crop&w=800&q=80" alt="Mountain Gorilla Trekking Experience">
            <div class="expedition-info">
                <h3>Ultimate Gorilla Trekking</h3>
                <p>Fly directly into Bwindi. Enjoy private luxury eco-lodge stays, custom permits, and personal trackers.</p>
                <br>
                <a href="<?php echo $whatsapp_link; ?>&text=Inquiry%20about%20Gorilla%20Trekking" class="btn-gold" target="_blank" rel="noopener noreferrer">Reserve via WhatsApp</a>
            </div>
        </article>

        <article class="expedition-card">
            <img src="https://images.unsplash.com/photo-1546182990-dffeafbe841d?auto=format&fit=crop&w=800&q=80" alt="Savanna Lion Safari">
            <div class="expedition-info">
                <h3>Big Cats & Savanna Safari</h3>
                <p>Private luxury game drives through Queen Elizabeth National Park tracking tree-climbing lions and leopards.</p>
                <br>
                <a href="<?php echo $whatsapp_link; ?>&text=Inquiry%20about%20Big%20Cats%20Safari" class="btn-gold" target="_blank" rel="noopener noreferrer">Reserve via WhatsApp</a>
            </div>
        </article>

        <article class="expedition-card">
            <img src="https://images.unsplash.com/photo-1557050543-4d5f4e07ef46?auto=format&fit=crop&w=800&q=80" alt="Elephant Herd Migration">
            <div class="expedition-info">
                <h3>The Great Wildlife Circuit</h3>
                <p>A comprehensive 10-day luxury journey connecting gorillas, chimpanzees, lions, and vast elephant herds.</p>
                <br>
                <a href="<?php echo $whatsapp_link; ?>&text=Inquiry%20about%20Great%20Wildlife%20Circuit" class="btn-gold" target="_blank" rel="noopener noreferrer">Reserve via WhatsApp</a>
            </div>
        </article>
    </div>
</section>

<?php include('footer.php'); ?>
<?php include('header.php'); ?>

<section class="section">
    <h2 class="section-title">Begin Your Journey</h2>
    <p class="section-subtitle">Our team is ready to design your custom African safari experience.</p>

    <div class="contact-container">
        <div>
            <h3 style="color: var(--color-gold-accent); font-family: var(--font-heading); margin-bottom: 1rem;">Direct Reservation Line</h3>
            <p style="margin-bottom: 1.5rem;">Speak directly with our safari specialists via WhatsApp for instant assistance and permit checks.</p>
            
            <a href="<?php echo $whatsapp_link; ?>" class="btn-gold" target="_blank" rel="noopener noreferrer" style="display: block; text-align: center; margin-bottom: 2rem;">Start WhatsApp Chat (+256 777990562)</a>

            <h3 style="color: var(--color-gold-accent); font-family: var(--font-heading); margin-bottom: 0.5rem;">Headquarters</h3>
            <p>Kampala, Uganda<br>East Africa</p>
        </div>

        <div>
            <form action="#" method="post" aria-label="Contact Form">
                <div class="form-group">
                    <label for="fullname">Full Name *</label>
                    <input type="text" id="fullname" name="fullname" required>
                </div>
                <div class="form-group">
                    <label for="email">Email Address *</label>
                    <input type="email" id="email" name="email" required>
                </div>
                <div class="form-group">
                    <label for="expedition">Expedition of Interest</label>
                    <input type="text" id="expedition" name="expedition" placeholder="e.g. Gorilla Trekking, Big Cats">
                </div>
                <div class="form-group">
                    <label for="message">Message / Travel Dates *</label>
                    <textarea id="message" name="message" rows="5" required></textarea>
                </div>
                <button type="submit" class="btn-gold" style="width:100%;">Submit Inquiry</button>
            </form>
        </div>
    </div>
</section>

<?php include('footer.php'); ?>
