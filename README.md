<div align="center">

<!-- ═══════════════════════════════════════════════════════════
     NOVA144Hz // QUANTUM CYBERNETIC CORE HUD
     ═══════════════════════════════════════════════════════════ -->
<svg width="100%" height="560" viewBox="0 0 1200 560" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Background Gradients -->
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#020403"/>
      <stop offset="50%" stop-color="#05140f"/>
      <stop offset="100%" stop-color="#000000"/>
    </linearGradient>

    <radialGradient id="radarSweep" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#00ff9c" stop-opacity="0.35"/>
      <stop offset="50%" stop-color="#00ff9c" stop-opacity="0.08"/>
      <stop offset="100%" stop-color="#00ff9c" stop-opacity="0"/>
    </radialGradient>

    <!-- Core glow & Bloom -->
    <radialGradient id="core">
      <stop offset="0%" stop-color="#ffffff"/>
      <stop offset="15%" stop-color="#9affdf"/>
      <stop offset="40%" stop-color="#00ff9c" stop-opacity=".85"/>
      <stop offset="85%" stop-color="#00ff9c" stop-opacity=".15"/>
      <stop offset="100%" stop-color="#00ff9c" stop-opacity="0"/>
    </radialGradient>

    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="4" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <filter id="softGlow" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur stdDeviation="15"/>
    </filter>

    <!-- Matrix Pattern Grids -->
    <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M40 0H0V40" fill="none" stroke="#00ff9c" stroke-opacity=".06"/>
      <circle cx="40" cy="40" r="0.8" fill="#00ff9c" opacity=".2"/>
    </pattern>

    <pattern id="scanlines" width="1" height="6" patternUnits="userSpaceOnUse">
      <rect width="1" height="2" fill="#00ff9c" opacity=".04"/>
    </pattern>
  </defs>

  <!-- CANVAS FOUNDATION -->
  <rect width="1200" height="560" fill="url(#bg)"/>
  <rect width="1200" height="560" fill="url(#grid)"/>
  <rect width="1200" height="560" fill="url(#scanlines)"/>

  <!-- HORIZONTAL & VERTICAL RASTER LASERS -->
  <rect x="0" y="-10" width="1200" height="2" fill="#00ff9c" opacity=".4">
    <animate attributeName="y" from="-10" to="570" dur="3.5s" repeatCount="indefinite"/>
  </rect>
  <rect x="-10" y="0" width="2" height="560" fill="#00ff9c" opacity=".25">
    <animate attributeName="x" from="-10" to="1210" dur="7s" repeatCount="indefinite"/>
  </rect>

  <!-- AMBIENT PULSING DATA PARTICLES -->
  <g fill="#00ff9c">
    <circle cx="85" cy="115" r="1.5"><animate attributeName="opacity" values="0.1;.9;0.1" dur="2.1s" repeatCount="indefinite"/></circle>
    <circle cx="210" cy="380" r="2"><animate attributeName="opacity" values="0.2;1;0.2" dur="3.3s" repeatCount="indefinite"/></circle>
    <circle cx="1020" cy="140" r="2.5"><animate attributeName="opacity" values="0;.8;0" dur="2.4s" repeatCount="indefinite"/></circle>
    <circle cx="1110" cy="360" r="1.5"><animate attributeName="opacity" values="0.3;1;0.3" dur="1.7s" repeatCount="indefinite"/></circle>
    <circle cx="260" cy="85" r="2"><animate attributeName="opacity" values="0;.7;0" dur="2.8s" repeatCount="indefinite"/></circle>
    <circle cx="920" cy="430" r="1.5"><animate attributeName="opacity" values="0.1;.9;0.1" dur="2.6s" repeatCount="indefinite"/></circle>
    <circle cx="510" cy="80" r="1"><animate attributeName="opacity" values="0;1;0" dur="1.9s" repeatCount="indefinite"/></circle>
    <circle cx="690" cy="470" r="1.5"><animate attributeName="opacity" values="0.2;.8;0.2" dur="3s" repeatCount="indefinite"/></circle>
  </g>

  <!-- CORNER TARGETING BRACKETS -->
  <g stroke="#00ff9c" stroke-width="1.5" fill="none" opacity=".7">
    <!-- Top-Left -->
    <path d="M25 80 V25 H80"/>
    <rect x="22" y="22" width="6" height="6" fill="#00ff9c"/>
    <!-- Top-Right -->
    <path d="M1120 25 H1175 V80"/>
    <rect x="1172" y="22" width="6" height="6" fill="#00ff9c"/>
    <!-- Bottom-Left -->
    <path d="M25 480 V535 H80"/>
    <rect x="22" y="532" width="6" height="6" fill="#00ff9c"/>
    <!-- Bottom-Right -->
    <path d="M1120 535 H1175 V480"/>
    <rect x="1172" y="532" width="6" height="6" fill="#00ff9c"/>
  </g>

  <!-- TELEMETRY HUD HEADER READOUTS -->
  <g fill="#00ff9c" font-family="monospace" font-size="11" letter-spacing="2" opacity=".85">
    <text x="45" y="58">SYS_ID // NOVA144Hz</text>
    <text x="45" y="76" font-size="9" fill="#9affdf" opacity=".6">LATENCY: 0.04ms [LOCKED]</text>
    
    <text x="960" y="58">FREQUENCY // 144.00 FPS</text>
    <text x="960" y="76" font-size="9" fill="#9affdf" opacity=".6">SEC_LEVEL // OMNI_ROOT</text>
  </g>

  <!-- CENTRAL ROTATING VECTOR REACTOR -->
  <g transform="translate(600 260)">
    <!-- Outer Field Pulse -->
    <circle r="160" fill="none" stroke="#00ff9c" stroke-width="1" stroke-dasharray="8 12" opacity=".2">
      <animate attributeName="r" values="150;175;150" dur="4s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values=".1;.35;.1" dur="4s" repeatCount="indefinite"/>
    </circle>

    <!-- Radar Sweep Rotor -->
    <path d="M0 0 L130 -60 A145 145 0 0 1 145 0 Z" fill="url(#radarSweep)">
      <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="4s" repeatCount="indefinite"/>
    </path>

    <!-- Outer Segmented Ring -->
    <circle r="135" fill="none" stroke="#00ff9c" stroke-width="1.5" stroke-dasharray="4 16" opacity=".7">
      <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="14s" repeatCount="indefinite"/>
    </circle>

    <!-- Heavy Segmented Ring -->
    <circle r="110" fill="none" stroke="#9affdf" stroke-width="2.5" stroke-dasharray="60 30 10 30" opacity=".65">
      <animateTransform attributeName="transform" type="rotate" from="360" to="0" dur="9s" repeatCount="indefinite"/>
    </circle>

    <!-- Counter-Clockwise Precision Dial -->
    <circle r="85" fill="none" stroke="#00ff9c" stroke-width="1" stroke-dasharray="2 6" opacity=".8">
      <animateTransform attributeName="transform" type="rotate" from="0" to="-360" dur="6s" repeatCount="indefinite"/>
    </circle>

    <!-- Core Bloom & Reaction Chamber -->
    <circle r="75" fill="url(#core)" filter="url(#softGlow)">
      <animate attributeName="r" values="68;82;68" dur="1.8s" repeatCount="indefinite"/>
    </circle>

    <circle r="36" fill="#00ff9c" opacity=".18" filter="url(#glow)"/>

    <!-- High-Rate Inner Tachyon Node -->
    <circle r="18" fill="#00ff9c" filter="url(#glow)">
      <animate attributeName="r" values="15;22;15" dur="0.9s" repeatCount="indefinite"/>
    </circle>
    <circle r="7" fill="#ffffff"/>

    <!-- Satellites & Flux Points -->
    <g>
      <circle cx="110" cy="0" r="3" fill="#ffffff" filter="url(#glow)">
        <animateTransform attributeName="transform" type="rotate" from="0" to="360" dur="3s" repeatCount="indefinite"/>
      </circle>
      <circle cx="-135" cy="0" r="2" fill="#9affdf">
        <animateTransform attributeName="transform" type="rotate" from="360" to="0" dur="5s" repeatCount="indefinite"/>
      </circle>
    </g>
  </g>

  <!-- TACTICAL CROSSHAIRS & MEASUREMENT TICKS -->
  <g stroke="#00ff9c" opacity=".35" stroke-width="1">
    <line x1="390" y1="260" x2="490" y2="260"/>
    <line x1="710" y1="260" x2="810" y2="260"/>
    <line x1="600" y1="80" x2="600" y2="150"/>
    <line x1="600" y1="370" x2="600" y2="440"/>
    <!-- Pitch Markers -->
    <path d="M490 255 V265 M710 255 V265 M595 150 H605 M595 370 H605"/>
  </g>

  <!-- CENTRAL IDENTITY BRANDING -->
  <g text-anchor="middle" font-family="monospace">
    <text x="600" y="475" fill="#ffffff" font-size="34" font-weight="900" letter-spacing="12" filter="url(#glow)">
      NOVA144Hz
      <animate attributeName="opacity" values="1;.55;1" dur="2.8s" repeatCount="indefinite"/>
    </text>
    <text x="600" y="504" fill="#00ff9c" font-size="11" letter-spacing="6" opacity=".9">
      AUTONOMOUS EXECUTION MATRIX // ARCHITECT
    </text>
  </g>

  <!-- GLITCH FRAGMENTS -->
  <g fill="#00ff9c">
    <rect x="360" y="210" width="30" height="2" opacity=".8">
      <animate attributeName="x" values="360;410;340;360" dur="0.8s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values=".2;1;.4;0" dur="0.8s" repeatCount="indefinite"/>
    </rect>
    <rect x="800" y="320" width="45" height="1.5" opacity=".7">
      <animate attributeName="x" values="800;760;820;800" dur="0.6s" repeatCount="indefinite"/>
      <animate attributeName="opacity" values=".1;.9;.2;0" dur="0.6s" repeatCount="indefinite"/>
    </rect>
  </g>
