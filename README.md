
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
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
      transition: all 0.3s ease;
      cursor: pointer;
      box-shadow: 0 0 10px rgba(0,172,193,0.4);
    }
    .button:hover, .action-btn:hover {
      transform: scale(1.07);
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
    ul { padding-left: 20px; }

    .popup {
      display: none;
      position: fixed;
      top: 30%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: #1a1a2e;
      color: white;
      padding: 20px;
      border-radius: 10px;
      z-index: 1000;
      box-shadow: 0 0 15px rgba(0,188,212,0.4);
      text-align: center;
    }
    .popup.active {
      display: block;
    }
    .popup img {
      margin-top: 15px;
      width: 160px;
    }
    .footer-buttons {
      text-align: center;
      margin: 50px 0;
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

  <!-- Sections -->
  <div id="rateSection" class="hidden-section">
    <h2>Service Rate List</h2>
    <h3>🎨 DESIGN SERVICES</h3>
    <ul>
      <li>Logo Design (Basic) – ₹799 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
      <li>Logo Design (Pro) – ₹1499 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
      <li>Landing Page Design – ₹2499 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
      <li>Full Website UI/UX – ₹4999 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
    </ul>

    <h3>📚 COURSES / PDF PACKS</h3>
    <ul>
      <li>Bulking Plan – ₹499 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
      <li>Cutting Plan – ₹499 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
      <li>Full Combo – ₹899 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
      <li>Freelance Like a Beast – ₹499 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
    </ul>

    <h3>🧠 CONSULTING & CUSTOMS</h3>
    <ul>
      <li>Brand Strategy Call – ₹699 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
      <li>Custom Bundle – Starts ₹999 <button class="button" onclick="buy('akashcharak726-2@okicici')">Buy</button></li>
    </ul>
    <p><strong>Note:</strong> Payments via UPI / GPay / Paytm / Razorpay / PhonePe</p>
  </div>

  <div id="formSection" class="hidden-section">
    <h2>Apply for a Role</h2>
    <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSeGxgOCqAzI-d8mpKss4QXefyI48pKEvjm5rFyBHxBMoZhDMw/viewform?embedded=true" width="100%" height="800" frameborder="0">Loading…</iframe>
  </div>

  <div id="aboutSection" class="hidden-section">
    <h2>About Yeagerson Services</h2>
    <p>We don’t just offer design or strategy — we deliver full-scale execution. From branding to dashboards, strategy, and digital ops — all custom, all fast.</p>
    <p><strong>Founded by John Yeagerson</strong>, a multi-skilled creator and builder. Not your average “agency” — this is a digital powerhouse built from hustle.</p>
    <blockquote><strong>"Others outsource. We execute."<br>"Others give you designs. We give you systems that sell."</strong></blockquote>
    <h3>💼 What We Stand For</h3>
    <ul>
      <li>Execution over Excuses</li>
      <li>Clarity over Chaos</li>
      <li>Design that Converts</li>
      <li>Service with Soul</li>
    </ul>
    <h3>🧠 What We Do Best</h3>
    <ul>
      <li>Branding, UI/UX, HTML/CSS Sites</li>
      <li>Presentation Decks, Dashboards, Funnels</li>
      <li>Business Strategy, Monthly Retainers</li>
    </ul>
    <p><strong>📍 Based in India – Serving Clients Worldwide 🌍</strong></p>
  </div>

  <!-- Buy Popup -->
  <div id="popup" class="popup">
    <p>Scan to Pay (UPI)</p>
    <img src="https://upload.wikimedia.org/wikipedia/commons/7/70/QRCode-2.png" alt="UPI QR">
    <p>Redirecting after payment...</p>
  </div>

  <div class="footer-buttons">
    <button class="action-btn" onclick="window.location.href='mailto:adityacharak14@gmail.com'">📧 Email</button>
    <button class="action-btn" onclick="window.open('https://www.instagram.com/son__yeager_', '_blank')">📸 Instagram</button>
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

    function buy(upiId) {
      const popup = document.getElementById('popup');
      popup.classList.add('active');
      setTimeout(() => {
        popup.classList.remove('active');
        window.location.href = "https://drive.google.com";
      }, 4000);
    }
  </script>
</body>
</html>
