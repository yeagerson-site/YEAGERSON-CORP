<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Yeagerson Services</title>
  <meta name="description" content="Design. Fitness. Digital Strategy. Full-service execution by Yeagerson Services.">
  <meta property="og:title" content="Yeagerson Services">
  <meta property="og:description" content="Design. Fitness. Digital Strategy. Execute faster with Yeagerson.">
  <meta property="og:image" content="https://yourdomain.com/og-image.jpg">
  <meta property="og:type" content="website">
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
    .shine {
      content: '';
      position: absolute;
      top: 0;
      left: -75%;
      width: 50%;
      height: 100%;
      background: linear-gradient(120deg, transparent, rgba(255,255,255,0.2), transparent);
      transform: skewX(-25deg);
      animation: shine 4s infinite;
      z-index: 0;
    }
    @keyframes shine {
      0% { left: -75%; }
      100% { left: 125%; }
    }
    .subtext {
      font-size: 20px;
      opacity: 0.95;
      z-index: 1;
      position: relative;
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
      transform: scale(1.07);
    }
    .hidden-section {
      display: none;
      background: rgba(255,255,255,0.02);
      padding: 30px;
      margin: 30px auto;
      max-width: 900px;
      border-radius: 12px;
      line-height: 1.7;
      animation: fadeIn 0.8s ease-in-out;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    h2, h3 { color: #00acc1; }
    ul { padding-left: 20px; }
    #scrollTop {
      position: fixed;
      bottom: 30px;
      right: 20px;
      background: #00acc1;
      color: white;
      padding: 10px 14px;
      border-radius: 50%;
      cursor: pointer;
      font-size: 18px;
      display: none;
    }
    .footer-buttons { text-align: center; margin: 50px 0; }
  </style>
</head>
<body>

  <header>
    <div class="logo">YEAGERSON SERVICES</div>
    <div class="shine"></div>
    <p class="subtext">Design. Fitness. Digital Strategy — Professional. Tactical. Real.</p>
    <div>
      <button class="action-btn" onclick="toggleSection('rateSection')">💸 View Rate List</button>
      <button class="action-btn" onclick="toggleSection('formSection')">📄 Apply</button>
      <button class="action-btn" onclick="toggleSection('aboutSection')">📌 About Us</button>
    </div>
  </header>

  <!-- 💸 Rate List Section -->
  <div id="rateSection" class="hidden-section">
    <h2>Service Rate List</h2>

    <h3>🎨 DESIGN SERVICES</h3>
    <ul>
      <li>Logo Design (Basic) – ₹799</li>
      <li>Logo Design (Pro) – ₹1499</li>
      <li>Landing Page Design – ₹2499</li>
      <li>Full Website UI/UX – ₹4999</li>
    </ul>

    <h3>📚 COURSES / PDF PACKS</h3>
    <ul>
      <li>Bulking Plan – ₹499</li>
      <li>Cutting Plan – ₹499</li>
      <li>Full Combo (Bulk + Cut) – ₹899</li>
      <li>Freelance Like a Beast – ₹499</li>
    </ul>

    <h3>🧠 CONSULTING & CUSTOMS</h3>
    <ul>
      <li>Brand Strategy Call (30 min) – ₹699</li>
      <li>Custom Bundle – Starts ₹999</li>
    </ul>

    <p><strong>Note:</strong> Payments via UPI / GPay / Paytm / Razorpay / PhonePe. Contact us to proceed.</p>
  </div>

  <!-- 📄 Job Application Form -->
  <div id="formSection" class="hidden-section">
    <h2>Apply for a Role</h2>
    <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSeGxgOCqAzI-d8mpKss4QXefyI48pKEvjm5rFyBHxBMoZhDMw/viewform?embedded=true" width="100%" height="800" frameborder="0">Loading…</iframe>
  </div>

  <!-- 📌 About Us -->
  <div id="aboutSection" class="hidden-section">
    <h2>About Yeagerson Services</h2>
    <p>We don’t just offer services. We build complete, outcome-focused solutions. Founded by John Yeagerson, this is where execution meets bold clarity. From design to digital to fitness – we’ve got your back.</p>
    <p><strong>📍 Based in India – Serving Clients Worldwide 🌍</strong></p>
  </div>

  <!-- 🔗 Contact Buttons -->
  <div class="footer-buttons">
    <button class="action-btn" onclick="window.open('mailto:adityacharak14@gmail.com')">📧 Email</button>
    <button class="action-btn" onclick="window.open('https://www.instagram.com/son__yeager_', '_blank')">📸 Instagram</button>
  </div>

  <!-- 🔝 Scroll-to-top -->
  <div id="scrollTop" onclick="window.scrollTo({ top: 0, behavior: 'smooth' })">↑</div>

  <!-- 🚀 Scripts -->
  <script>
    function toggleSection(id) {
      const section = document.getElementById(id);
      section.style.display = (section.style.display === "block") ? "none" : "block";
      section.scrollIntoView({ behavior: "smooth" });
    }

    window.onscroll = () => {
      document.getElementById("scrollTop").style.display = window.scrollY > 300 ? "block" : "none";
    };
  </script>
</body>
</html>


