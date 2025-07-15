<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Yeagerson Services</title>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Outfit', sans-serif;
      color: #f2f2f2;
      background: radial-gradient(ellipse at bottom, #1b2735 0%, #090a0f 100%);
      overflow-x: hidden;
    }

    header {
      background: linear-gradient(135deg, #121212, #1f1f1f);
      text-align: center;
      padding: 60px 20px 40px;
      color: white;
      position: relative;
      overflow: hidden;
    }

    .logo {
      font-size: 42px;
      font-weight: 700;
      position: relative;
      z-index: 1;
    }

    .subtext {
      font-size: 20px;
      opacity: 0.95;
      z-index: 1;
      position: relative;
    }

    .shine {
      content: '';
      position: absolute;
      top: 0;
      left: -75%;
      width: 50%;
      height: 100%;
      background: linear-gradient(120deg, transparent, rgba(255,255,255,0.1), transparent);
      transform: skewX(-25deg);
      animation: shine 4s infinite;
      z-index: 0;
    }

    @keyframes shine {
      0% { left: -75%; }
      100% { left: 125%; }
    }

    .button, .action-btn {
      display: inline-block;
      background: linear-gradient(135deg, #00acc1, #007c91);
      color: white;
      padding: 12px 24px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      font-weight: 600;
      text-decoration: none;
      cursor: pointer;
      box-shadow: 0 0 10px rgba(0,172,193,0.4);
      transition: all 0.3s ease;
    }

    .button:hover, .action-btn:hover {
      transform: scale(1.05);
    }

    .loader {
      display: none;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }

    .loader span {
      display: inline-block;
      width: 30px;
      height: 30px;
      border: 4px solid #00acc1;
      border-top: 4px solid transparent;
      border-radius: 50%;
      animation: spin 1s linear infinite;
    }

    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    .hidden-section {
      display: none;
      background: rgba(255,255,255,0.02);
      padding: 30px;
      margin: 30px auto;
      max-width: 900px;
      border-radius: 12px;
      line-height: 1.7;
    }

    h2, h3 {
      color: #00acc1;
    }

    .rate-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin: 8px 0;
      gap: 20px;
    }

    .rate-item span {
      flex: 1;
    }

    ul {
      padding-left: 20px;
    }

    .footer {
      text-align: center;
      margin: 40px 0;
    }

    .footer .contact-btn {
      background: none;
      border: 2px solid #00acc1;
      color: #00acc1;
      padding: 10px 16px;
      margin: 10px;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }

    .footer .contact-btn:hover {
      background: #00acc1;
      color: black;
    }
  </style>
</head>
<body>

  <header>
    <div class="logo">YEAGERSON SERVICES</div>
    <div class="shine"></div>
    <p class="subtext">Design. Fitness. Digital Strategy — Professional. Tactical. Real.</p>
    <div>
      <button class="action-btn" onclick="revealSection('rateLoader', 'rateSection')">💸 View Rate List</button>
      <button class="action-btn" onclick="revealSection('formLoader', 'formSection')">📄 Apply</button>
      <button class="action-btn" onclick="revealSection('aboutLoader', 'aboutSection')">📌 About Us</button>
    </div>
  </header>

  <!-- Loaders -->
  <div id="rateLoader" class="loader"><span></span></div>
  <div id="formLoader" class="loader"><span></span></div>
  <div id="aboutLoader" class="loader"><span></span></div>

  <!-- Rate List Section -->
  <div id="rateSection" class="hidden-section">
    <h2>Service Rate List</h2>

    <h3>🎨 DESIGN SERVICES</h3>
    <div class="rate-item"><span>Logo Design (Basic): ₹799</span><button class="button">Buy</button></div>
    <div class="rate-item"><span>Logo Design (Pro): ₹1499</span><button class="button">Buy</button></div>
    <div class="rate-item"><span>Landing Page Design: ₹2499</span><button class="button">Buy</button></div>
    <div class="rate-item"><span>Full Website UI/UX: ₹4999</span><button class="button">Buy</button></div>

    <h3>📚 COURSES / PDF PACKS</h3>
    <div class="rate-item"><span>Bulking Plan: ₹499</span><button class="button">Buy</button></div>
    <div class="rate-item"><span>Cutting Plan: ₹499</span><button class="button">Buy</button></div>
    <div class="rate-item"><span>Full Combo (Bulk + Cut): ₹899</span><button class="button">Buy</button></div>
    <div class="rate-item"><span>Freelance Like a Beast: ₹499</span><button class="button">Buy</button></div>

    <h3>🧠 CONSULTING & CUSTOMS</h3>
    <div class="rate-item"><span>Strategy Call (30 min): ₹699</span><button class="button">Buy</button></div>
    <div class="rate-item"><span>Custom Bundle: Starts ₹999</span><button class="button">Buy</button></div>

    <p><strong>Notes:</strong> Payments accepted via UPI / GPay / Paytm / Razorpay / PhonePe.<br>Delivery via Email, Drive or WhatsApp.<br>1 Free revision. ₹299 per extra. Urgent delivery: +₹499</p>
  </div>

  <!-- Form Section -->
  <div id="formSection" class="hidden-section">
    <h2>Apply for a Role</h2>
    <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSeGxgOCqAzI-d8mpKss4QXefyI48pKEvjm5rFyBHxBMoZhDMw/viewform?embedded=true" width="100%" height="800" frameborder="0">Loading…</iframe>
  </div>

  <!-- About Us Section -->
  <div id="aboutSection" class="hidden-section">
    <h2>About Yeagerson Services</h2>
    <p>At Yeagerson Services, we don’t just offer design or strategy — we deliver full-scale execution. From stunning branding to razor-sharp websites, business-ready presentations, project dashboards, growth strategies, UPI-ready funnels, and ongoing digital management — we do it all in-house, all custom, all fast.</p>
    <p>Founded by John Yeagerson, a multi-skilled creator, strategist, and builder — this isn’t your typical “agency.” It’s a growing digital powerhouse born out of hustle, purpose, and pure grind.</p>
    <blockquote>
      <p><strong>"Others outsource. We execute."<br>"Others give you designs. We give you systems that sell."</strong></p>
    </blockquote>
    <h3>💼 What We Stand For</h3>
    <ul>
      <li>Execution over Excuses</li>
      <li>Clarity over Chaos</li>
      <li>Design that Converts</li>
      <li>Service with Soul</li>
    </ul>
    <h3>🧠 What We Do Best</h3>
    <ul>
      <li>Branding & Logo Design</li>
      <li>Website Design (UI/UX, HTML/CSS)</li>
      <li>Presentation Decks, Dashboards, Funnels</li>
      <li>Business Strategy, Monthly Retainers</li>
    </ul>
    <p><strong>📍 Based in India – Serving Clients Worldwide 🌍</strong></p>
  </div>

  <!-- Contact Footer -->
  <div class="footer">
    <button class="contact-btn" onclick="window.location.href='mailto:adityacharak14@gmail.com'">Email</button>
    <button class="contact-btn" onclick="window.open('https://www.instagram.com/son__yeager_', '_blank')">Instagram</button>
  </div>

  <script>
    function revealSection(loaderId, sectionId) {
      const loader = document.getElementById(loaderId);
      const section = document.getElementById(sectionId);

      loader.style.display = "flex";

      setTimeout(() => {
        loader.style.display = "none";
        section.style.display = "block";
        section.scrollIntoView({ behavior: "smooth" });
      }, 2000);
    }
  </script>
</body>
</html>
