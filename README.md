<div align="center"><!-- ═══════════════════════════════════════════════════════════
     NOVA144Hz // CUSTOM CYBER INTERFACE
     ═══════════════════════════════════════════════════════════ --><svg width="100%" height="520" viewBox="0 0 1200 520"
xmlns="http://www.w3.org/2000/svg">

<defs>  <!-- Background -->  <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
    <stop offset="0%" stop-color="#020303"/>
    <stop offset="50%" stop-color="#06110e"/>
    <stop offset="100%" stop-color="#000000"/>
  </linearGradient>  <!-- Core glow -->  <radialGradient id="core">
    <stop offset="0%" stop-color="#ffffff"/>
    <stop offset="15%" stop-color="#9affdf"/>
    <stop offset="45%" stop-color="#00ff9c" stop-opacity=".8"/>
    <stop offset="100%" stop-color="#00ff9c" stop-opacity="0"/>
  </radialGradient>  <!-- Glow -->  <filter id="glow">
    <feGaussianBlur stdDeviation="5" result="blur"/>
    <feMerge>
      <feMergeNode in="blur"/>
      <feMergeNode in="SourceGraphic"/>
    </feMerge>
  </filter>  <filter id="softGlow">
    <feGaussianBlur stdDeviation="12"/>
  </filter>  <!-- Scanline pattern -->  <pattern id="scanlines" width="1" height="8" patternUnits="userSpaceOnUse">
    <rect width="1" height="2" fill="#00ff9c" opacity=".08"/>
  </pattern>  <!-- Grid -->  <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
    <path d="M40 0H0V40" fill="none" stroke="#00ff9c" stroke-opacity=".08"/>
  </pattern></defs><!-- BACKGROUND --><rect width="1200" height="520" fill="url(#bg)"/>
<rect width="1200" height="520" fill="url(#grid)"/>
<rect width="1200" height="520" fill="url(#scanlines)"/><!-- MOVING SCAN --><rect x="0" y="-100" width="1200" height="3" fill="#00ff9c" opacity=".35">
  <animate attributeName="y"
           from="-100" to="620"
           dur="4s"
           repeatCount="indefinite"/>
</rect><!-- PARTICLES --><g fill="#00ff9c">  <circle cx="90" cy="110" r="2">
    <animate attributeName="opacity"
             values="0;.8;0"
             dur="2s"
             repeatCount="indefinite"/>
  </circle>  <circle cx="190" cy="390" r="1.5">
    <animate attributeName="opacity"
             values="0;.7;0"
             dur="3s"
             repeatCount="indefinite"/>
  </circle>  <circle cx="1030" cy="130" r="2">
    <animate attributeName="opacity"
             values="0;.8;0"
             dur="2.5s"
             repeatCount="indefinite"/>
  </circle>  <circle cx="1090" cy="350" r="1.5">
    <animate attributeName="opacity"
             values="0;.8;0"
             dur="1.8s"
             repeatCount="indefinite"/>
  </circle>  <circle cx="280" cy="90" r="1">
    <animate attributeName="opacity"
             values="0;.8;0"
             dur="2.2s"
             repeatCount="indefinite"/>
  </circle>  <circle cx="900" cy="410" r="2">
    <animate attributeName="opacity"
             values="0;.8;0"
             dur="2.8s"
             repeatCount="indefinite"/>
  </circle></g><!-- CORNER HUD --><g stroke="#00ff9c" fill="none" opacity=".65">  <path d="M35 90V35H90"/>
  <path d="M1110 35H1165V90"/>
  <path d="M35 430V485H90"/>
  <path d="M1110 485H1165V430"/></g><!-- TOP DATA --><g fill="#00ff9c" font-family="monospace" font-size="12">  <text x="48" y="65">
    NODE_01 // ONLINE
  </text>  <text x="930" y="65">
    SECURE_CHANNEL // 144Hz
  </text></g><!-- CENTRAL REACTOR --><g transform="translate(600 260)">  <!-- outer pulse --><circle r="145"