</svg>

<br>

<!-- ═══════════════════════════════════════════════════════════
     DYNAMIC STREAM TYPEWRITER
     ═══════════════════════════════════════════════════════════ -->
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=15&duration=900&pause=400&color=00FF9C&center=true&vCenter=true&width=720&height=40&lines=%5B+KERNEL+INITIALIZED+%3A+144Hz+CLOCK+LOCKED+%5D;%5B+SYSTEMS+ENGAGED+%3A+FULL-STACK+%2B+LOW-LEVEL+%5D;%5B+ORCHESTRATING+HIGH-EFFICIENCY+PIPELINES..._%5D" alt="Typing SVG" />

<br><br>

<!-- ═══════════════════════════════════════════════════════════
     DYNAMIC CYBER DIAGNOSTICS DECK
     ═══════════════════════════════════════════════════════════ -->
<svg width="100%" height="90" viewBox="0 0 1200 90" xmlns="http://www.w3.org/2000/svg">
  <rect x="100" y="10" width="1000" height="70" fill="#040c09" stroke="#00ff9c" stroke-opacity=".25" rx="4"/>
  
  <!-- Diagnostic Bars -->
  <g font-family="monospace" font-size="10" fill="#00ff9c" letter-spacing="1">
    <!-- Channel 1 -->
    <text x="140" y="38">THREAD_OCCUPANCY</text>
    <rect x="140" y="48" width="220" height="8" fill="#002b1b" rx="2"/>
    <rect x="140" y="48" width="180" height="8" fill="#00ff9c" rx="2">
      <animate attributeName="width" values="140;210;175;195;140" dur="3s" repeatCount="indefinite"/>
    </rect>

    <!-- Channel 2 -->
    <text x="490" y="38">MEMORY_MAP // HEAP_INTEGRITY</text>
    <rect x="490" y="48" width="220" height="8" fill="#002b1b" rx="2"/>
    <rect x="490" y="48" width="195" height="8" fill="#9affdf" rx="2">
      <animate attributeName="width" values="190;140;215;180;190" dur="4s" repeatCount="indefinite"/>
    </rect>

    <!-- Channel 3 -->
    <text x="840" y="38">SIGNAL_S/N // STABLE</text>
    <rect x="840" y="48" width="220" height="8" fill="#002b1b" rx="2"/>
    <rect x="840" y="48" width="205" height="8" fill="#00ff9c" rx="2">
      <animate attributeName="width" values="205;190;215;160;205" dur="2.5s" repeatCount="indefinite"/>
    </rect>
  </g>
