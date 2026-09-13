

<!DOCTYPE html>
<html>
<head>
<style>
  /* Container for the entire README – dark cyber theme */
  body {
    background: #0a0f1e;
    color: #e0e0e0;
    font-family: 'Fira Code', 'Courier New', monospace;
    padding: 2rem;
    max-width: 900px;
    margin: auto;
  }

  /* Glitch effect for main name */
  @keyframes glitch {
    0% { text-shadow: 2px 2px 0 #ff00c1, -2px -2px 0 #00fff9; }
    25% { text-shadow: -2px 2px 0 #ff00c1, 2px -2px 0 #00fff9; }
    50% { text-shadow: 3px -1px 0 #ff00c1, -3px 1px 0 #00fff9; }
    75% { text-shadow: 1px 3px 0 #ff00c1, -1px -3px 0 #00fff9; }
    100% { text-shadow: 2px 2px 0 #ff00c1, -2px -2px 0 #00fff9; }
  }
  .glitch-text {
    font-size: 2.8rem;
    font-weight: bold;
    animation: glitch 1.2s infinite step-end;
    color: #fff;
    display: inline-block;
  }

  /* Typewriter for subtitle */
  @keyframes typing {
    from { width: 0; }
    to { width: 100%; }
  }
  @keyframes blink-caret {
    50% { border-color: transparent; }
  }
  .typewriter {
    overflow: hidden;
    white-space: nowrap;
    border-right: 3px solid #00ffff;
    animation: typing 3s steps(30) 1s forwards, blink-caret 0.75s step-end infinite;
    width: 0;
    font-size: 1.3rem;
    color: #00d4ff;
    margin: 20px 0;
  }

  /* Pulsing neon badge */
  @keyframes neon-pulse {
    0%, 100% { text-shadow: 0 0 5px #ff007f, 0 0 10px #ff007f; }
    50% { text-shadow: 0 0 20px #ff007f, 0 0 30px #ff007f, 0 0 40px #ff007f; }
  }
  .pulse-badge {
    display: inline-block;
    padding: 8px 18px;
    border: 2px solid #ff007f;
    border-radius: 50px;
    background: #1a1a2e;
    animation: neon-pulse 1.8s ease-in-out infinite;
    margin: 6px;
  }

  /* Slide in from left for skills */
  @keyframes slide-left {
    from { transform: translateX(-100px); opacity: 0; }
    to { transform: translateX(0); opacity: 1; }
  }
  .slide-item {
    display: inline-block;
    animation: slide-left 0.6s ease-out forwards;
    opacity: 0;
    margin-right: 10px;
    background: #16213e;
    padding: 5px 12px;
    border-radius: 20px;
    color: #a0f0ff;
  }

  /* Fade-in with bounce */
  @keyframes bounceIn {
    0% { transform: scale(0.3); opacity: 0; }
    50% { transform: scale(1.05); }
    70% { transform: scale(0.9); }
    100% { transform: scale(1); opacity: 1; }
  }
  .bounce-text {
    animation: bounceIn 1.2s ease-out;
    display: inline-block;
  }

  /* Rotating gear icon (SVG animated) */
  @keyframes spin {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }
  .gear-svg {
    animation: spin 4s linear infinite;
    display: inline-block;
    vertical-align: middle;
  }

  /* Drifting binary text */
  @keyframes drift {
    0% { transform: translateY(0px); }
    50% { transform: translateY(-10px); }
    100% { transform: translateY(0px); }
  }
  .binary-drift {
    display: inline-block;
    animation: drift 3s ease-in-out infinite;
    color: #39ff14;
    font-size: 0.8rem;
  }

  /* Float effect for stats */
  @keyframes float {
    0% { transform: translateY(0px); }
    50% { transform: translateY(-8px); }
    100% { transform: translateY(0px); }
  }
  .float-card {
    display: inline-block;
    animation: float 3s ease-in-out infinite;
    background: #1c2541;
    padding: 10px 20px;
    border-radius: 12px;
    margin: 8px;
  }

  /* Scan lines (mask) */
  .scanlines {
    position: relative;
  }
  .scanlines::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      rgba(255,255,255,0.03) 2px,
      rgba(255,255,255,0.03) 4px
    );
    pointer-events: none;
  }
</style>
</head>
<body class="scanlines">

<!-- HEADER with glitch effect -->
<div style="text-align: center; margin-bottom: 15px;">
  <span class="glitch-text">NOVA144Hz</span>
  <br>
  <!-- Typewriter subtitle -->
  <div class="typewriter">Cybersecurity Reversal & Software Engineer</div>
</div>

<!-- Animated SVG badge – pulse + gear -->
<div style="text-align: center;">
  <span class="pulse-badge">
    <svg class="gear-svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#ff007f" stroke-width="2">
      <path d="M12 2l2 4h4l1 3-3 3 1 4-4 1-3-3-4 1 1-4-3-3 1-3h4z"/>
    </svg>
    &#160;Reverse Engineer
  </span>
  <span class="pulse-badge" style="animation-delay: 0.6s;">
    <svg class="gear-svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#00fff9" stroke-width="2">
      <circle cx="12" cy="12" r="3"/>
      <path d="M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42"/>
    </svg>
    &#160;Software Engineer
  </span>
</div>

<!-- Skills with unique animations per skill -->
<div style="margin: 30px 0;">
  <span class="slide-item" style="animation-delay: 0.1s;">🔧 Reverse Engineering</span>
  <span class="slide-item" style="animation-delay: 0.2s;">💻 Python / C++ / Rust</span>
  <span class="slide-item" style="animation-delay: 0.3s;">🛡️ Exploit Dev</span>
  <span class="slide-item" style="animation-delay: 0.4s;">🧠 Malware Analysis</span>
  <span class="slide-item" style="animation-delay: 0.5s;">🌐 Binary Exploitation</span>
  <span class="slide-item" style="animation-delay: 0.6s;">⚙️ Fuzzing / SMT</span>
  <span class="slide-item" style="animation-delay: 0.7s;">🔬 OSINT</span>
  <span class="slide-item" style="animation-delay: 0.8s;">🕵️‍♂️ Forensics</span>
</div>

<!-- Stats cards with float -->
<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px; margin: 25px 0;">
  <div class="float-card" style="animation-delay: 0s;">
    <span style="font-size: 1.5rem;">🔓</span><br>
    <span style="color: #ff007f; font-weight: bold;">1,247</span> Repos
  </div>
  <div class="float-card" style="animation-delay: 0.5s;">
    <span style="font-size: 1.5rem;">⚠️</span><br>
    <span style="color: #ffaa00;">14</span> CVEs
  </div>
  <div class="float-card" style="animation-delay: 1s;">
    <span style="font-size: 1.5rem;">🧩</span><br>
    <span style="color: #00ff88;">90%</span> Code Coverage
  </div>
</div>

<!-- Drifting binary line (each char has own animation? But block is fine) -->
<div style="text-align: center; margin: 20px 0;">
  <span class="binary-drift" style="animation-duration: 2s;">0</span>
  <span class="binary-drift" style="animation-duration: 2.3s;">1</span>
  <span class="binary-drift" style="animation-duration: 2.7s;">1</span>
  <span class="binary-drift" style="animation-duration: 1.9s;">0</span>
  <span class="binary-drift" style="animation-duration: 3.1s;">1</span>
  <span class="binary-drift" style="animation-duration: 2.5s;">0</span>
  <span class="binary-drift" style="animation-duration: 2.2s;">1</span>
  <span class="binary-drift" style="animation-duration: 2.8s;">1</span>
  <span class="binary-drift" style="animation-duration: 1.8s;">0</span>
  <span class="binary-drift" style="animation-duration: 2.6s;">1</span>
  <span class="binary-drift" style="animation-duration: 3.0s;">0</span>
  <span class="binary-drift" style="animation-duration: 2.1s;">1</span>
</div>

<!-- Quote with bounce -->
<div style="text-align: center; margin-top: 30px; font-size: 1.1rem;">
  <span class="bounce-text" style="color: #9d4edd;">"In reversing we trust. Every byte has a story."</span>
</div>

<!-- Footer with glow drift -->
<div style="margin-top: 40px; text-align: center;">
  <span style="display: inline-block; animation: neon-pulse 2.5s infinite alternate; color: #b200ff;">
    🔥 NOVA144Hz · 0xDEADBEEF 🔥
  </span>
  <br><br>
  <!-- Animated SVG indicator (pulse circle) -->
  <svg width="30" height="30" viewBox="0 0 30 30" style="animation: neon-pulse 1s infinite;">
    <circle cx="15" cy="15" r="10" fill="#ff00c1" opacity="0.8"/>
    <circle cx="15" cy="15" r="5" fill="white" opacity="0.6"/>
  </svg>
</div>

</body>
</html>