fill="none"
stroke="#00ff9c"
stroke-width="1"
opacity=".18">

<animate attributeName="r"
         values="135;160;135"
         dur="3s"
         repeatCount="indefinite"/>

<animate attributeName="opacity"
         values=".1;.35;.1"
         dur="3s"
         repeatCount="indefinite"/>

  </circle>  <!-- rotating ring --><circle r="120"
fill="none"
stroke="#00ff9c"
stroke-width="1"
stroke-dasharray="3 14"
opacity=".8">

<animateTransform
  attributeName="transform"
  type="rotate"
  from="0"
  to="360"
  dur="10s"
  repeatCount="indefinite"/>

  </circle>  <!-- second rotating ring --><circle r="95"
fill="none"
stroke="#9affdf"
stroke-width="2"
stroke-dasharray="45 18"
opacity=".7">

<animateTransform
  attributeName="transform"
  type="rotate"
  from="360"
  to="0"
  dur="7s"
  repeatCount="indefinite"/>

  </circle>  <!-- reactor glow --><circle r="90"
fill="url(#core)"
filter="url(#softGlow)">
<animate attributeName="r"
values="75;95;75"
dur="2s"
repeatCount="indefinite"/>
</circle>

  <!-- reactor core --><circle r="38"
fill="#00ff9c"
opacity=".12"
filter="url(#glow)"/>

<circle r="18"
fill="#00ff9c"
filter="url(#glow)">

<animate attributeName="r"
         values="15;21;15"
         dur="1.2s"
         repeatCount="indefinite"/>

  </circle>  <circle r="6" fill="white"/>  <!-- orbital particles -->  <circle cx="120" cy="0" r="3" fill="#00ff9c">
    <animateTransform
      attributeName="transform"
      type="rotate"
      from="0"
      to="360"
      dur="4s"
      repeatCount="indefinite"/>
  </circle></g><!-- CROSSHAIR --><g stroke="#00ff9c" opacity=".35">  <line x1="430" y1="260" x2="520" y2="260"/>
  <line x1="680" y1="260" x2="770" y2="260"/>
  <line x1="600" y1="110" x2="600" y2="175"/>
  <line x1="600" y1="345" x2="600" y2="410"/></g><!-- IDENTITY --><g text-anchor="middle" font-family="monospace"><text x="600" y="455"
fill="#ffffff"
font-size="34"
letter-spacing="10"
filter="url(#glow)">

NOVA144Hz

<animate attributeName="opacity"
         values="1;.45;1"
         dur="2.5s"
         repeatCount="indefinite"/>

  </text><text x="600" y="482"
fill="#00ff9c"
font-size="11"
letter-spacing="5">

SYSTEM // ACTIVE // BUILDING

  </text></g><!-- RANDOM GLITCH BARS --><g fill="#00ff9c">  <rect x="380" y="205" width="40" height="2">
    <animate attributeName="x"
             values="380;410;370;380"
             dur=".7s"
             repeatCount="indefinite"/>
  </rect>  <rect x="780" y="310" width="35" height="2">
    <animate attributeName="x"
             values="780;750;800;780"
             dur=".5s"
             repeatCount="indefinite"/>
  </rect></g></svg><br><!-- ═══════════════════════════════════════════════════════════
                         SIGNAL
     ═══════════════════════════════════════════════════════════ --><img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=14&duration=800&pause=300&color=00FF9C&center=true&vCenter=true&width=650&height=35&lines=%5B+SIGNAL+ACQUIRED+%5D;%5B+IDENTITY+CONFIRMED+%5D;%5B+NOVA_CORE+ONLINE+%5D" /><br><br>

<!-- ═══════════════════════════════════════════════════════════
                       VISUAL SEPARATOR
     ═══════════════════════════════════════════════════════════ --><svg width="100%" height="50" viewBox="0 0 1200 50"
