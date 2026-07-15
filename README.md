# index.htm
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sai Shiva Balaboina — Portfolio</title>
<meta name="description" content="Sai Shiva Balaboina — MSc Project Management candidate bridging AI capability and everyday adoption.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#0E1B2A;
    --ink-soft:#132537;
    --blueprint-deep:#173A52;
    --blueprint:#4FA3C7;
    --blueprint-bright:#7DC3E0;
    --amber:#E2A63B;
    --paper:#ECE7D8;
    --paper-2:#E2DCC9;
    --ink-text:#16232F;
    --slate:#5F6B78;
    --line: rgba(79,163,199,0.28);
    --display: 'Space Grotesk', sans-serif;
    --body: 'IBM Plex Sans', sans-serif;
    --mono: 'IBM Plex Mono', monospace;
  }

  *{ box-sizing:border-box; }
  html{ scroll-behavior:smooth; }
  body{
    margin:0;
    background:var(--paper);
    color:var(--ink-text);
    font-family:var(--body);
    -webkit-font-smoothing:antialiased;
  }
  img,svg{ display:block; max-width:100%; }
  a{ color:inherit; }
  h1,h2,h3{ font-family:var(--display); margin:0; }
  p{ margin:0; }
  ul{ margin:0; padding:0; list-style:none; }
  .mono{ font-family:var(--mono); }

  ::selection{ background:var(--amber); color:var(--ink); }

  @media (prefers-reduced-motion: reduce){
    *{ animation-duration:0.01ms !important; animation-iteration-count:1 !important; transition-duration:0.01ms !important; scroll-behavior:auto !important; }
  }

  /* ---------- shared layout ---------- */
  .wrap{ max-width:1140px; margin:0 auto; padding:0 32px; }
  .eyebrow{
    font-family:var(--mono);
    font-size:12px;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--blueprint);
  }
  .dark .eyebrow{ color:var(--blueprint-bright); }

  .sheet-tag{
    font-family:var(--mono);
    font-size:11px;
    letter-spacing:0.08em;
    color:var(--slate);
    text-transform:uppercase;
  }

  /* corner-bracket frame, drafting-sheet motif */
  .frame{
    position:relative;
    border:1px solid var(--line);
  }
  .frame::before,.frame::after,
  .frame .c2::before,.frame .c2::after{
    content:"";
    position:absolute;
    width:14px; height:14px;
    border:2px solid var(--blueprint);
    opacity:0.85;
  }
  .frame::before{ top:-1px; left:-1px; border-right:none; border-bottom:none; }
  .frame::after{ bottom:-1px; right:-1px; border-left:none; border-top:none; }

  section{ position:relative; }
  .section-pad{ padding:96px 0; }
  @media (max-width:720px){ .section-pad{ padding:64px 0; } }

  .section-head{
    display:flex;
    align-items:baseline;
    justify-content:space-between;
    gap:24px;
    border-bottom:1px solid rgba(22,35,47,0.14);
    padding-bottom:18px;
    margin-bottom:48px;
    flex-wrap:wrap;
  }
  .dark .section-head{ border-bottom-color:rgba(255,255,255,0.14); }
  .section-title{ font-size:32px; font-weight:600; letter-spacing:-0.01em; }
  @media (max-width:560px){ .section-title{ font-size:26px; } }

  /* ---------- nav ---------- */
  header.nav{
    position:fixed; top:0; left:0; right:0; z-index:50;
    background:rgba(14,27,42,0.92);
    backdrop-filter:blur(8px);
    border-bottom:1px solid rgba(79,163,199,0.35);
  }
  header.nav::after{
    content:"";
    display:block;
    height:6px;
    background-image:repeating-linear-gradient(90deg, rgba(79,163,199,0.55) 0 1px, transparent 1px 12px);
    background-position:bottom;
  }
  .nav-inner{
    max-width:1140px; margin:0 auto; padding:0 32px;
    height:64px; display:flex; align-items:center; justify-content:space-between;
  }
  .brand{
    font-family:var(--mono); font-weight:600; color:var(--paper);
    letter-spacing:0.04em; font-size:15px; text-decoration:none;
    display:flex; align-items:center; gap:8px;
  }
  .brand .dot{ width:8px; height:8px; background:var(--amber); border-radius:1px; transform:rotate(45deg); }
  nav.links{ display:flex; gap:28px; }
  nav.links a{
    color:rgba(236,231,216,0.72);
    text-decoration:none;
    font-family:var(--mono);
    font-size:12.5px;
    letter-spacing:0.06em;
    text-transform:uppercase;
    transition:color .2s ease;
  }
  nav.links a:hover{ color:var(--blueprint-bright); }
  .nav-cta{
    font-family:var(--mono); font-size:12px; letter-spacing:0.06em;
    color:var(--ink); background:var(--amber);
    padding:8px 14px; text-decoration:none; text-transform:uppercase;
    border-radius:2px;
  }
  .menu-btn{ display:none; background:none; border:1px solid rgba(236,231,216,0.4); color:var(--paper); padding:6px 10px; font-family:var(--mono); }
  @media (max-width:860px){
    nav.links{ display:none; }
    .menu-btn{ display:block; }
  }

  /* ---------- hero ---------- */
  .hero{
    background:
      radial-gradient(ellipse at 20% -10%, rgba(79,163,199,0.18), transparent 55%),
      var(--ink);
    color:var(--paper);
    padding:150px 0 90px;
    overflow:hidden;
  }
  .hero::before{
    content:"";
    position:absolute; inset:0;
    background-image:
      linear-gradient(rgba(79,163,199,0.07) 1px, transparent 1px),
      linear-gradient(90deg, rgba(79,163,199,0.07) 1px, transparent 1px);
    background-size:38px 38px;
    mask-image:linear-gradient(to bottom, black, transparent 85%);
    pointer-events:none;
  }
  .hero-grid{
    position:relative;
    display:grid;
    grid-template-columns:1.05fr 0.95fr;
    gap:48px;
    align-items:center;
  }
  @media (max-width:900px){ .hero-grid{ grid-template-columns:1fr; } }

  .hero h1{
    font-size:clamp(34px, 5vw, 54px);
    line-height:1.08;
    font-weight:700;
    letter-spacing:-0.015em;
    margin:18px 0 22px;
  }
  .hero h1 em{
    font-style:normal;
    color:var(--blueprint-bright);
    border-bottom:3px solid var(--amber);
  }
  .hero p.sub{
    font-size:17px;
    line-height:1.65;
    color:rgba(236,231,216,0.78);
    max-width:46ch;
  }
  .hero-ctas{ display:flex; gap:14px; margin-top:34px; flex-wrap:wrap; }
  .btn{
    font-family:var(--mono);
    font-size:13px;
    letter-spacing:0.05em;
    text-transform:uppercase;
    text-decoration:none;
    padding:13px 22px;
    display:inline-block;
    border-radius:2px;
    transition:transform .18s ease, background .18s ease, color .18s ease;
  }
  .btn:hover{ transform:translateY(-2px); }
  .btn-primary{ background:var(--amber); color:var(--ink); }
  .btn-primary:hover{ background:var(--blueprint-bright); }
  .btn-ghost{ border:1px solid rgba(236,231,216,0.4); color:var(--paper); }
  .btn-ghost:hover{ border-color:var(--blueprint-bright); color:var(--blueprint-bright); }

  .hero-meta{
    margin-top:44px;
    display:flex;
    gap:28px;
    flex-wrap:wrap;
    font-family:var(--mono);
    font-size:12px;
    color:rgba(236,231,216,0.55);
  }
  .hero-meta b{ color:var(--blueprint-bright); font-weight:500; }

  /* bridge svg */
  .bridge-wrap{ position:relative; }
  .bridge-wrap .sheet-label{
    position:absolute; bottom:-26px; right:0;
    font-family:var(--mono); font-size:10.5px; color:rgba(236,231,216,0.4);
    letter-spacing:0.08em;
  }
  #bridge-svg .draw{
    stroke-dasharray:1400;
    stroke-dashoffset:1400;
    animation:draw 2.6s ease forwards;
  }
  #bridge-svg .draw2{
    stroke-dasharray:900;
    stroke-dashoffset:900;
    animation:draw 2.2s ease forwards .3s;
  }
  #bridge-svg .fade{ opacity:0; animation:fadein 1s ease forwards 2.1s; }
  @keyframes draw{ to{ stroke-dashoffset:0; } }
  @keyframes fadein{ to{ opacity:1; } }

  /* ---------- stat strip ---------- */
  .stats{
    background:var(--ink-soft);
    border-top:1px solid rgba(79,163,199,0.25);
    border-bottom:1px solid rgba(79,163,199,0.25);
    padding:36px 0;
  }
  .stats-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:24px;
    text-align:center;
  }
  @media (max-width:760px){ .stats-grid{ grid-template-columns:repeat(2,1fr); row-gap:32px; } }
  .stat b{
    display:block; font-family:var(--display); font-weight:700;
    font-size:clamp(24px,3vw,32px); color:var(--paper);
    letter-spacing:-0.01em;
  }
  .stat span{
    display:block; margin-top:6px; font-family:var(--mono); font-size:11px;
    letter-spacing:0.05em; text-transform:uppercase; color:rgba(236,231,216,0.55);
  }

  /* ---------- resume link btn ---------- */
  .btn-resume{
    background:transparent; color:var(--blueprint-bright);
    border:1px solid rgba(125,195,224,0.5);
  }
  .btn-resume:hover{ background:rgba(125,195,224,0.1); color:var(--blueprint-bright); }
  .btn-resume svg{ display:inline; vertical-align:-2px; margin-right:6px; width:13px; height:13px; }

  /* ---------- project impact chips ---------- */
  .chip-row{ display:flex; gap:10px; flex-wrap:wrap; margin-top:22px; }
  .chip{
    font-family:var(--mono); font-size:11.5px; letter-spacing:0.03em;
    color:var(--amber); border:1px solid rgba(226,166,59,0.45);
    padding:6px 12px; border-radius:2px; white-space:nowrap;
  }

  /* ---------- floating CTA ---------- */
  .float-cta{
    position:fixed; right:24px; bottom:24px; z-index:60;
    background:var(--amber); color:var(--ink);
    font-family:var(--mono); font-size:12.5px; letter-spacing:0.04em;
    text-transform:uppercase; text-decoration:none;
    padding:14px 20px; border-radius:2px;
    box-shadow:0 8px 24px rgba(0,0,0,0.28);
    display:flex; align-items:center; gap:8px;
    opacity:0; transform:translateY(12px) scale(0.96);
    pointer-events:none;
    transition:opacity .3s ease, transform .3s ease;
  }
  .float-cta.show{ opacity:1; transform:translateY(0) scale(1); pointer-events:auto; }
  .float-cta:hover{ background:var(--blueprint-bright); }
  @media (max-width:560px){ .float-cta{ left:16px; right:16px; justify-content:center; } }

  /* ---------- about ---------- */
  .about-grid{
    display:grid;
    grid-template-columns:1.3fr 1fr;
    gap:56px;
    align-items:start;
  }
  @media (max-width:860px){ .about-grid{ grid-template-columns:1fr; } }
  .about-text p{ font-size:16.5px; line-height:1.75; color:#293846; margin-bottom:18px; }
  .about-text p:last-child{ margin-bottom:0; }

  .spec-table{ padding:24px; }
  .spec-row{
    display:flex; justify-content:space-between; gap:16px;
    padding:12px 0;
    border-bottom:1px dashed rgba(22,35,47,0.18);
    font-size:13.5px;
  }
  .spec-row:last-child{ border-bottom:none; }
  .spec-row .k{ font-family:var(--mono); color:var(--slate); text-transform:uppercase; letter-spacing:0.05em; font-size:11.5px; }
  .spec-row .v{ font-weight:500; text-align:right; }

  /* ---------- skills ---------- */
  .skill-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:1px;
    background:rgba(22,35,47,0.14);
    border:1px solid rgba(22,35,47,0.14);
  }
  @media (max-width:860px){ .skill-grid{ grid-template-columns:repeat(2,1fr); } }
  .skill-card{ background:var(--paper); padding:26px 22px; }
  .skill-card h3{
    font-family:var(--mono); font-size:12px; text-transform:uppercase;
    letter-spacing:0.06em; color:var(--blueprint); margin-bottom:14px;
  }
  .skill-card ul li{
    font-size:14px; padding:5px 0; color:#293846;
    border-top:1px solid rgba(22,35,47,0.08);
  }
  .skill-card ul li:first-child{ border-top:none; }

  /* ---------- certifications ---------- */
  .cert-list{ display:flex; flex-direction:column; }
  .cert-row{
    display:grid;
    grid-template-columns:1fr auto;
    gap:16px;
    padding:18px 0;
    border-bottom:1px solid rgba(22,35,47,0.12);
    align-items:baseline;
  }
  .cert-row:first-child{ padding-top:0; }
  .cert-row:last-child{ border-bottom:none; }
  .cert-name{ font-weight:600; font-size:16px; }
  .cert-issuer{ color:var(--slate); font-size:13.5px; margin-top:3px; }
  .cert-date{ font-family:var(--mono); font-size:12.5px; color:var(--blueprint); white-space:nowrap; }

  /* ---------- projects ---------- */
  .project-card{
    background:var(--ink);
    color:var(--paper);
    padding:36px;
    margin-bottom:28px;
  }
  .project-card:last-child{ margin-bottom:0; }
  .titleblock{
    display:flex; justify-content:space-between; align-items:flex-start;
    border-bottom:1px solid rgba(79,163,199,0.3);
    padding-bottom:16px; margin-bottom:22px;
    flex-wrap:wrap; gap:10px;
  }
  .titleblock .tb-left .sheet-tag{ color:var(--blueprint-bright); opacity:0.8; }
  .titleblock h3{ font-size:22px; margin-top:6px; }
  .titleblock .tb-right{ text-align:right; font-family:var(--mono); font-size:12px; color:rgba(236,231,216,0.55); }
  .project-org{ color:rgba(236,231,216,0.55); font-size:13.5px; margin-bottom:18px; }
  .project-cols{
    display:grid; grid-template-columns:repeat(3,1fr); gap:24px;
  }
  @media (max-width:760px){ .project-cols{ grid-template-columns:1fr; } }
  .project-cols h4{
    font-family:var(--mono); font-size:11px; text-transform:uppercase;
    letter-spacing:0.06em; color:var(--amber); margin-bottom:8px;
  }
  .project-cols p{ font-size:14.5px; line-height:1.65; color:rgba(236,231,216,0.85); }

  /* ---------- experience timeline (ruler) ---------- */
  .ruler{ position:relative; padding-left:26px; }
  .ruler::before{
    content:""; position:absolute; left:5px; top:6px; bottom:6px; width:1px;
    background-image:repeating-linear-gradient(to bottom, var(--blueprint) 0 2px, transparent 2px 14px);
  }
  .exp-item{ position:relative; padding-bottom:44px; }
  .exp-item:last-child{ padding-bottom:0; }
  .exp-item::before{
    content:""; position:absolute; left:-26px; top:4px;
    width:11px; height:11px; border-radius:50%;
    background:var(--paper); border:2px solid var(--blueprint);
  }
  .exp-role{ font-size:19px; font-weight:600; }
  .exp-org{ color:var(--slate); font-size:14px; margin-top:2px; }
  .exp-date{ font-family:var(--mono); font-size:12px; color:var(--blueprint); margin-top:4px; display:block; }
  .exp-desc{ font-size:14.5px; line-height:1.65; color:#293846; margin-top:12px; max-width:62ch; }

  /* ---------- education ---------- */
  .edu-grid{ display:grid; grid-template-columns:1fr 1fr; gap:24px; }
  @media (max-width:760px){ .edu-grid{ grid-template-columns:1fr; } }
  .edu-card{ padding:26px; }
  .edu-card .sheet-tag{ margin-bottom:10px; display:block; }
  .edu-card h3{ font-size:19px; margin-bottom:6px; line-height:1.35; }
  .edu-card .org{ color:var(--slate); font-size:14px; }
  .edu-card .date{ font-family:var(--mono); font-size:12px; color:var(--blueprint); margin-top:10px; display:block; }

  /* ---------- contact ---------- */
  .contact{
    background:var(--ink); color:var(--paper);
    padding:110px 0 80px;
    text-align:center;
  }
  .contact .eyebrow{ justify-content:center; display:flex; }
  .contact h2{
    font-size:clamp(28px,4vw,42px); margin:16px 0 20px; font-weight:600;
  }
  .contact p{ color:rgba(236,231,216,0.72); font-size:16px; max-width:52ch; margin:0 auto 34px; line-height:1.6; }
  .contact-ctas{ display:flex; justify-content:center; gap:14px; flex-wrap:wrap; }
  footer{
    text-align:center; padding:26px 0; font-family:var(--mono);
    font-size:11.5px; color:rgba(236,231,216,0.4); background:var(--ink);
    border-top:1px solid rgba(79,163,199,0.2);
  }

  /* reveal on scroll */
  .reveal{ opacity:0; transform:translateY(18px); transition:opacity .7s ease, transform .7s ease; }
  .reveal.in{ opacity:1; transform:translateY(0); }
</style>
</head>
<body>

<header class="nav">
  <div class="nav-inner">
    <a href="#" class="brand"><span class="dot"></span>S. BALABOINA</a>
    <nav class="links">
      <a href="#about">About</a>
      <a href="#work">Work</a>
      <a href="#certifications">Certs</a>
      <a href="#experience">Experience</a>
      <a href="#education">Education</a>
      <a href="Sai_Shiva_Balaboina_Resume_SKEMA_AI_Project_Assistant.docx">Resume</a>
    </nav>
    <a class="nav-cta" href="#contact">Contact</a>
  </div>
</header>

<!-- ================= HERO ================= -->
<section class="hero dark">
  <div class="wrap hero-grid">
    <div>
      <p class="eyebrow">MSc Project Management · SKEMA Business School · Available Sept 2026</p>
      <h1>I turn AI capability into <em>everyday adoption.</em></h1>
      <p class="sub">Trained on the Anthropic API and Model Context Protocol. I've shipped no-code tools that non-technical teams run without me in the room — and I'm looking for the room where that skill compounds.</p>
      <div class="hero-ctas">
        <a class="btn btn-primary" href="#work">View the work</a>
        <a class="btn btn-ghost" href="#contact">Get in touch</a>
        <a class="btn btn-resume" href="Sai_Shiva_Balaboina_Resume_SKEMA_AI_Project_Assistant.docx" download>
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 3v12m0 0l-4-4m4 4l4-4M4 19h16"/></svg>Download résumé
        </a>
      </div>
      <div class="hero-meta">
        <span><b>Based in</b> Paris, France</span>
        <span><b>Languages</b> English · French (A2/B1)</span>
        <span><b>Available</b> Sep 2026 – Feb 2027</span>
      </div>
    </div>

    <div class="bridge-wrap">
      <svg id="bridge-svg" viewBox="0 0 640 380" xmlns="http://www.w3.org/2000/svg">
        <!-- grid ticks -->
        <g stroke="rgba(125,195,224,0.25)" stroke-width="1">
          <line x1="40" y1="330" x2="600" y2="330"/>
        </g>
        <!-- towers -->
        <g stroke="#4FA3C7" stroke-width="2" fill="none" class="draw2">
          <line x1="180" y1="330" x2="180" y2="70"/>
          <line x1="460" y1="330" x2="460" y2="70"/>
          <line x1="165" y1="330" x2="195" y2="330"/>
          <line x1="445" y1="330" x2="475" y2="330"/>
        </g>
        <!-- deck -->
        <g stroke="#7DC3E0" stroke-width="2" class="draw">
          <line x1="40" y1="300" x2="600" y2="300"/>
        </g>
        <g stroke="rgba(125,195,224,0.55)" stroke-width="1" class="fade">
          <line x1="60" y1="300" x2="60" y2="312"/>
          <line x1="100" y1="300" x2="100" y2="312"/>
          <line x1="140" y1="300" x2="140" y2="312"/>
          <line x1="220" y1="300" x2="220" y2="312"/>
          <line x1="260" y1="300" x2="260" y2="312"/>
          <line x1="300" y1="300" x2="300" y2="312"/>
          <line x1="340" y1="300" x2="340" y2="312"/>
          <line x1="380" y1="300" x2="380" y2="312"/>
          <line x1="420" y1="300" x2="420" y2="312"/>
          <line x1="500" y1="300" x2="500" y2="312"/>
          <line x1="540" y1="300" x2="540" y2="312"/>
          <line x1="580" y1="300" x2="580" y2="312"/>
        </g>
        <!-- main cables -->
        <path d="M40,300 Q180,90 320,205 Q460,90 600,300" fill="none" stroke="#E2A63B" stroke-width="2.5" class="draw"/>
        <!-- hangers -->
        <g stroke="rgba(226,166,59,0.55)" stroke-width="1" class="fade">
          <line x1="180" y1="300" x2="180" y2="112"/>
          <line x1="460" y1="300" x2="460" y2="112"/>
          <line x1="320" y1="300" x2="320" y2="207"/>
          <line x1="240" y1="300" x2="240" y2="150"/>
          <line x1="400" y1="300" x2="400" y2="150"/>
        </g>
        <!-- keystone node -->
        <circle cx="320" cy="205" r="10" fill="#0E1B2A" stroke="#E2A63B" stroke-width="2" class="fade"/>
        <text x="320" y="209" text-anchor="middle" font-family="IBM Plex Mono" font-size="9" fill="#E2A63B" class="fade">SB</text>
        <!-- labels -->
        <text x="40" y="345" font-family="IBM Plex Mono" font-size="11" fill="rgba(236,231,216,0.55)" class="fade">COMMUNITY NEEDS</text>
        <text x="600" y="345" text-anchor="end" font-family="IBM Plex Mono" font-size="11" fill="rgba(236,231,216,0.55)" class="fade">AI CAPABILITY</text>
        <!-- crop marks -->
        <g stroke="rgba(125,195,224,0.4)" stroke-width="1">
          <line x1="10" y1="10" x2="26" y2="10"/><line x1="10" y1="10" x2="10" y2="26"/>
          <line x1="630" y1="370" x2="614" y2="370"/><line x1="630" y1="370" x2="630" y2="354"/>
        </g>
      </svg>
      <span class="sheet-label mono">FIG. 01 — ADOPTION SPAN, ELEV.</span>
    </div>
  </div>
</section>

<!-- ================= STATS ================= -->
<section class="stats dark">
  <div class="wrap stats-grid">
    <div class="stat"><b>250+</b><span>Candidate records owned solo</span></div>
    <div class="stat"><b>26/26</b><span>Governance cycles held aligned</span></div>
    <div class="stat"><b>7 days</b><span>Idea to shipped ESG dashboard</span></div>
    <div class="stat"><b>100+</b><span>Live events coordinated</span></div>
  </div>
</section>

<!-- ================= ABOUT ================= -->
<section id="about" class="section-pad">
  <div class="wrap reveal">
    <div class="section-head">
      <h2 class="section-title">About</h2>
      <span class="sheet-tag">Profile · Sheet 01</span>
    </div>
    <div class="about-grid">
      <div class="about-text">
        <p>I'm an MSc Project Management candidate at SKEMA, and most of what I do comes down to one habit: build the tool, then make sure nobody needs me in the room to run it.</p>
        <p>That's meant shipping a no-code ESG dashboard a non-technical team could trust from day one, and training directly on the Anthropic API and Model Context Protocol to understand how AI agents actually get built — not just how they get discussed. I pair that technical curiosity with a genuinely service-oriented streak: as the single point of contact for 250+ candidate records at a staffing firm, I learned that clarity, patience, and good documentation are what actually get people to adopt something new.</p>
        <p>I'm entering M2 in September 2026, and I'm looking for a role where I can keep doing exactly this: bridging complex AI tools and the everyday people who need them to just work.</p>
      </div>
      <div class="spec-table frame">
        <div class="spec-row"><span class="k">Location</span><span class="v">Paris, France</span></div>
        <div class="spec-row"><span class="k">Program</span><span class="v">MSc Project Mgmt, SKEMA</span></div>
        <div class="spec-row"><span class="k">Prior degree</span><span class="v">B.Tech, Civil Engineering</span></div>
        <div class="spec-row"><span class="k">Availability</span><span class="v">Sep 2026 – Feb 2027</span></div>
        <div class="spec-row"><span class="k">Languages</span><span class="v">English · French (A2/B1)</span></div>
        <div class="spec-row"><span class="k">Contact</span><span class="v">saishiva.balaboina@skema.edu</span></div>
      </div>
    </div>
  </div>
</section>

<!-- ================= SKILLS ================= -->
<section class="section-pad" style="background:var(--paper-2);">
  <div class="wrap reveal">
    <div class="section-head">
      <h2 class="section-title">Skills</h2>
      <span class="sheet-tag">Toolset · Sheet 02</span>
    </div>
    <div class="skill-grid frame">
      <div class="skill-card">
        <h3>Automation &amp; Data</h3>
        <ul>
          <li>No-Code (Power Apps)</li>
          <li>Anthropic API</li>
          <li>Model Context Protocol (MCP)</li>
          <li>Python</li>
          <li>Power BI</li>
        </ul>
      </div>
      <div class="skill-card">
        <h3>Management &amp; Tools</h3>
        <ul>
          <li>MS Project</li>
          <li>JIRA</li>
          <li>HubSpot</li>
          <li>Advanced Excel</li>
          <li>Process Documentation</li>
        </ul>
      </div>
      <div class="skill-card">
        <h3>Soft Skills</h3>
        <ul>
          <li>Workshop Facilitation</li>
          <li>Stakeholder Support</li>
          <li>Cross-Functional Comms</li>
        </ul>
      </div>
      <div class="skill-card">
        <h3>Languages</h3>
        <ul>
          <li>English — Native/Fluent</li>
          <li>French — A2/B1, progressing</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ================= CERTIFICATIONS ================= -->
<section id="certifications" class="section-pad">
  <div class="wrap reveal">
    <div class="section-head">
      <h2 class="section-title">Certifications</h2>
      <span class="sheet-tag">Credentials · Sheet 03</span>
    </div>
    <div class="cert-list frame" style="padding:8px 28px;">
      <div class="cert-row">
        <div><div class="cert-name">Claude with the Anthropic API</div><div class="cert-issuer">Anthropic Academy</div></div>
        <div class="cert-date">2026</div>
      </div>
      <div class="cert-row">
        <div><div class="cert-name">Model Context Protocol: Advanced Topics</div><div class="cert-issuer">Anthropic Academy</div></div>
        <div class="cert-date">2026</div>
      </div>
      <div class="cert-row">
        <div><div class="cert-name">AI Literacy &amp; AI Fluency</div><div class="cert-issuer">DataCamp / Anthropic Academy</div></div>
        <div class="cert-date">2025–2026</div>
      </div>
      <div class="cert-row">
        <div><div class="cert-name">HubSpot Revenue Operations Certified</div><div class="cert-issuer">HubSpot Academy</div></div>
        <div class="cert-date">Jul 2026</div>
      </div>
      <div class="cert-row">
        <div><div class="cert-name">Customer Relationship Management</div><div class="cert-issuer">HP LIFE / HP Foundation</div></div>
        <div class="cert-date">Jul 2026</div>
      </div>
      <div class="cert-row">
        <div><div class="cert-name">Google Project Management Professional Certificate</div><div class="cert-issuer">Coursera</div></div>
        <div class="cert-date">Apr 2026</div>
      </div>
    </div>
  </div>
</section>

<!-- ================= PROJECTS ================= -->
<section id="work" class="section-pad" style="background:var(--paper-2);">
  <div class="wrap reveal">
    <div class="section-head">
      <h2 class="section-title">Selected Work</h2>
      <span class="sheet-tag">Case Studies · Sheet 04</span>
    </div>

    <div class="project-card">
      <div class="titleblock">
        <div class="tb-left">
          <span class="sheet-tag">Project 01 — No-Code / ESG</span>
          <h3>Green Office Tracker</h3>
        </div>
        <div class="tb-right">MAR 2026<br>SKEMA BUSINESS SCHOOL</div>
      </div>
      <p class="project-org">Low-code ESG analytics platform, built solo in a 7-day sprint.</p>
      <div class="project-cols">
        <div>
          <h4>Objective</h4>
          <p>Replace a manual, spreadsheet-driven ESG reporting process with something the sustainability team could run without a developer on call.</p>
        </div>
        <div>
          <h4>Approach</h4>
          <p>Designed and shipped a custom Power Apps dashboard, then documented and tested it specifically so non-technical users could manage the data and trust the output on their own.</p>
        </div>
        <div>
          <h4>Outcome</h4>
          <p>A self-serve ESG dashboard now in use with zero dependency on me to operate it — the actual measure of success for a tool meant to disappear into the workflow.</p>
        </div>
      </div>
      <div class="chip-row">
        <span class="chip">Shipped solo</span>
        <span class="chip">7-day build</span>
        <span class="chip">Zero-touch adoption</span>
      </div>
    </div>

    <div class="project-card">
      <div class="titleblock">
        <div class="tb-left">
          <span class="sheet-tag">Project 02 — Strategy Simulation</span>
          <h3>Brand PRO</h3>
        </div>
        <div class="tb-right">AUG – DEC 2025<br>SKEMA BUSINESS SCHOOL</div>
      </div>
      <p class="project-org">Cross-functional business strategy simulation, 5 international teams, 26 cycles.</p>
      <div class="project-cols">
        <div>
          <h4>Objective</h4>
          <p>Keep five international teams aligned on shared, complex project goals across 26 rolling decision cycles.</p>
        </div>
        <div>
          <h4>Approach</h4>
          <p>Acted as the coordination bridge across teams — surfacing conflicts early, standardizing how decisions were communicated cycle over cycle.</p>
        </div>
        <div>
          <h4>Outcome</h4>
          <p>Governance held across all 26 cycles with no team drifting out of alignment — the facilitation instinct I now bring to any multi-stakeholder room.</p>
        </div>
      </div>
      <div class="chip-row">
        <span class="chip">5 international teams</span>
        <span class="chip">26 cycles, 0 misalignment</span>
      </div>
    </div>
  </div>
</section>

<!-- ================= EXPERIENCE ================= -->
<section id="experience" class="section-pad">
  <div class="wrap reveal">
    <div class="section-head">
      <h2 class="section-title">Experience</h2>
      <span class="sheet-tag">Timeline · Sheet 05</span>
    </div>
    <div class="ruler">
      <div class="exp-item">
        <div class="exp-role">Talent Acquisition &amp; HR Operations Specialist</div>
        <div class="exp-org">ADEPT People Staffing Solutions Pvt. Ltd., Hyderabad, India</div>
        <span class="exp-date mono">DEC 2024 – FEB 2025</span>
        <p class="exp-desc">Sole point of contact for corporate clients and candidates alike — explaining process, resolving confusion, and keeping 250+ records straight across Excel and Google Sheets.</p>
      </div>
      <div class="exp-item">
        <div class="exp-role">Business Operations &amp; People Experience Manager</div>
        <div class="exp-org">Pallavi Catering and Food Services, India (family-owned, 15+ employees)</div>
        <span class="exp-date mono">AUG 2022 – DEC 2024</span>
        <p class="exp-desc">Coordinated 100+ live events and briefed a 15+ person team — comfortable running the room, not just the spreadsheet behind it.</p>
      </div>
    </div>
  </div>
</section>

<!-- ================= EDUCATION ================= -->
<section id="education" class="section-pad" style="background:var(--paper-2);">
  <div class="wrap reveal">
    <div class="section-head">
      <h2 class="section-title">Education</h2>
      <span class="sheet-tag">Foundations · Sheet 06</span>
    </div>
    <div class="edu-grid">
      <div class="edu-card frame">
        <span class="sheet-tag">M2 · Bac+5 · French System</span>
        <h3>MSc Project Management and Business Development</h3>
        <div class="org">SKEMA Business School, Grand Paris Campus</div>
        <span class="date mono">SEP 2025 – MAY 2027</span>
      </div>
      <div class="edu-card frame">
        <span class="sheet-tag">Undergraduate</span>
        <h3>B.Tech, Civil Engineering</h3>
        <div class="org">JNTU College of Engineering, Hyderabad, India</div>
        <span class="date mono">AUG 2018 – MAY 2022</span>
      </div>
    </div>
  </div>
</section>

<!-- ================= CONTACT ================= -->
<section id="contact" class="contact">
  <div class="wrap reveal">
    <p class="eyebrow">Sheet 07 — Get in touch</p>
    <h2>Let's build the next bridge.</h2>
    <p>Available for internship from September 2026 to February 2027. If you need someone who can prototype the tool and teach the room to use it, I'd welcome the conversation — no pitch required, just fifteen minutes.</p>
    <div class="contact-ctas">
      <a class="btn btn-primary" href="mailto:saishiva.balaboina@skema.edu">Email me</a>
      <a class="btn btn-ghost" href="https://linkedin.com/in/saishiva082000" target="_blank" rel="noopener">Connect on LinkedIn</a>
      <a class="btn btn-resume" href="Sai_Shiva_Balaboina_Resume_SKEMA_AI_Project_Assistant.docx" download>Download résumé</a>
    </div>
  </div>
</section>

<footer>SAI SHIVA BALABOINA — PARIS, FRANCE — REV. JUL 2026</footer>

<a href="#contact" class="float-cta" id="floatCta">
  <svg width="13" height="13" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2"><path d="M4 4h16v12H8l-4 4V4z"/></svg>
  Let's connect
</a>

<script>
  // scroll reveal
  const observer = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); observer.unobserve(e.target); } });
  }, { threshold:0.12 });
  document.querySelectorAll('.reveal').forEach(el=>observer.observe(el));

  // floating CTA: show after hero, hide once contact is in view
  const floatCta = document.getElementById('floatCta');
  const heroEl = document.querySelector('.hero');
  const contactEl = document.getElementById('contact');
  const heroObs = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(!e.isIntersecting && e.boundingClientRect.top < 0){ floatCta.classList.add('show'); } else { floatCta.classList.remove('show'); } });
  }, { threshold:0 });
  heroObs.observe(heroEl);
  const contactObs = new IntersectionObserver((entries)=>{
    entries.forEach(e=>{ if(e.isIntersecting){ floatCta.classList.remove('show'); } });
  }, { threshold:0.2 });
  contactObs.observe(contactEl);
</script>
</body>
</html>
