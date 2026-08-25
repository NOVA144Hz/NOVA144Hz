<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NOVA — GitHub Profile README</title>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;600;700&family=Share+Tech+Mono&family=Noto+Sans+JP:wght@300;400;700&display=swap" rel="stylesheet">
<style>
  :root {
    --bg:       #0a0a0f;
    --panel:    #10101a;
    --border:   #2a1a2e;
    --accent1:  #ff2d55;   /* Zero Two crimson */
    --accent2:  #c084fc;   /* soft violet */
    --accent3:  #38bdf8;   /* cyber blue */
    --text:     #e2d9f3;
    --muted:    #6b5f7a;
    --gold:     #fbbf24;
    --green:    #4ade80;
    --mono:     'Share Tech Mono', monospace;
    --display:  'Rajdhani', sans-serif;
    --jp:       'Noto Sans JP', sans-serif;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--display);
    min-height: 100vh;
    overflow-x: hidden;
    position: relative;
  }

  /* ── SAKURA PARTICLES ── */
  #sakura-canvas {
    position: fixed; inset: 0;
    pointer-events: none;
    z-index: 0;
    opacity: .35;
  }

  /* ── SCANLINE OVERLAY ── */
  body::after {
    content: '';
    position: fixed; inset: 0;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(0,0,0,.08) 2px,
      rgba(0,0,0,.08) 4px
    );
    pointer-events: none;
    z-index: 1000;
  }

  .wrapper {
    position: relative;
    z-index: 1;
    max-width: 860px;
    margin: 0 auto;
    padding: 2rem 1.5rem 4rem;
  }

  /* ── HERO ── */
  .hero {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 2rem;
    align-items: center;
    padding: 2.5rem 2rem;
    background: linear-gradient(135deg, #14001a 0%, #0a0a0f 60%);
    border: 1px solid var(--accent1);
    border-radius: 4px;
    position: relative;
    overflow: hidden;
    margin-bottom: 1.5rem;
    animation: borderPulse 4s ease-in-out infinite;
  }

  @keyframes borderPulse {
    0%,100% { box-shadow: 0 0 8px var(--accent1), inset 0 0 20px rgba(255,45,85,.04); }
    50%      { box-shadow: 0 0 24px var(--accent1), inset 0 0 40px rgba(255,45,85,.08); }
  }

  /* diagonal stripe decoration */
  .hero::before {
    content: '';
    position: absolute;
    top: -40px; right: -40px;
    width: 200px; height: 200px;
    background: conic-gradient(from 45deg, var(--accent1) 0deg 45deg, transparent 45deg 360deg);
    opacity: .07;
    border-radius: 50%;
  }

  .avatar-ring {
    width: 110px; height: 110px;
    border-radius: 50%;
    background: linear-gradient(135deg, var(--accent1), var(--accent2));
    padding: 3px;
    animation: spin 8s linear infinite;
    flex-shrink: 0;
  }

  @keyframes spin {
    to { transform: rotate(360deg); }
  }

  .avatar-inner {
    width: 100%; height: 100%;
    border-radius: 50%;
    background: var(--bg);
    display: flex; align-items: center; justify-content: center;
    font-size: 3.5rem;
    animation: spin 8s linear infinite reverse;
  }

  .hero-text h1 {
    font-family: var(--display);
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 700;
    letter-spacing: .12em;
    color: var(--text);
    line-height: 1;
  }

  .hero-text h1 span { color: var(--accent1); }

  .jp-subtitle {
    font-family: var(--jp);
    font-size: .75rem;
    color: var(--muted);
    letter-spacing: .2em;
    margin: .3rem 0 .8rem;
  }

  #typewriter {
    font-family: var(--mono);
    font-size: .95rem;
    color: var(--accent3);
    min-height: 1.4em;
  }

  #typewriter::after {
    content: '█';
    animation: blink .7s step-end infinite;
  }

  @keyframes blink { 50% { opacity: 0; } }

  .badges {
    display: flex; flex-wrap: wrap; gap: .5rem;
    margin-top: 1rem;
  }

  .badge {
    font-family: var(--mono);
    font-size: .7rem;
    padding: .2rem .6rem;
    border-radius: 2px;
    letter-spacing: .08em;
    text-transform: uppercase;
    border: 1px solid;
    animation: badgeFade .5s ease forwards;
    opacity: 0;
  }

  .badge-red   { color: var(--accent1); border-color: var(--accent1); background: rgba(255,45,85,.08); }
  .badge-blue  { color: var(--accent3); border-color: var(--accent3); background: rgba(56,189,248,.08); }
  .badge-purp  { color: var(--accent2); border-color: var(--accent2); background: rgba(192,132,252,.08); }
  .badge-gold  { color: var(--gold);   border-color: var(--gold);   background: rgba(251,191,36,.08); }

  @keyframes badgeFade { to { opacity: 1; } }

  /* ── DIVIDER ── */
  .divider {
    display: flex; align-items: center; gap: 1rem;
    margin: 1.5rem 0;
    color: var(--muted);
    font-family: var(--mono);
    font-size: .7rem;
    letter-spacing: .15em;
  }
  .divider::before, .divider::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
  }

  /* ── SECTION HEADER ── */
  .section-head {
    font-family: var(--display);
    font-size: 1.1rem;
    font-weight: 700;
    letter-spacing: .2em;
    text-transform: uppercase;
    color: var(--accent1);
    margin-bottom: 1rem;
    display: flex; align-items: center; gap: .5rem;
  }
  .section-head::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--accent1), transparent);
    opacity: .4;
  }

  /* ── ABOUT PANEL ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-bottom: 1.5rem;
  }

  .panel {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 1.2rem 1.4rem;
    transition: border-color .3s, box-shadow .3s;
  }
  .panel:hover {
    border-color: var(--accent2);
    box-shadow: 0 0 12px rgba(192,132,252,.15);
  }

  .panel-title {
    font-family: var(--mono);
    font-size: .65rem;
    letter-spacing: .2em;
    color: var(--muted);
    text-transform: uppercase;
    margin-bottom: .7rem;
  }

  .panel p {
    font-size: .9rem;
    line-height: 1.6;
    color: var(--text);
  }

  .panel p .highlight {
    color: var(--accent2);
    font-weight: 600;
  }

  /* ── SKILL BARS ── */
  .skill-bars { display: flex; flex-direction: column; gap: .7rem; margin-bottom: 1.5rem; }

  .skill-row { display: grid; grid-template-columns: 140px 1fr 38px; align-items: center; gap: .8rem; }

  .skill-label {
    font-family: var(--mono);
    font-size: .75rem;
    color: var(--text);
    letter-spacing: .05em;
  }

  .bar-track {
    height: 6px;
    background: var(--border);
    border-radius: 3px;
    overflow: hidden;
  }

  .bar-fill {
    height: 100%;
    border-radius: 3px;
    width: 0;
    transition: width 1.6s cubic-bezier(.22,1,.36,1);
  }

  .bar-fill.red   { background: linear-gradient(90deg, var(--accent1), #ff6b88); }
  .bar-fill.blue  { background: linear-gradient(90deg, var(--accent3), #7dd3fc); }
  .bar-fill.purp  { background: linear-gradient(90deg, var(--accent2), #e879f9); }
  .bar-fill.gold  { background: linear-gradient(90deg, var(--gold), #fde68a); }
  .bar-fill.green { background: linear-gradient(90deg, var(--green), #86efac); }

  .bar-pct {
    font-family: var(--mono);
    font-size: .7rem;
    color: var(--muted);
    text-align: right;
  }

  /* ── STAT CARDS ── */
  .stat-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    margin-bottom: 1.5rem;
  }

  .stat-card {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 1.2rem;
    text-align: center;
    position: relative;
    overflow: hidden;
    transition: transform .2s, box-shadow .2s;
  }
  .stat-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(0,0,0,.4);
  }

  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
  }
  .stat-card.s1::before { background: var(--accent1); }
  .stat-card.s2::before { background: var(--accent3); }
  .stat-card.s3::before { background: var(--accent2); }
  .stat-card.s4::before { background: var(--gold); }
  .stat-card.s5::before { background: var(--green); }
  .stat-card.s6::before { background: #f97316; }

  .stat-icon { font-size: 1.6rem; margin-bottom: .3rem; }
  .stat-value {
    font-family: var(--display);
    font-size: 1.7rem;
    font-weight: 700;
    line-height: 1;
  }
  .stat-label {
    font-family: var(--mono);
    font-size: .6rem;
    color: var(--muted);
    letter-spacing: .12em;
    text-transform: uppercase;
    margin-top: .3rem;
  }

  .s1 .stat-value { color: var(--accent1); }
  .s2 .stat-value { color: var(--accent3); }
  .s3 .stat-value { color: var(--accent2); }
  .s4 .stat-value { color: var(--gold); }
  .s5 .stat-value { color: var(--green); }
  .s6 .stat-value { color: #f97316; }

  /* ── PROJECT CARDS ── */
  .project-list { display: flex; flex-direction: column; gap: .8rem; margin-bottom: 1.5rem; }

  .project-card {
    background: var(--panel);
    border: 1px solid var(--border);
    border-left: 3px solid var(--accent1);
    border-radius: 0 4px 4px 0;
    padding: 1rem 1.2rem;
    display: flex; justify-content: space-between; align-items: flex-start;
    transition: border-color .3s, box-shadow .2s;
  }
  .project-card:nth-child(2) { border-left-color: var(--accent3); }
  .project-card:nth-child(3) { border-left-color: var(--accent2); }
  .project-card:nth-child(4) { border-left-color: var(--gold); }
  .project-card:hover { box-shadow: 0 4px 16px rgba(0,0,0,.4); }

  .project-name {
    font-family: var(--display);
    font-size: 1rem;
    font-weight: 700;
    letter-spacing: .08em;
    color: var(--text);
  }
  .project-desc {
    font-family: var(--mono);
    font-size: .72rem;
    color: var(--muted);
    margin-top: .25rem;
    line-height: 1.5;
  }
  .project-tags { display: flex; gap: .4rem; flex-wrap: wrap; margin-top: .5rem; }
  .tag {
    font-family: var(--mono);
    font-size: .6rem;
    padding: .1rem .4rem;
    border-radius: 2px;
    background: rgba(255,255,255,.04);
    border: 1px solid var(--border);
    color: var(--muted);
  }
  .project-status {
    font-family: var(--mono);
    font-size: .6rem;
    white-space: nowrap;
    padding: .2rem .6rem;
    border-radius: 2px;
    margin-left: 1rem;
    flex-shrink: 0;
  }
  .status-active { background: rgba(74,222,128,.1); color: var(--green); border: 1px solid var(--green); }
  .status-wip    { background: rgba(251,191,36,.1);  color: var(--gold);  border: 1px solid var(--gold); }

  /* ── QUOTE BLOCK ── */
  .quote-block {
    background: linear-gradient(135deg, #14001a 0%, var(--panel) 100%);
    border: 1px solid var(--accent1);
    border-radius: 4px;
    padding: 1.5rem 2rem;
    text-align: center;
    position: relative;
    margin-bottom: 1.5rem;
    animation: borderPulse 4s ease-in-out infinite 2s;
  }
  .quote-text {
    font-family: var(--jp);
    font-size: 1rem;
    color: var(--accent2);
    font-style: italic;
    margin-bottom: .4rem;
    letter-spacing: .05em;
  }
  .quote-src {
    font-family: var(--mono);
    font-size: .65rem;
    color: var(--muted);
    letter-spacing: .15em;
  }
  .quote-block::before {
    content: '❝';
    position: absolute;
    top: .5rem; left: 1rem;
    font-size: 2rem;
    color: var(--accent1);
    opacity: .3;
    line-height: 1;
  }

  /* ── CONNECT ROW ── */
  .connect-row {
    display: flex; gap: .7rem; flex-wrap: wrap;
    justify-content: center;
    margin-top: .5rem;
  }

  .connect-btn {
    font-family: var(--mono);
    font-size: .75rem;
    padding: .5rem 1.1rem;
    border-radius: 3px;
    border: 1px solid var(--border);
    background: var(--panel);
    color: var(--text);
    cursor: pointer;
    letter-spacing: .1em;
    text-transform: uppercase;
    transition: border-color .2s, color .2s, box-shadow .2s;
    text-decoration: none;
  }
  .connect-btn:hover {
    border-color: var(--accent1);
    color: var(--accent1);
    box-shadow: 0 0 8px rgba(255,45,85,.2);
  }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    font-family: var(--mono);
    font-size: .65rem;
    color: var(--muted);
    letter-spacing: .12em;
    margin-top: 2rem;
    padding-top: 1rem;
    border-top: 1px solid var(--border);
  }
  .footer span { color: var(--accent1); }

  /* ── RESPONSIVE ── */
  @media (max-width: 600px) {
    .hero { grid-template-columns: 1fr; text-align: center; }
    .badges { justify-content: center; }
    .about-grid, .stat-grid { grid-template-columns: 1fr; }
    .avatar-ring { margin: 0 auto; }
  }

  /* ── ENTRANCE ANIMATIONS ── */
  .fade-up {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity .6s ease, transform .6s ease;
  }
  .fade-up.visible {
    opacity: 1;
    transform: translateY(0);
  }
</style>
</head>
<body>

<canvas id="sakura-canvas"></canvas>

<div class="wrapper">

  <!-- HERO -->
  <section class="hero fade-up">
    <div class="avatar-ring">
      <div class="avatar-inner">🌸</div>
    </div>
    <div class="hero-text">
      <h1>N<span>OV</span>A</h1>
      <p class="jp-subtitle">ノヴァ &nbsp;／&nbsp; Dixit &nbsp;／&nbsp; RTU · CSE</p>
      <div id="typewriter"></div>
      <div class="badges">
        <span class="badge badge-red">C++ Dev</span>
        <span class="badge badge-blue">Discord Engineer</span>
        <span class="badge badge-purp">Anime Fan</span>
        <span class="badge badge-gold">Valorant Player</span>
        <span class="badge badge-red">System Builder</span>
        <span class="badge badge-blue">B.Tech CSE</span>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <div class="divider fade-up">// OPERATOR FILE //</div>
  <div class="section-head fade-up">About</div>

  <div class="about-grid fade-up">
    <div class="panel">
      <div class="panel-title">// identity</div>
      <p>
        <span class="highlight">NOVA</span> — a 19-year-old builder from
        <span class="highlight">Banswara, Rajasthan</span> deep in a B.Tech CSE grind at RTU.
        The kind of dev who doesn't just study code — builds entire ecosystems around it.
        Aesthetic driven. Zero Two enjoyer. Serious about craft.
      </p>
    </div>
    <div class="panel">
      <div class="panel-title">// current mission</div>
      <p>
        Architecting the <span class="highlight">NOVA ecosystem</span> — a multi-layered
        platform spanning a Railway-deployed Discord bot, a PySide6 desktop dashboard,
        and a Game Hub with Discord Rich Presence. C++ is the weapon of choice.
      </p>
    </div>
  </div>

  <!-- SKILL BARS -->
  <div class="section-head fade-up">Skill Levels</div>
  <div class="skill-bars fade-up" id="skill-bars">
    <div class="skill-row">
      <span class="skill-label">C++</span>
      <div class="bar-track"><div class="bar-fill red" data-w="72"></div></div>
      <span class="bar-pct">72%</span>
    </div>
    <div class="skill-row">
      <span class="skill-label">Python</span>
      <div class="bar-track"><div class="bar-fill blue" data-w="68"></div></div>
      <span class="bar-pct">68%</span>
    </div>
    <div class="skill-row">
      <span class="skill-label">Discord Bots</span>
      <div class="bar-track"><div class="bar-fill purp" data-w="80"></div></div>
      <span class="bar-pct">80%</span>
    </div>
    <div class="skill-row">
      <span class="skill-label">System Design</span>
      <div class="bar-track"><div class="bar-fill gold" data-w="60"></div></div>
      <span class="bar-pct">60%</span>
    </div>
    <div class="skill-row">
      <span class="skill-label">C# / WinForms</span>
      <div class="bar-track"><div class="bar-fill green" data-w="55"></div></div>
      <span class="bar-pct">55%</span>
    </div>
    <div class="skill-row">
      <span class="skill-label">Deployment (Railway)</span>
      <div class="bar-track"><div class="bar-fill red" data-w="65"></div></div>
      <span class="bar-pct">65%</span>
    </div>
  </div>

  <!-- STAT CARDS -->
  <div class="section-head fade-up">Stats</div>
  <div class="stat-grid fade-up">
    <div class="stat-card s1">
      <div class="stat-icon">⚔️</div>
      <div class="stat-value">4</div>
      <div class="stat-label">Live Projects</div>
    </div>
    <div class="stat-card s2">
      <div class="stat-icon">🛠️</div>
      <div class="stat-value">3</div>
      <div class="stat-label">Languages Active</div>
    </div>
    <div class="stat-card s3">
      <div class="stat-icon">🤖</div>
      <div class="stat-value">1</div>
      <div class="stat-label">Bot Deployed</div>
    </div>
    <div class="stat-card s4">
      <div class="stat-icon">🌸</div>
      <div class="stat-value">∞</div>
      <div class="stat-label">Anime Episodes</div>
    </div>
    <div class="stat-card s5">
      <div class="stat-icon">🎮</div>
      <div class="stat-value">GE</div>
      <div class="stat-label">Valorant Rank</div>
    </div>
    <div class="stat-card s6">
      <div class="stat-icon">☕</div>
      <div class="stat-value">99</div>
      <div class="stat-label">Debug Sessions</div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section-head fade-up">Active Builds</div>
  <div class="project-list fade-up">

    <div class="project-card">
      <div>
        <div class="project-name">🤖 NOVA Discord Bot</div>
        <div class="project-desc">Free Fire stat bot with slash commands, deployed on Railway. Built from scratch — auth, env vars, crash recovery, the works.</div>
        <div class="project-tags">
          <span class="tag">Python</span>
          <span class="tag">discord.py</span>
          <span class="tag">Railway</span>
          <span class="tag">REST API</span>
        </div>
      </div>
      <span class="project-status status-active">LIVE</span>
    </div>

    <div class="project-card">
      <div>
        <div class="project-name">🎮 NOVA Game Hub</div>
        <div class="project-desc">Discord Rich Presence launcher tracking active games via psutil + pypresence. Personal-brand-first design.</div>
        <div class="project-tags">
          <span class="tag">Python</span>
          <span class="tag">pypresence</span>
          <span class="tag">psutil</span>
          <span class="tag">PySide6</span>
        </div>
      </div>
      <span class="project-status status-wip">WIP</span>
    </div>

    <div class="project-card">
      <div>
        <div class="project-name">🔐 C++ Auth Panel</div>
        <div class="project-desc">KeyAuth-style admin + licensing system. Crow HTTP server, Qt6 UI, MySQL backend, JWT tokens — real production architecture.</div>
        <div class="project-tags">
          <span class="tag">C++</span>
          <span class="tag">Crow</span>
          <span class="tag">Qt6</span>
          <span class="tag">MySQL</span>
          <span class="tag">JWT</span>
        </div>
      </div>
      <span class="project-status status-active">BUILT</span>
    </div>

    <div class="project-card">
      <div>
        <div class="project-name">🌌 Asteroid Field Effect</div>
        <div class="project-desc">144Hz-optimised C# WinForms ambient visual. Pure style experiment — NOVA's aesthetic in code form.</div>
        <div class="project-tags">
          <span class="tag">C#</span>
          <span class="tag">WinForms</span>
          <span class="tag">GDI+</span>
        </div>
      </div>
      <span class="project-status status-active">COMPLETE</span>
    </div>

  </div>

  <!-- QUOTE -->
  <div class="quote-block fade-up">
    <p class="quote-text">"I am Zero Two. The partner who carries you — and the storm that never stops."</p>
    <p class="quote-src">— Darling in the FranXX &nbsp;·&nbsp; NOVA's spirit animal</p>
  </div>

  <!-- CONNECT -->
  <div class="divider fade-up">// SIGNAL LINK //</div>
  <div class="section-head fade-up">Connect</div>
  <div class="connect-row fade-up">
    <a class="connect-btn" href="#">Discord</a>
    <a class="connect-btn" href="#">GitHub</a>
    <a class="connect-btn" href="#">Valorant.gg</a>
    <a class="connect-btn" href="#">Free Fire</a>
  </div>

  <!-- FOOTER -->
  <div class="footer fade-up">
    <p>Made with <span>♥</span> & way too much caffeine &nbsp;·&nbsp; NOVA © 2024 &nbsp;·&nbsp; Banswara, Rajasthan</p>
    <p style="margin-top:.4rem">「まだまだ、始まりだ。」&nbsp;— It's only just beginning.</p>
  </div>

</div>

<script>
// ── SAKURA / PARTICLE CANVAS ──
const canvas = document.getElementById('sakura-canvas');
const ctx = canvas.getContext('2d');

function resize() {
  canvas.width  = window.innerWidth;
  canvas.height = window.innerHeight;
}
resize();
window.addEventListener('resize', resize);

const PETALS = 60;
const petals = Array.from({ length: PETALS }, () => ({
  x: Math.random() * window.innerWidth,
  y: Math.random() * window.innerHeight,
  r: Math.random() * 4 + 2,
  dx: Math.random() * .6 - .3,
  dy: Math.random() * .8 + .3,
  angle: Math.random() * Math.PI * 2,
  spin: Math.random() * .04 - .02,
  alpha: Math.random() * .6 + .2,
  color: Math.random() > .5 ? '#ff2d55' : '#c084fc',
}));

function drawPetal(p) {
  ctx.save();
  ctx.translate(p.x, p.y);
  ctx.rotate(p.angle);
  ctx.globalAlpha = p.alpha;
  ctx.fillStyle = p.color;
  ctx.beginPath();
  ctx.ellipse(0, 0, p.r, p.r * 1.8, 0, 0, Math.PI * 2);
  ctx.fill();
  ctx.restore();
}

function animatePetals() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  for (const p of petals) {
    p.x += p.dx;
    p.y += p.dy;
    p.angle += p.spin;
    if (p.y > canvas.height + 10) {
      p.y = -10;
      p.x = Math.random() * canvas.width;
    }
    drawPetal(p);
  }
  requestAnimationFrame(animatePetals);
}
animatePetals();

// ── TYPEWRITER ──
const lines = [
  'B.Tech CSE @ RTU | Class of \'27',
  'Building the NOVA Ecosystem...',
  'C++ | Python | Discord Engineer',
  'Zero Two sympathizer. Always.',
  'Competitive. Creative. Chaotic.',
];
let li = 0, ci = 0, del = false;
const tw = document.getElementById('typewriter');

function type() {
  const current = lines[li];
  if (!del) {
    tw.textContent = current.slice(0, ++ci);
    if (ci === current.length) { del = true; setTimeout(type, 1800); return; }
  } else {
    tw.textContent = current.slice(0, --ci);
    if (ci === 0) { del = false; li = (li + 1) % lines.length; }
  }
  setTimeout(type, del ? 30 : 60);
}
type();

// ── BADGE STAGGER ──
document.querySelectorAll('.badge').forEach((b, i) => {
  b.style.animationDelay = `${i * .12 + .5}s`;
});

// ── SCROLL FADE IN ──
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: .12 });

document.querySelectorAll('.fade-up').forEach(el => obs.observe(el));

// ── SKILL BAR ANIMATION ──
const barObs = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.querySelectorAll('.bar-fill').forEach(bar => {
        bar.style.width = bar.dataset.w + '%';
      });
      barObs.unobserve(e.target);
    }
  });
}, { threshold: .3 });

const skillSection = document.getElementById('skill-bars');
if (skillSection) barObs.observe(skillSection);
</script>
</body>
</html>
