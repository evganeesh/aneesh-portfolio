<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aneesh N — Social Media Manager</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;1,400&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --gold: #C4922A;
    --gold-light: #E8C47A;
    --gold-pale: #FAF3E0;
    --ink: #1A1614;
    --ink-mid: #3D3530;
    --ink-soft: #7A706B;
    --sand: #F5F0E8;
    --sand-mid: #EDE5D8;
    --white: #FDFCFA;
    --border: rgba(196,146,42,0.2);
    --border-strong: rgba(196,146,42,0.4);
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    background: var(--white);
    color: var(--ink);
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.25rem 4rem;
    background: rgba(253,252,250,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 0.5px solid var(--border);
  }
  .nav-logo {
    font-family: 'DM Mono', monospace;
    font-size: 13px;
    letter-spacing: 0.15em;
    color: var(--gold);
    text-transform: uppercase;
  }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    font-size: 13px;
    font-weight: 400;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--ink-soft);
    text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    position: relative;
    overflow: hidden;
  }
  .hero-left {
    background: var(--ink);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 8rem 5rem 5rem 4rem;
    position: relative;
  }
  .hero-left::after {
    content: '';
    position: absolute;
    right: -1px; top: 10%; bottom: 10%;
    width: 1px;
    background: linear-gradient(to bottom, transparent, var(--gold), transparent);
  }
  .hero-eyebrow {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1.5rem;
    display: flex;
    align-items: center;
    gap: 12px;
  }
  .hero-eyebrow::before {
    content: '';
    display: inline-block;
    width: 32px;
    height: 1px;
    background: var(--gold);
  }
  .hero-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3.5rem, 5vw, 5.5rem);
    font-weight: 400;
    line-height: 1.05;
    color: var(--white);
    margin-bottom: 0.25rem;
  }
  .hero-name em {
    font-style: italic;
    color: var(--gold-light);
  }
  .hero-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1rem, 1.5vw, 1.2rem);
    font-weight: 400;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--ink-soft);
    margin-bottom: 2.5rem;
  }
  .hero-desc {
    font-size: 15px;
    color: rgba(253,252,250,0.65);
    max-width: 420px;
    line-height: 1.8;
    margin-bottom: 3rem;
  }
  .hero-cta {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
  }
  .btn {
    display: inline-block;
    padding: 0.75rem 2rem;
    font-size: 13px;
    font-weight: 400;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    transition: all 0.25s;
    cursor: pointer;
    border: none;
  }
  .btn-gold {
    background: var(--gold);
    color: var(--ink);
  }
  .btn-gold:hover { background: var(--gold-light); }
  .btn-outline {
    background: transparent;
    border: 1px solid rgba(196,146,42,0.5);
    color: var(--gold-light);
  }
  .btn-outline:hover {
    border-color: var(--gold);
    color: var(--gold);
  }

  .hero-right {
    background: var(--sand);
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 8rem 4rem 5rem 5rem;
    position: relative;
  }
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
    margin-bottom: 4rem;
  }
  .stat-card {
    background: var(--white);
    padding: 2rem;
    position: relative;
  }
  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 2px; height: 40%;
    background: var(--gold);
  }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 3rem;
    font-weight: 600;
    color: var(--ink);
    line-height: 1;
    margin-bottom: 0.35rem;
  }
  .stat-label {
    font-size: 12px;
    font-weight: 400;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--ink-soft);
  }
  .platforms-label {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1rem;
  }
  .platform-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  .tag {
    padding: 6px 14px;
    background: var(--sand-mid);
    border: 0.5px solid var(--border);
    font-size: 12px;
    letter-spacing: 0.05em;
    color: var(--ink-mid);
  }

  /* ── SECTIONS ── */
  section { padding: 6rem 4rem; }
  .section-inner { max-width: 1100px; margin: 0 auto; }
  .section-header { margin-bottom: 4rem; }
  .section-num {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.2em;
    color: var(--gold);
    margin-bottom: 0.75rem;
  }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(2rem, 3vw, 3rem);
    font-weight: 400;
    line-height: 1.15;
  }
  .section-title em { font-style: italic; color: var(--gold); }
  .divider {
    width: 60px; height: 1px;
    background: var(--gold);
    margin-top: 1.5rem;
  }

  /* ── ABOUT ── */
  .about-section { background: var(--white); }
  .about-grid {
    display: grid;
    grid-template-columns: 1.2fr 1fr;
    gap: 5rem;
    align-items: start;
  }
  .about-text p { font-size: 16px; color: var(--ink-mid); margin-bottom: 1.25rem; line-height: 1.85; }
  .about-text p:first-child { font-size: 18px; color: var(--ink); }
  .skills-block { }
  .skills-title {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 1.5rem;
    padding-bottom: 0.75rem;
    border-bottom: 0.5px solid var(--border);
  }
  .skill-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.75rem 0;
    border-bottom: 0.5px solid var(--border);
    font-size: 14px;
    color: var(--ink-mid);
  }
  .skill-bar-wrap {
    width: 80px;
    height: 2px;
    background: var(--sand-mid);
    position: relative;
  }
  .skill-bar {
    position: absolute;
    left: 0; top: 0;
    height: 100%;
    background: var(--gold);
  }

  /* ── EXPERIENCE ── */
  .exp-section { background: var(--sand); }
  .exp-timeline { position: relative; }
  .exp-timeline::before {
    content: '';
    position: absolute;
    left: 0; top: 12px; bottom: 0;
    width: 1px;
    background: linear-gradient(to bottom, var(--gold), transparent);
  }
  .exp-item {
    padding-left: 3rem;
    padding-bottom: 3.5rem;
    position: relative;
  }
  .exp-item::before {
    content: '';
    position: absolute;
    left: -5px; top: 10px;
    width: 11px; height: 11px;
    border: 1.5px solid var(--gold);
    background: var(--sand);
    transform: rotate(45deg);
  }
  .exp-date {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.12em;
    color: var(--gold);
    margin-bottom: 0.5rem;
  }
  .exp-role {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.5rem;
    font-weight: 600;
    color: var(--ink);
    margin-bottom: 0.25rem;
  }
  .exp-company {
    font-size: 13px;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--ink-soft);
    margin-bottom: 1rem;
  }
  .exp-bullets {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 0.6rem;
  }
  .exp-bullets li {
    font-size: 14px;
    color: var(--ink-mid);
    padding-left: 1.25rem;
    position: relative;
  }
  .exp-bullets li::before {
    content: '—';
    position: absolute;
    left: 0;
    color: var(--gold);
    font-size: 12px;
  }

  /* ── SERVICES ── */
  .services-section { background: var(--ink); }
  .services-section .section-title { color: var(--white); }
  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5px;
  }
  .service-card {
    background: rgba(255,255,255,0.03);
    border: 0.5px solid rgba(196,146,42,0.15);
    padding: 2.5rem;
    transition: background 0.3s;
    position: relative;
    overflow: hidden;
  }
  .service-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: var(--gold);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.35s ease;
  }
  .service-card:hover::after { transform: scaleX(1); }
  .service-card:hover { background: rgba(255,255,255,0.06); }
  .service-icon {
    font-size: 28px;
    margin-bottom: 1.25rem;
  }
  .service-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.25rem;
    font-weight: 600;
    color: var(--gold-light);
    margin-bottom: 0.75rem;
  }
  .service-desc {
    font-size: 13px;
    color: rgba(253,252,250,0.5);
    line-height: 1.7;
  }

  /* ── WORK SAMPLES PLACEHOLDER ── */
  .work-section { background: var(--white); }
  .work-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }
  .work-card {
    aspect-ratio: 4/3;
    background: var(--sand);
    border: 0.5px solid var(--border);
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    padding: 1.5rem;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s;
  }
  .work-card:hover { border-color: var(--gold); }
  .work-placeholder {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.15em;
    color: var(--border-strong);
    text-transform: uppercase;
  }
  .work-label {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 0.35rem;
    position: relative;
    z-index: 1;
  }
  .work-title {
    font-size: 14px;
    font-weight: 400;
    color: var(--ink);
    position: relative;
    z-index: 1;
  }

  /* ── CONTACT ── */
  .contact-section {
    background: var(--sand);
    text-align: center;
  }
  .contact-section .section-header { margin-bottom: 3rem; }
  .contact-section .divider { margin: 1.5rem auto 0; }
  .contact-grid {
    display: flex;
    justify-content: center;
    gap: 3rem;
    flex-wrap: wrap;
    margin: 3rem 0;
  }
  .contact-item {
    text-align: center;
  }
  .contact-type {
    font-family: 'DM Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 0.35rem;
  }
  .contact-val {
    font-size: 15px;
    color: var(--ink-mid);
  }
  .contact-val a { color: inherit; text-decoration: none; }
  .contact-val a:hover { color: var(--gold); }
  .contact-availability {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 0.6rem 1.5rem;
    border: 1px solid rgba(196,146,42,0.3);
    font-size: 13px;
    color: var(--ink-soft);
    margin-bottom: 2.5rem;
  }
  .dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: #4CAF50;
    animation: pulse 2s ease-in-out infinite;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  /* ── FOOTER ── */
  footer {
    background: var(--ink);
    padding: 2rem 4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-top: 0.5px solid rgba(196,146,42,0.2);
  }
  footer p {
    font-size: 12px;
    color: var(--ink-soft);
    letter-spacing: 0.05em;
  }
  .footer-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem;
    color: var(--gold-light);
  }

  /* ── ANIMATIONS ── */
  .fade-up {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }
  .fade-up.visible { opacity: 1; transform: translateY(0); }

  @media (max-width: 900px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    .hero { grid-template-columns: 1fr; }
    .hero-right { display: none; }
    .hero-left { padding: 6rem 2rem 4rem; }
    section { padding: 4rem 1.5rem; }
    .about-grid, .services-grid, .work-grid { grid-template-columns: 1fr; }
    footer { flex-direction: column; gap: 0.5rem; text-align: center; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <span class="nav-logo">Aneesh N</span>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#work">Work</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" id="top">
  <div class="hero-left">
    <p class="hero-eyebrow">Dubai, UAE — Available for opportunities</p>
    <h1 class="hero-name">Aneesh <em>N</em></h1>
    <p class="hero-title">Social Media Manager &amp; Real Estate Marketer</p>
    <p class="hero-desc">Crafting campaigns that convert. 5+ years driving brand visibility and lead generation across Dubai's competitive real estate landscape.</p>
    <div class="hero-cta">
      <a href="#contact" class="btn btn-gold">Get in touch</a>
      <a href="#work" class="btn btn-outline">View work</a>
    </div>
  </div>
  <div class="hero-right">
    <div class="stats-grid">
      <div class="stat-card">
        <div class="stat-num">5+</div>
        <div class="stat-label">Years in Dubai RE</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">3</div>
        <div class="stat-label">Major agencies</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">360°</div>
        <div class="stat-label">Campaign coverage</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">↑ROI</div>
        <div class="stat-label">Proven ad results</div>
      </div>
    </div>
    <div>
      <p class="platforms-label">Platforms &amp; Tools</p>
      <div class="platform-tags">
        <span class="tag">Instagram</span>
        <span class="tag">Facebook</span>
        <span class="tag">LinkedIn</span>
        <span class="tag">Google Ads</span>
        <span class="tag">Meta Ads</span>
        <span class="tag">Property Finder</span>
        <span class="tag">Bayut</span>
        <span class="tag">Dubizzle</span>
        <span class="tag">Canva</span>
        <span class="tag">Photoshop</span>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section class="about-section fade-up" id="about">
  <div class="section-inner">
    <div class="section-header">
      <p class="section-num">01 — About</p>
      <h2 class="section-title">Strategy-driven.<br><em>Results-focused.</em></h2>
      <div class="divider"></div>
    </div>
    <div class="about-grid">
      <div class="about-text">
        <p>I'm a results-driven marketing professional with over 5 years of specialised experience in Dubai's real estate sector — one of the world's most competitive property markets.</p>
        <p>From high-end residential developments to commercial listings, I build and execute end-to-end marketing strategies that drive measurable enquiries, grow engaged audiences, and convert attention into sales leads.</p>
        <p>My background spans digital advertising, content production (photography, videography, virtual tours), regulatory compliance with RERA &amp; Trakheesi, and full-funnel CRM management — giving me a rare combination of creative and operational fluency.</p>
      </div>
      <div class="skills-block">
        <p class="skills-title">Core skills</p>
        <div class="skill-row">Real Estate Marketing<div class="skill-bar-wrap"><div class="skill-bar" style="width:95%"></div></div></div>
        <div class="skill-row">Social Media Strategy<div class="skill-bar-wrap"><div class="skill-bar" style="width:92%"></div></div></div>
        <div class="skill-row">Paid Advertising (Meta / Google)<div class="skill-bar-wrap"><div class="skill-bar" style="width:88%"></div></div></div>
        <div class="skill-row">Content Creation<div class="skill-bar-wrap"><div class="skill-bar" style="width:90%"></div></div></div>
        <div class="skill-row">SEO &amp; Analytics<div class="skill-bar-wrap"><div class="skill-bar" style="width:82%"></div></div></div>
        <div class="skill-row">Graphic Design (Canva / Photoshop)<div class="skill-bar-wrap"><div class="skill-bar" style="width:85%"></div></div></div>
        <div class="skill-row">RERA / Trakheesi Compliance<div class="skill-bar-wrap"><div class="skill-bar" style="width:95%"></div></div></div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section class="exp-section fade-up" id="experience">
  <div class="section-inner">
    <div class="section-header">
      <p class="section-num">02 — Experience</p>
      <h2 class="section-title">A decade of<br><em>building brands.</em></h2>
      <div class="divider"></div>
    </div>
    <div class="exp-timeline">

      <div class="exp-item">
        <p class="exp-date">Nov 2024 — Present</p>
        <p class="exp-role">Real Estate Marketing Manager & Social Media Manager</p>
        <p class="exp-company">DNAAR Properties LLC — Dubai, UAE</p>
        <ul class="exp-bullets">
          <li>Developed comprehensive marketing campaigns for high-end residential and commercial properties, increasing enquiries significantly.</li>
          <li>Managed Instagram, Facebook, and LinkedIn accounts, boosting engagement rates and follower growth.</li>
          <li>Executed paid ad campaigns on Google and Meta, optimising ad spend for increased ROI.</li>
          <li>Organised property launches and open house events driving immediate sales leads.</li>
          <li>Created high-converting listings on Property Finder, Bayut, and Dubizzle.</li>
          <li>Ensured full RERA and Trakheesi compliance across all advertising.</li>
        </ul>
      </div>

      <div class="exp-item">
        <p class="exp-date">Aug 2022 — Oct 2024</p>
        <p class="exp-role">Real Estate Marketing Specialist & Social Media Manager</p>
        <p class="exp-company">APTIN Properties LLC — Dubai, UAE</p>
        <ul class="exp-bullets">
          <li>Maintained daily posting schedules and audience engagement across all platforms.</li>
          <li>Developed hashtag strategies that increased organic reach measurably.</li>
          <li>Designed promotional materials for high-value property listings.</li>
          <li>Supported property launches, open houses, and promotional events.</li>
          <li>Maintained accurate listings across all property portals.</li>
        </ul>
      </div>

      <div class="exp-item">
        <p class="exp-date">Mar 2018 — Jun 2022</p>
        <p class="exp-role">Social Media Manager</p>
        <p class="exp-company">VSK Media House — Kerala, India</p>
        <ul class="exp-bullets">
          <li>Led social media campaigns and managed full monthly content calendars.</li>
          <li>Handled website content creation and implementation.</li>
          <li>Administered web analytics dashboards and delivered performance reports.</li>
          <li>Aligned media and PR schedules across channels.</li>
        </ul>
      </div>

    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="services-section fade-up" id="services">
  <div class="section-inner">
    <div class="section-header">
      <p class="section-num" style="color: var(--gold);">03 — Services</p>
      <h2 class="section-title">What I bring<br><em>to your brand.</em></h2>
      <div class="divider"></div>
    </div>
    <div class="services-grid">
      <div class="service-card">
        <div class="service-icon">📱</div>
        <p class="service-name">Social Media Management</p>
        <p class="service-desc">Full-service management of Instagram, Facebook, and LinkedIn — from strategy and content calendars to daily posting, community engagement, and growth reporting.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">🏠</div>
        <p class="service-name">Real Estate Marketing</p>
        <p class="service-desc">End-to-end property marketing including portal listings (Property Finder, Bayut, Dubizzle), campaign strategy, compliance with RERA/Trakheesi, and event coordination.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">🎯</div>
        <p class="service-name">Paid Advertising</p>
        <p class="service-desc">Performance-driven Google Ads and Meta Ads campaigns with audience targeting, creative testing, and ROI optimisation tailored to the Dubai market.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">📸</div>
        <p class="service-name">Content Creation</p>
        <p class="service-desc">Photography, videography, virtual tours, and graphic design (Canva, Photoshop) crafted to showcase properties at their most compelling.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">📊</div>
        <p class="service-name">Analytics & Reporting</p>
        <p class="service-desc">Data-driven performance tracking, KPI dashboards, and actionable monthly reports that connect marketing activity to business outcomes.</p>
      </div>
      <div class="service-card">
        <div class="service-icon">🔍</div>
        <p class="service-name">SEO & Lead Generation</p>
        <p class="service-desc">Website optimisation, organic content strategy, and multi-channel lead generation funnels designed to capture and convert the right audience.</p>
      </div>
    </div>
  </div>
</section>

<!-- WORK SAMPLES -->
<section class="work-section fade-up" id="work">
  <div class="section-inner">
    <div class="section-header">
      <p class="section-num">04 — Work</p>
      <h2 class="section-title">Selected<br><em>projects.</em></h2>
      <div class="divider"></div>
    </div>
    <div class="work-grid">
      <div class="work-card">
        <div class="work-placeholder">Campaign screenshot</div>
        <p class="work-label">Social Campaign</p>
        <p class="work-title">DNAAR — Property Launch</p>
      </div>
      <div class="work-card">
        <div class="work-placeholder">Ad creative</div>
        <p class="work-label">Paid Ads</p>
        <p class="work-title">Meta Ads — Lead Generation</p>
      </div>
      <div class="work-card">
        <div class="work-placeholder">Listing screenshot</div>
        <p class="work-label">Portal Listing</p>
        <p class="work-title">Property Finder — Premium Listing</p>
      </div>
      <div class="work-card">
        <div class="work-placeholder">Post design</div>
        <p class="work-label">Content Design</p>
        <p class="work-title">APTIN — Instagram Series</p>
      </div>
      <div class="work-card">
        <div class="work-placeholder">Event photo</div>
        <p class="work-label">Event Marketing</p>
        <p class="work-title">Open House — High-Rise Launch</p>
      </div>
      <div class="work-card">
        <div class="work-placeholder">Analytics screenshot</div>
        <p class="work-label">Analytics Report</p>
        <p class="work-title">Performance Dashboard — Q4</p>
      </div>
    </div>
    <p style="margin-top: 2rem; font-size: 13px; color: var(--ink-soft); font-style: italic;">↑ Work samples and screenshots to be added. Contact for portfolio deck.</p>
  </div>
</section>

<!-- CONTACT -->
<section class="contact-section fade-up" id="contact">
  <div class="section-inner">
    <div class="section-header">
      <p class="section-num">05 — Contact</p>
      <h2 class="section-title">Let's work<br><em>together.</em></h2>
      <div class="divider"></div>
    </div>
    <div class="contact-availability"><span class="dot"></span> Open to new opportunities in Dubai</div>
    <div class="contact-grid">
      <div class="contact-item">
        <p class="contact-type">Email</p>
        <p class="contact-val"><a href="mailto:evergreenaneesh@gmail.com">evergreenaneesh@gmail.com</a></p>
      </div>
      <div class="contact-item">
        <p class="contact-type">Phone / WhatsApp</p>
        <p class="contact-val"><a href="tel:+971557118169">+971 55 711 8169</a></p>
      </div>
      <div class="contact-item">
        <p class="contact-type">Location</p>
        <p class="contact-val">Dubai Silicon Oasis, Dubai — UAE</p>
      </div>
      <div class="contact-item">
        <p class="contact-type">Languages</p>
        <p class="contact-val">English · Hindi · Malayalam</p>
      </div>
    </div>
    <a href="mailto:evergreenaneesh@gmail.com" class="btn btn-gold">Send a message</a>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p class="footer-name">Aneesh N</p>
  <p>Social Media &amp; Real Estate Marketing Manager</p>
  <p>Dubai, UAE · © 2025</p>
</footer>

<script>
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.1 });
  document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));
</script>
</body>
</html>
