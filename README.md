<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>URBAN CHARM</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600&family=Inter:wght@300;500&display=swap" rel="stylesheet">
  <style>
    * {margin: 0; padding: 0; box-sizing: border-box;}
    body {
      line-height: 1.6;
      color: #e5e5e5;
      font-family: 'Inter', sans-serif;
      background: linear-gradient(135deg, #000000, #2c2c2c);
    }
    
    /* Header */
    header {
      background: linear-gradient(90deg, #0d0d0d, #1a1a1a);
      color: #fff;
      padding: 1rem 2rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: fixed;
      top: 0; width: 100%;
      z-index: 1000;
      box-shadow: 0 4px 12px rgba(0,0,0,0.8);
    }
    header .logo-container {
      display: flex;
      align-items: center;
      gap: 12px;
    }
    header img {
      height: 55px;
      width: auto;
      filter: drop-shadow(0 0 6px rgba(212,175,55,0.6));
    }
    header h1 {
      font-size: 1.6rem;
      color: #d4af37;
      font-family: 'Playfair Display', serif;
      font-weight: 600;
      letter-spacing: 1.5px;
    }

    nav {margin-top: 0.5rem;}
    nav a {
      color: #fff;
      margin: 0 12px;
      text-decoration: none;
      font-weight: 500;
      font-family: 'Inter', sans-serif;
      transition: color 0.3s ease;
    }
    nav a:hover {color: #d4af37;}

    .menu-toggle {display: none; font-size: 1.8rem; cursor: pointer; color: #fff;}

    /* Hero */
    .hero {
      display: flex; flex-direction: column; align-items: center; justify-content: center;
      padding: 7rem 2rem 4rem;
      background: linear-gradient(135deg, #1a1a1a, #2b2b2b);
      text-align: center;
      border-bottom: 1px solid #333;
    }
    .hero h2 {
      font-size: 2.2rem;
      margin-bottom: 1rem;
      font-family: 'Playfair Display', serif;
      color: #d4af37;
      text-shadow: 0 0 10px rgba(212,175,55,0.5);
    }
    .hero p {
      max-width: 650px;
      margin-bottom: 1.5rem;
      font-family: 'Inter', sans-serif;
      color: #ccc;
    }
    .hero button {
      padding: 0.8rem 1.8rem;
      background: #d4af37;
      border: none;
      color: #000;
      border-radius: 10px;
      cursor: pointer;
      font-size: 1.05rem;
      font-family: 'Inter', sans-serif;
      font-weight: 600;
      transition: all 0.3s ease;
      box-shadow: 0 4px 10px rgba(0,0,0,0.6);
    }
    .hero button:hover {
      background: #bfa036;
      transform: scale(1.05);
      box-shadow: 0 6px 14px rgba(0,0,0,0.8);
    }

    /* Sections */
    section {padding: 5rem 2rem 3rem; text-align: center;}
    section h2 {
      font-family: 'Playfair Display', serif;
      color: #d4af37;
      margin-bottom: 1rem;
      font-size: 1.8rem;
      letter-spacing: 1px;
    }

    /* Services */
    .services {display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1.8rem;}
    .card {
      background: #1e1e1e;
      padding: 2rem;
      border-radius: 14px;
      box-shadow: 0 6px 14px rgba(0,0,0,0.7);
      border: 1px solid #333;
      font-family: 'Inter', sans-serif;
      transition: transform 0.3s ease;
    }
    .card img {width: 100%; height: 190px; object-fit: cover; border-radius: 10px; margin-bottom: 1rem;}
    .card h3 {color: #d4af37; margin-bottom: 0.5rem;}
    .card p {color: #bbb;}
    .card:hover {transform: translateY(-8px);}

    /* Footer */
    footer {
      background: linear-gradient(90deg, #0d0d0d, #1a1a1a);
      color: #ccc;
      padding: 2rem;
      text-align: center;
      margin-top: 2rem;
      font-family: 'Inter', sans-serif;
      position: relative;
      border-top: 1px solid #333;
    }
    footer img {
      height: 65px;
      width: auto;
      margin-bottom: 12px;
      opacity: 0.9;
      filter: drop-shadow(0 0 8px rgba(212,175,55,0.5));
    }
    footer p {color: #888;}

    /* Mobile Menu */
    @media (max-width: 768px) {
      nav {display: none; flex-direction: column; background: #111; padding: 1rem; border-radius: 8px;}
      nav a {display: block; margin: 10px 0;}
      .menu-toggle {display: block;}
      nav.active {display: flex;}
    }
  </style>
</head>
<body>
  <header>
    <div class="logo-container">
      <img src="IMG_6525.PNG" alt="Urban Charm Logo">
      <h1>URBAN CHARM</h1>
    </div>
    <div class="menu-toggle" onclick="toggleMenu()">☰</div>
    <nav id="nav-menu">
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Welcome to URBAN CHARM</h2>
    <p>Where sophistication meets everyday style — discover timeless fashion and accessories crafted to bring out your unique charm.</p>
    <button onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'})">Get in Touch</button>
  </section>

  <section id="about">
    <h2>About Us</h2>
    <p style="max-width: 600px; margin: 1rem auto; font-family: 'Inter', sans-serif; color:#ccc;">
      At URBAN CHARM, we believe fashion should be effortless, elegant, and expressive. 
      Our collections blend contemporary urban trends with classic sophistication, 
      offering versatile clothing and accessories designed for every occasion. 
      With a focus on premium quality and refined details, URBAN CHARM ensures that 
      every piece makes you feel confident, stylish, and uniquely you.
    </p>
  </section>

  <section id="services">
    <h2>Our Services</h2>
    <div class="services">
      <div class="card">
        <img src="https://i.pinimg.com/1200x/57/16/02/5716025f2a0f3c908bd09f688de0430b.jpg" alt="Clothing">
        <h3>CLOTHING</h3>
        <p>Explore our premium clothing line, blending comfort and luxury to suit every occasion.</p>
      </div>
      <div class="card">
        <img src="https://i.pinimg.com/736x/8a/0a/87/8a0a871ee9bb2a4f88a518cf172e1101.jpg" alt="Accessories">
        <h3>ACCESSORIES</h3>
        <p>Discover statement accessories that elevate your style with elegance and detail.</p>
      </div>
      <div class="card">
        <img src="https://i.pinimg.com/736x/ac/c6/4c/acc64c361d32110a887361bf99f57085.jpg" alt="Lifestyle">
        <h3>LIFESTYLE</h3>
        <p>Curated lifestyle essentials to bring sophistication and charm into your daily life.</p>
      </div>
    </div>
  </section>

  <section id="contact">
    <h2>Contact Us</h2>
    <p style="color:#ccc;">Email: yoursurbancharm@gmail.com | Phone: +91-8368035400</p>
  </section>

  <footer>
    <img src="IMG_6525.PNG" alt="Urban Charm Footer Logo">
    <p>&copy; 2025 URBAN CHARM. All rights reserved.</p>
  </footer>

  <script>
    function toggleMenu() {
      document.getElementById("nav-menu").classList.toggle("active");
    }
  </script>
</body>
</html>