xmlns="http://www.w3.org/2000/svg">

<line x1="0" y1="25" x2="1200" y2="25"
stroke="#00ff9c" stroke-opacity=".15"/>

<circle cx="600" cy="25" r="5" fill="#00ff9c"><animate attributeName="r"
values="3;8;3"
dur="1.5s"
repeatCount="indefinite"/>

</circle><line x1="480" y1="25" x2="570" y2="25"
stroke="#00ff9c">

<animate attributeName="x1"
values="480;500;480"
dur="2s"
repeatCount="indefinite"/>

</line><line x1="630" y1="25" x2="720" y2="25"
stroke="#00ff9c">

<animate attributeName="x2"
values="720;700;720"
dur="2s"
repeatCount="indefinite"/>

</line></svg><br><!-- ═══════════════════════════════════════════════════════════
                         CORE DATA
     ═══════════════════════════════════════════════════════════ --><img src="https://github-readme-activity-graph.vercel.app/graph?username=NOVA144Hz&bg_color=00000000&color=00ff9c&line=00ff9c&point=ffffff&area=true&hide_border=true" width="100%"/><br><br>

<!-- ═══════════════════════════════════════════════════════════
                         TECH CORE
     ═══════════════════════════════════════════════════════════ --><img src="https://skillicons.dev/icons?i=python,cpp,c,js,html,css,bash,linux,git,github,docker&theme=dark"/><br><br>

<!-- ═══════════════════════════════════════════════════════════
                     CONTRIBUTION MATRIX
     ═══════════════════════════════════════════════════════════ --><svg width="100%" height="100" viewBox="0 0 1200 100"
xmlns="http://www.w3.org/2000/svg">

<g fill="#00ff9c"><rect x="0" y="45" width="20" height="4">
  <animate attributeName="width"
           values="20;180;20"
           dur="2s"
           repeatCount="indefinite"/>
</rect><rect x="1020" y="45" width="180" height="4">
  <animate attributeName="width"
           values="180;20;180"
           dur="2s"
           repeatCount="indefinite"/>
</rect></g><text x="600" y="52"
text-anchor="middle"
fill="#00ff9c"
font-family="monospace"
font-size="14"
letter-spacing="6">

CONTRIBUTION_MATRIX

<animate attributeName="opacity"
values=".3;1;.3"
dur="2s"
repeatCount="indefinite"/>

</text></svg><br><img src="https://raw.githubusercontent.com/Platane/snk/output/github-contribution-grid-snake-dark.svg" width="100%"/><br><br>

<!-- ═══════════════════════════════════════════════════════════
                           EXIT
     ═══════════════════════════════════════════════════════════ --><img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=13&duration=1200&pause=300&color=00FF9C&center=true&vCenter=true&width=700&height=80&lines=%3E+TERMINATING+SESSION...;%3E+CORE+REMAINS+ACTIVE...;%3E+PROCESS+NOVA144Hz.exe+CONTINUES...;%3E+CONNECTION+SUSPENDED_"/><br><svg width="100%" height="120" viewBox="0 0 1200 120"
xmlns="http://www.w3.org/2000/svg">

<defs><linearGradient id="footer" x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#000000"/>
<stop offset="50%" stop-color="#00ff9c"/>
<stop offset="100%" stop-color="#000000"/></linearGradient></defs><path d="M0 80 Q300 20 600 80 T1200 80"
fill="none"
stroke="url(#footer)"
stroke-width="2">

<animate attributeName="d"
values="
M0 80 Q300 20 600 80 T1200 80;
M0 80 Q300 140 600 80 T1200 80;
M0 80 Q300 20 600 80 T1200 80"
dur="4s"
repeatCount="indefinite"/>

</path><circle cx="600" cy="80" r="4" fill="#00ff9c"><animate attributeName="r"
values="3;10;3"
dur="2s"
repeatCount="indefinite"/>

</circle></svg></div>