</svg>

<br>

<!-- ═══════════════════════════════════════════════════════════
     HEADER // CORE TELEMETRY ACTIVITY
     ═══════════════════════════════════════════════════════════ -->
<svg width="100%" height="60" viewBox="0 0 1200 60" xmlns="http://www.w3.org/2000/svg">
  <line x1="100" y1="30" x2="440" y2="30" stroke="#00ff9c" stroke-opacity=".2"/>
  <line x1="760" y1="30" x2="1100" y2="30" stroke="#00ff9c" stroke-opacity=".2"/>
  
  <!-- Sweeping Reticle -->
  <circle cx="450" cy="30" r="3" fill="#00ff9c">
    <animate attributeName="cx" values="440;460;440" dur="1.5s" repeatCount="indefinite"/>
  </circle>
  <circle cx="750" cy="30" r="3" fill="#00ff9c">
    <animate attributeName="cx" values="760;740;760" dur="1.5s" repeatCount="indefinite"/>
  </circle>

  <text x="600" y="35" text-anchor="middle" fill="#00ff9c" font-family="monospace" font-size="13" letter-spacing="5">
    [ ACTIVITY_STREAM // KERNEL_LOAD ]
  </text>
</svg>

<br>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=NOVA144Hz&bg_color=00000000&color=00ff9c&line=00ff9c&point=ffffff&area=true&hide_border=true" width="94%"/>

<br><br>

<!-- ═══════════════════════════════════════════════════════════
     HEADER // TECH CAPABILITY MATRIX
     ═══════════════════════════════════════════════════════════ -->
<svg width="100%" height="60" viewBox="0 0 1200 60" xmlns="http://www.w3.org/2000/svg">
  <line x1="100" y1="30" x2="440" y2="30" stroke="#00ff9c" stroke-opacity=".2"/>
  <line x1="760" y1="30" x2="1100" y2="30" stroke="#00ff9c" stroke-opacity=".2"/>
  
  <text x="600" y="35" text-anchor="middle" fill="#00ff9c" font-family="monospace" font-size="13" letter-spacing="5">
    [ INJECTED_MODULES // STACK ]
  </text>
</svg>

<br>

<a href="#">
  <img src="https://skillicons.dev/icons?i=c,cpp,python,rust,linux,bash,docker,git,github,js,ts,html,css&theme=dark" alt="Tech Stack Icons"/>
</a>

<br><br>

<!-- ═══════════════════════════════════════════════════════════
     HEADER // CONTRIBUTION GRID MATRIX
     ═══════════════════════════════════════════════════════════ -->
<svg width="100%" height="70" viewBox="0 0 1200 70" xmlns="http://www.w3.org/2000/svg">
  <g fill="#00ff9c">
    <rect x="80" y="34" width="300" height="2" opacity=".2"/>
    <rect x="820" y="34" width="300" height="2" opacity=".2"/>
    
    <!-- Laser Oscillators -->
    <rect x="300" y="33" width="80" height="4">
      <animate attributeName="x" values="100;300;100" dur="3s" repeatCount="indefinite"/>
    </rect>
    <rect x="820" y="33" width="80" height="4">
      <animate attributeName="x" values="1020;820;1020" dur="3s" repeatCount="indefinite"/>
    </rect>
  </g>

  <text x="600" y="39" text-anchor="middle" fill="#00ff9c" font-family="monospace" font-size="14" font-weight="700" letter-spacing="6">
    COMMIT_TOPOLOGY // CHRONO_TRACE
    <animate attributeName="opacity" values=".4;1;.4" dur="2.2s" repeatCount="indefinite"/>
  </text>
</svg>

<br>

<img src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg" width="94%" alt="Snake Grid Matrix"/>

<br><br>

<!-- ═══════════════════════════════════════════════════════════
     SYSTEM TERMINATION GATEWAY
     ═══════════════════════════════════════════════════════════ -->
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=13&duration=1100&pause=350&color=00FF9C&center=true&vCenter=true&width=750&height=50&lines=%3E+COMMENCE_STANDBY_MODE...;%3E+MONITORING_DAEMON_PERSISTED+%5B144Hz%5D;%3E+TRANSMISSION_SUSPENDED..._"/><br>

<svg width="100%" height="110" viewBox="0 0 1200 110" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="waveGrad" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#00ff9c" stop-opacity="0"/>
      <stop offset="50%" stop-color="#00ff9c" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#00ff9c" stop-opacity="0"/>
    </linearGradient>
  </defs>

  <!-- Waveform Phase Alpha -->
  <path d="M0 55 Q300 15 600 55 T1200 55" fill="none" stroke="url(#waveGrad)" stroke-width="2">
    <animate attributeName="d" values="
      M0 55 Q300 15 600 55 T1200 55;
      M0 55 Q300 95 600 55 T1200 55;
      M0 55 Q300 15 600 55 T1200 55"
      dur="3.2s" repeatCount="indefinite"/>
  </path>

  <!-- Waveform Phase Beta (Inverted Counter-Oscillator) -->
  <path d="M0 55 Q300 95 600 55 T1200 55" fill="none" stroke="url(#waveGrad)" stroke-width="1.2" opacity=".45">
    <animate attributeName="d" values="
      M0 55 Q300 95 600 55 T1200 55;
      M0 55 Q300 15 600 55 T1200 55;
      M0 55 Q300 95 600 55 T1200 55"
      dur="3.2s" repeatCount="indefinite"/>
  </path>

  <!-- Center Tachyon Node -->
  <circle cx="600" cy="55" r="4" fill="#ffffff" filter="url(#glow)">
    <animate attributeName="r" values="3;7;3" dur="1.6s" repeatCount="indefinite"/>
  </circle>
</svg>

</div>
