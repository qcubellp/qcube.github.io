<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Q Cube LLP | CX, CPQ & Services</title>
  <meta name="description" content="Q Cube LLP - Software & IT Consulting in CX, CPQ and Digital Services." />

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#ffffff;
      --text:#0b0b0b;
      --muted:#3a3a3a;
      --line:#111111;
      --shadow:6px 6px 0px #000;
      --radius:18px;
    }

    *{margin:0;padding:0;box-sizing:border-box;}
    html{scroll-behavior:smooth;}
    body{
      font-family:"Space Grotesk",sans-serif;
      background:var(--bg);
      color:var(--text);
      overflow-x:hidden;
    }

    .container{width:min(1150px,92%);margin:0 auto;}

    /* Comic dotted background */
    .comic-bg{
      position:fixed;
      inset:0;
      background:
        radial-gradient(circle at 20% 30%, rgba(0,0,0,0.06) 0 2px, transparent 3px),
        radial-gradient(circle at 70% 60%, rgba(0,0,0,0.06) 0 2px, transparent 3px),
        radial-gradient(circle at 40% 80%, rgba(0,0,0,0.06) 0 2px, transparent 3px);
      background-size:60px 60px;
      z-index:-1;
      opacity:0.85;
    }

    /* Header */
    header{
      position:sticky;
      top:0;
      z-index:50;
      background:rgba(255,255,255,0.92);
      backdrop-filter:blur(10px);
      border-bottom:2px solid var(--line);
    }

    .nav-wrap{
      display:flex;
      align-items:center;
      justify-content:space-between;
      padding:14px 0;
      position:relative;
    }

    .logo{
      display:flex;
      align-items:center;
      gap:10px;
      text-decoration:none;
      color:var(--text);
    }

    .logo-mark{
      width:42px;height:42px;
      display:grid;place-items:center;
      border:2px solid var(--line);
      border-radius:14px;
      box-shadow:var(--shadow);
      font-weight:800;
      background:#fff;
    }

    .logo-text{
      font-weight:800;
      font-size:18px;
    }

    .menu-btn{
      display:none;
      border:2px solid var(--line);
      background:#fff;
      padding:8px 12px;
      border-radius:12px;
      box-shadow:var(--shadow);
      font-weight:800;
      cursor:pointer;
    }

    nav{
      display:flex;
      align-items:center;
      gap:18px;
    }

    nav a{
      text-decoration:none;
      color:var(--text);
      font-weight:700;
      padding:8px 10px;
      border-radius:12px;
    }

    nav a:hover,
    nav a.active{
      background:#000;
      color:#fff;
    }

    /* Buttons */
    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      padding:12px 18px;
      border-radius:14px;
      font-weight:800;
      text-decoration:none;
      border:2px solid var(--line);
      box-shadow:var(--shadow);
      transition:transform 0.15s ease;
      white-space:nowrap;
    }

    .btn:active{transform:translate(3px,3px);box-shadow:3px 3px 0 #000;}
    .btn-primary{background:#000;color:#fff;}
    .btn-outline{background:#fff;color:#000;}
    .btn-full{width:100%;}

    /* Sections */
    section{padding:90px 0;}
    section.alt{
      background:#f7f7f7;
      border-top:2px solid var(--line);
      border-bottom:2px solid var(--line);
    }

    .section-head{margin-bottom:35px;}
    .section-head h2{
      font-size:clamp(26px,4vw,42px);
      letter-spacing:-1px;
    }
    .section-head p{
      margin-top:10px;
      color:var(--muted);
      max-width:760px;
    }

    /* Hero */
    .hero{padding-top:70px;}
    .hero-grid{
      display:grid;
      grid-template-columns:1.2fr 0.9fr;
      gap:40px;
      align-items:center;
    }

    .badge{
      display:inline-block;
      border:2px solid var(--line);
      padding:8px 14px;
      border-radius:999px;
      background:#fff;
      box-shadow:var(--shadow);
      font-weight:800;
      margin-bottom:16px;
    }

    .hero-title{
      font-size:clamp(34px,5vw,56px);
      line-height:1.05;
      letter-spacing:-2px;
    }

    .underline{
      position:relative;
      display:inline-block;
    }
    .underline::after{
      content:"";
      position:absolute;
      left:0;
      bottom:-6px;
      width:100%;
      height:10px;
      background:#000;
      opacity:0.12;
      border-radius:999px;
    }

    .comic-burst{
      display:inline-block;
      margin-left:10px;
      font-size:16px;
      padding:6px 10px;
      border:2px solid var(--line);
      border-radius:999px;
      box-shadow:var(--shadow);
      transform:rotate(-6deg);
      background:#fff;
    }

    .hero-subtitle{
      margin-top:18px;
      font-size:18px;
      color:var(--muted);
      max-width:600px;
    }

    .hero-cta{
      display:flex;
      gap:14px;
      flex-wrap:wrap;
      margin-top:20px;
    }

    .stats{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:14px;
      margin-top:26px;
    }

    .stat-card{
      background:#fff;
      border:2px solid var(--line);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
      padding:16px;
    }
    .stat-card h3{font-size:22px;}
    .stat-card p{color:var(--muted);font-size:14px;}

    /* Right card */
    .comic-card{
      background:#fff;
      border:2px solid var(--line);
      border-radius:22px;
      box-shadow:var(--shadow);
      overflow:hidden;
    }

    .comic-card-top{
      display:flex;
      gap:8px;
      padding:12px;
      border-bottom:2px solid var(--line);
      background:#f7f7f7;
    }

    .dot{
      width:12px;height:12px;
      border:2px solid #000;
      border-radius:999px;
    }

    .comic-card-body{padding:22px;}
    .comic-card-body h3{font-size:24px;}
    .comic-card-body p{color:var(--muted);margin-top:10px;}

    .checklist{margin-top:14px;padding-left:18px;}
    .checklist li{margin:8px 0;font-weight:700;}

    .comic-strip{
      margin-top:16px;
      display:flex;
      gap:10px;
      flex-wrap:wrap;
    }
    .comic-strip span{
      padding:8px 12px;
      border:2px solid var(--line);
      border-radius:999px;
      font-weight:900;
      background:#fff;
      box-shadow:4px 4px 0 #000;
    }

    .floating-note{
      margin-top:14px;
      border:2px dashed #000;
      border-radius:18px;
      padding:12px 14px;
      background:#fff;
      box-shadow:4px 4px 0 #000;
      font-weight:700;
    }

    /* Cards Grid */
    .grid-3{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:18px;
    }

    .card{
      background:#fff;
      border:2px solid var(--line);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
      padding:20px;
    }

    .card h3{font-size:20px;margin-bottom:8px;}
    .card p{color:var(--muted);}

    .tag-row{
      margin-top:14px;
      display:flex;
      gap:10px;
      flex-wrap:wrap;
    }

    .tag{
      border:2px solid var(--line);
      border-radius:999px;
      padding:6px 10px;
      font-weight:900;
      background:#fff;
    }

    /* Projects */
    .projects-grid{
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:18px;
    }

    .project-meta{
      margin-top:14px;
      display:flex;
      justify-content:space-between;
      color:var(--muted);
      font-size:13px;
      font-weight:700;
    }

    /* Contact */
    .contact-grid{
      display:grid;
      grid-template-columns:0.9fr 1.1fr;
      gap:18px;
    }

    .comic-tip{
      margin-top:14px;
      border:2px solid var(--line);
      border-radius:14px;
      padding:12px;
      background:#f7f7f7;
      font-weight:800;
    }

    .form-row{
      display:flex;
      flex-direction:column;
      gap:8px;
      margin-bottom:14px;
    }

    label{font-weight:900;}
    input, textarea{
      border:2px solid var(--line);
      border-radius:14px;
      padding:12px 14px;
      outline:none;
      font-size:15px;
      background:#fff;
    }

    input:focus, textarea:focus{
      box-shadow:0 0 0 4px rgba(0,0,0,0.12);
    }

    .success{
      display:none;
      margin-top:12px;
      font-weight:900;
    }

    /* Footer */
    footer{
      border-top:2px solid var(--line);
      padding:30px 0;
      background:#fff;
    }

    .footer-grid{
      display:grid;
      grid-template-columns:1fr 1fr 1fr;
      gap:16px;
      align-items:center;
    }

    .footer-links{
      display:flex;
      gap:14px;
      flex-wrap:wrap;
      justify-content:center;
    }

    .footer-links a{
      color:#000;
      text-decoration:none;
      font-weight:900;
    }

    .footer-copy{
      text-align:right;
      color:var(--muted);
      font-weight:700;
    }

    /* Fade animation */
    .fade-in{
      opacity:0;
      transform:translateY(18px);
      transition:opacity 0.6s ease, transform 0.6s ease;
    }
    .fade-in.show{
      opacity:1;
      transform:translateY(0);
    }

    /* Responsive */
    @media (max-width: 900px){
      .hero-grid{grid-template-columns:1fr;}
      .grid-3{grid-template-columns:1fr;}
      .projects-grid{grid-template-columns:1fr;}
      .contact-grid{grid-template-columns:1fr;}
      .footer-grid{grid-template-columns:1fr;text-align:center;}
      .footer-copy{text-align:center;}

      .menu-btn{display:block;}

      nav{
        position:absolute;
        top:70px;
        left:4%;
        right:4%;
        background:#fff;
        border:2px solid var(--line);
        border-radius:18px;
        box-shadow:var(--shadow);
        padding:14px;
        display:none;
        flex-direction:column;
        align-items:stretch;
      }
      nav.open{display:flex;}
    }
  </style>
</head>

<body>
  <div class="comic-bg" aria-hidden="true"></div>

  <header>
    <div class="container nav-wrap">
      <a class="logo" href="#home">
        <span class="logo-mark">Q</span>
        <span class="logo-text">Cube LLP</span>
      </a>

      <button class="menu-btn" id="menuBtn" aria-label="Open Menu">☰</button>

      <nav id="nav">
        <a href="#home" class="active nav-link">Home</a>
        <a href="#about" class="nav-link">About</a>
        <a href="#services" class="nav-link">Services</a>
        <a href="#projects" class="nav-link">Projects</a>
        <a href="#contact" class="nav-link">Contact</a>
        <a href="#contact" class="btn btn-primary">Get Started</a>
      </nav>
    </div>
  </header>

  <main>
    <!-- HERO -->
    <section id="home" class="hero">
      <div class="container hero-grid">
        <div class="fade-in">
          <div class="badge">⚡ Future-ready Consulting • CX • CPQ • Services</div>

          <h1 class="hero-title">
            Transforming <span class="underline">CX</span>, <span class="underline">CPQ</span> & Digital Services
            <span class="comic-burst">WOW!</span>
          </h1>

          <p class="hero-subtitle">
            Q Cube LLP helps businesses streamline customer journeys, automate quoting,
            and deliver scalable digital solutions with enterprise-grade reliability.
          </p>

          <div class="hero-cta">
            <a href="#services" class="btn btn-primary">Explore Services</a>
            <a href="#projects" class="btn btn-outline">View Projects</a>
          </div>

          <div class="stats">
            <div class="stat-card">
              <h3>CX</h3>
              <p>Customer Experience</p>
            </div>
            <div class="stat-card">
              <h3>CPQ</h3>
              <p>Configure • Price • Quote</p>
            </div>
            <div class="stat-card">
              <h3>24/7</h3>
              <p>Support & Services</p>
            </div>
          </div>
        </div>

        <div class="fade-in">
          <div class="comic-card">
            <div class="comic-card-top">
              <span class="dot"></span>
              <span class="dot"></span>
              <span class="dot"></span>
            </div>

            <div class="comic-card-body">
              <h3>Q Cube LLP</h3>
              <p>Enterprise-grade consulting in:</p>
              <ul class="checklist">
                <li>✔ CX Strategy & Implementation</li>
                <li>✔ CPQ Configuration & Optimization</li>
                <li>✔ Digital Services & Integration</li>
              </ul>

              <div class="comic-strip">
                <span>FAST</span>
                <span>SMART</span>
                <span>SECURE</span>
              </div>
            </div>
          </div>

          <div class="floating-note">
            <strong>Comic Mode:</strong> Black & White + Bold UI ✨
          </div>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <div class="container">
        <div class="section-head fade-in">
          <h2>About Us</h2>
          <p>
            Q Cube LLP is a software & IT consulting company delivering modern,
            scalable solutions with a business-first approach.
          </p>
        </div>

        <div class="grid-3 fade-in">
          <div class="card">
            <h3>🎯 Mission</h3>
            <p>Deliver reliable CX and CPQ solutions that improve speed, accuracy, and customer trust.</p>
          </div>
          <div class="card">
            <h3>🧠 Expertise</h3>
            <p>Strong consulting experience in enterprise systems, integrations, and performance optimization.</p>
          </div>
          <div class="card">
            <h3>🤝 Partnership</h3>
            <p>We work as your extended team, ensuring smooth delivery, testing, and go-live success.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- SERVICES -->
    <section id="services" class="alt">
      <div class="container">
        <div class="section-head fade-in">
          <h2>Services</h2>
          <p>Comic style outside, enterprise quality inside 😄</p>
        </div>

        <div class="grid-3 fade-in">
          <div class="card">
            <h3>CX Solutions</h3>
            <p>Improve customer journeys, touchpoints, and engagement with smart CX transformation.</p>
            <div class="tag-row">
              <span class="tag">Journey</span>
              <span class="tag">Support</span>
              <span class="tag">Automation</span>
            </div>
          </div>

          <div class="card">
            <h3>CPQ Implementations</h3>
            <p>Build accurate quotes faster with robust CPQ configuration, rules, and approvals.</p>
            <div class="tag-row">
              <span class="tag">Pricing</span>
              <span class="tag">Rules</span>
              <span class="tag">Workflow</span>
            </div>
          </div>

          <div class="card">
            <h3>Digital & IT Services</h3>
            <p>Integration, support, upgrades, and optimization for stable, scalable delivery.</p>
            <div class="tag-row">
              <span class="tag">Integration</span>
              <span class="tag">Support</span>
              <span class="tag">Cloud</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects">
      <div class="container">
        <div class="section-head fade-in">
          <h2>Projects / Case Studies</h2>
          <p>Sample portfolio to represent Q Cube LLP delivery capabilities</p>
        </div>

        <div class="projects-grid fade-in">
          <div class="card">
            <h3>CPQ Quote Automation</h3>
            <p>Reduced quote turnaround time with streamlined pricing logic and approvals.</p>
            <div class="project-meta">
              <span>Type: CPQ</span>
              <span>Impact: Faster Quotes</span>
            </div>
          </div>

          <div class="card">
            <h3>CX Process Enhancement</h3>
            <p>Improved customer experience with better service flows and automation.</p>
            <div class="project-meta">
              <span>Type: CX</span>
              <span>Impact: Better NPS</span>
            </div>
          </div>

          <div class="card">
            <h3>Support & Optimization</h3>
            <p>Performance tuning and continuous support for enterprise systems.</p>
            <div class="project-meta">
              <span>Type: Services</span>
              <span>Impact: Stability</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="alt">
      <div class="container">
        <div class="section-head fade-in">
          <h2>Contact Us</h2>
          <p>Let’s build something powerful together 🚀</p>
        </div>

        <div class="contact-grid fade-in">
          <div class="card">
            <h3>Reach Us</h3>
            <p><strong>Email:</strong> info@qcube.com</p>
            <p><strong>Location:</strong> India / Global Delivery</p>
            <p><strong>Services:</strong> CX • CPQ • Digital Services</p>

            <div class="comic-tip">💡 Tip: We respond within 24 hours.</div>
          </div>

          <form class="card" id="contactForm">
            <div class="form-row">
              <label>Name</label>
              <input type="text" id="name" placeholder="Enter your name" required />
            </div>

            <div class="form-row">
              <label>Email</label>
              <input type="email" id="email" placeholder="Enter your email" required />
            </div>

            <div class="form-row">
              <label>Message</label>
              <textarea id="message" rows="4" placeholder="Tell us about your requirement..." required></textarea>
            </div>

            <button type="submit" class="btn btn-primary btn-full">Send Message</button>
            <p class="success" id="successMsg">✅ Message sent successfully! We will contact you soon.</p>
          </form>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-grid">
      <div>
        <h3>Q Cube LLP</h3>
        <p style="color:var(--muted);font-weight:700;">Modern Consulting for CX, CPQ & Digital Services.</p>
      </div>

      <div class="footer-links">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </div>

      <div class="footer-copy">
        <p>© <span id="year"></span> Q Cube LLP. All rights reserved.</p>
      </div>
    </div>
  </footer>

  <script>
    // Mobile menu toggle
    const menuBtn = document.getElementById("menuBtn");
    const nav = document.getElementById("nav");

    menuBtn.addEventListener("click", () => {
      nav.classList.toggle("open");
    });

    // Close menu on click (mobile)
    document.querySelectorAll("nav a").forEach(link => {
      link.addEventListener("click", () => nav.classList.remove("open"));
    });

    // Active nav link on scroll
    const sections = document.querySelectorAll("section");
    const navLinks = document.querySelectorAll(".nav-link");

    window.addEventListener("scroll", () => {
      let current = "home";
      sections.forEach(section => {
        const sectionTop = section.offsetTop - 130;
        if (scrollY >= sectionTop) current = section.getAttribute("id");
      });

      navLinks.forEach(link => {
        link.classList.remove("active");
        if (link.getAttribute("href") === `#${current}`) link.classList.add("active");
      });
    });

    // Fade-in animation
    const fadeEls = document.querySelectorAll(".fade-in");
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) entry.target.classList.add("show");
      });
    }, { threshold: 0.12 });

    fadeEls.forEach(el => observer.observe(el));

    // Contact form
    const form = document.getElementById("contactForm");
    const successMsg = document.getElementById("successMsg");

    form.addEventListener("submit", (e) => {
      e.preventDefault();

      const name = document.getElementById("name").value.trim();
      const email = document.getElementById("email").value.trim();
      const message = document.getElementById("message").value.trim();

      if (!name || !email || !message) {
        alert("Please fill all fields.");
        return;
      }

      if (!email.includes("@") || !email.includes(".")) {
        alert("Please enter a valid email.");
        return;
      }

      successMsg.style.display = "block";
      form.reset();

      setTimeout(() => {
        successMsg.style.display = "none";
      }, 4000);
    });

    // Footer year
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
