<!--
  SINGLE-FILE README
  This file combines README.md, banner.svg, moveset.svg, pokedex.svg, and footer.svg.
  You can rename this file to README.md when you are ready to use it.
-->
<!-- ═══════════════════════════════════════════════════════════ -->
<!--        GOKULAN ANBALAGAN  ·  POKÉMON EDITION README        -->
<!--                   github.com/gokulan                       -->
<!-- ═══════════════════════════════════════════════════════════ -->

<div align="center">

<!-- ══════════════════════ HERO BANNER ══════════════════════ -->

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 860 200" width="860" height="200">
  <defs>
    <!-- Gradients -->
    <linearGradient id="bgTop" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#1A1A2E"/>
      <stop offset="100%" stop-color="#0F0F1A"/>
    </linearGradient>
    <radialGradient id="ballRed" cx="50%" cy="40%" r="60%">
      <stop offset="0%" stop-color="#FF4444"/>
      <stop offset="100%" stop-color="#CC0000"/>
    </radialGradient>
    <radialGradient id="ballWhite" cx="50%" cy="40%" r="60%">
      <stop offset="0%" stop-color="#FFFFFF"/>
      <stop offset="100%" stop-color="#CCCCCC"/>
    </radialGradient>
    <radialGradient id="btnGlow" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#FFFFFF"/>
      <stop offset="60%" stop-color="#EEEEEE"/>
      <stop offset="100%" stop-color="#AAAAAA"/>
    </radialGradient>
    <linearGradient id="goldText" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#F5C518"/>
      <stop offset="50%" stop-color="#FFE566"/>
      <stop offset="100%" stop-color="#F5C518"/>
    </linearGradient>
    <filter id="glowGold" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="3" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="glowRed" x="-30%" y="-30%" width="160%" height="160%">
      <feGaussianBlur in="SourceGraphic" stdDeviation="4" result="blur"/>
      <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <clipPath id="topHalf">
      <rect x="0" y="0" width="120" height="60"/>
    </clipPath>
    <clipPath id="botHalf">
      <rect x="0" y="60" width="120" height="60"/>
    </clipPath>

    <!-- Animations -->
    <style>
      .ball-top    { animation: openTop  3s ease-in-out infinite; transform-origin: 60px 60px; }
      .ball-bot    { animation: openBot  3s ease-in-out infinite; transform-origin: 60px 60px; }
      .ball-btn    { animation: btnPulse 3s ease-in-out infinite; }
      .sparkle     { animation: sparkle  3s ease-in-out infinite; }
      .s1 { animation-delay: 0s;    }
      .s2 { animation-delay: 0.3s;  }
      .s3 { animation-delay: 0.6s;  }
      .s4 { animation-delay: 0.9s;  }
      .s5 { animation-delay: 1.2s;  }
      .s6 { animation-delay: 1.5s;  }
      .title-glow  { animation: titleGlow 2s ease-in-out infinite; }
      .sub-fade    { animation: subFade  2.5s ease-in-out infinite; }
      .star        { animation: twinkle  2s ease-in-out infinite; }
      .st1 { animation-delay:0s; }
      .st2 { animation-delay:0.7s; }
      .st3 { animation-delay:1.4s; }
      .st4 { animation-delay:0.3s; }
      .st5 { animation-delay:1.1s; }
      .st6 { animation-delay:1.8s; }
      .st7 { animation-delay:0.5s; }
      .st8 { animation-delay:1.6s; }
      .border-pulse { animation: borderPulse 3s ease-in-out infinite; }
      .card-line    { animation: cardLine   4s ease-in-out infinite; }

      @keyframes openTop {
        0%,30%    { transform: translateY(0);   }
        45%,55%   { transform: translateY(-18px); }
        70%,100%  { transform: translateY(0);   }
      }
      @keyframes openBot {
        0%,30%    { transform: translateY(0);   }
        45%,55%   { transform: translateY(18px);  }
        70%,100%  { transform: translateY(0);   }
      }
      @keyframes btnPulse {
        0%,30%    { opacity:1; r:12; }
        45%,55%   { opacity:1; r:15; filter:url(#glowGold); }
        70%,100%  { opacity:1; r:12; }
      }
      @keyframes sparkle {
        0%,40%    { opacity:0; transform:scale(0); }
        50%       { opacity:1; transform:scale(1); }
        65%,100%  { opacity:0; transform:scale(0); }
      }
      @keyframes titleGlow {
        0%,100% { opacity:0.9; }
        50%     { opacity:1;   }
      }
      @keyframes subFade {
        0%,100% { opacity:0.7; }
        50%     { opacity:1;   }
      }
      @keyframes twinkle {
        0%,100% { opacity:0.2; r:1.2; }
        50%     { opacity:1;   r:2;   }
      }
      @keyframes borderPulse {
        0%,100% { stroke:#EE1515; stroke-opacity:0.6; }
        50%     { stroke:#FF4444; stroke-opacity:1;   }
      }
      @keyframes cardLine {
        0%,100% { stroke-opacity:0.2; }
        50%     { stroke-opacity:0.5; }
      }
    </style>
  </defs>

  <!-- Background -->
  <rect width="860" height="200" fill="url(#bgTop)" rx="14"/>
  <!-- Border -->
  <rect width="858" height="198" x="1" y="1" fill="none" stroke="#EE1515" stroke-width="2" rx="13" class="border-pulse"/>
  <rect width="852" height="192" x="4" y="4" fill="none" stroke="#F5C518" stroke-width="0.5" rx="11" opacity="0.3"/>

  <!-- Stars scattered -->
  <circle cx="30"  cy="18"  class="star st1" fill="#F5C518"/>
  <circle cx="100" cy="10"  class="star st2" fill="#FFFFFF"/>
  <circle cx="200" cy="22"  class="star st3" fill="#F5C518"/>
  <circle cx="340" cy="8"   class="star st4" fill="#FFFFFF"/>
  <circle cx="520" cy="15"  class="star st5" fill="#F5C518"/>
  <circle cx="660" cy="20"  class="star st6" fill="#FFFFFF"/>
  <circle cx="780" cy="9"   class="star st7" fill="#F5C518"/>
  <circle cx="840" cy="22"  class="star st8" fill="#FFFFFF"/>

  <!-- ═══ POKÉBALL (left side) ═══ -->
  <g transform="translate(60, 40)">
    <!-- Shadow -->
    <ellipse cx="60" cy="125" rx="42" ry="8" fill="#000000" opacity="0.3"/>

    <!-- Bottom half (white) -->
    <g class="ball-bot">
      <path d="M 5,60 A 55,55 0 0,0 115,60 Z" fill="url(#ballWhite)"/>
      <path d="M 5,60 A 55,55 0 0,0 115,60 Z" fill="none" stroke="#999" stroke-width="1.5"/>
    </g>

    <!-- Top half (red) -->
    <g class="ball-top">
      <path d="M 5,60 A 55,55 0 0,1 115,60 Z" fill="url(#ballRed)" filter="url(#glowRed)"/>
      <path d="M 5,60 A 55,55 0 0,1 115,60 Z" fill="none" stroke="#AA0000" stroke-width="1.5"/>
      <!-- Shine on red half -->
      <ellipse cx="40" cy="35" rx="14" ry="8" fill="#FF8888" opacity="0.4" transform="rotate(-20,40,35)"/>
    </g>

    <!-- Center band -->
    <rect x="5" y="55" width="110" height="10" fill="#111111"/>
    <rect x="5" y="56" width="110" height="1"  fill="#333333"/>
    <rect x="5" y="64" width="110" height="1"  fill="#333333"/>

    <!-- Center button -->
    <circle cx="60" cy="60" r="16" fill="#333333"/>
    <circle cx="60" cy="60" r="12" fill="url(#btnGlow)" class="ball-btn"/>
    <circle cx="55" cy="56" r="3"  fill="#FFFFFF" opacity="0.7"/>

    <!-- Sparkles when open -->
    <g class="sparkle s1"><text x="18"  y="18"  font-size="14" fill="#FFE566" text-anchor="middle">✦</text></g>
    <g class="sparkle s2"><text x="102" y="18"  font-size="12" fill="#FFE566" text-anchor="middle">✦</text></g>
    <g class="sparkle s3"><text x="60"  y="10"  font-size="10" fill="#FFFFFF"  text-anchor="middle">★</text></g>
    <g class="sparkle s4"><text x="10"  y="40"  font-size="8"  fill="#FFE566" text-anchor="middle">✦</text></g>
    <g class="sparkle s5"><text x="110" y="40"  font-size="8"  fill="#FFE566" text-anchor="middle">✦</text></g>
    <g class="sparkle s6"><text x="60"  y="106" font-size="10" fill="#FFFFFF"  text-anchor="middle">★</text></g>
  </g>

  <!-- ═══ TRAINER CARD (right of ball) ═══ -->
  <g transform="translate(220, 20)">
    <!-- Card bg -->
    <rect width="600" height="160" rx="10" fill="#0D1B3E" opacity="0.8"/>
    <rect width="598" height="158" x="1" y="1" rx="9" fill="none" stroke="#F5C518" stroke-width="1" opacity="0.5"/>

    <!-- Card top strip -->
    <rect width="600" height="30" rx="10" fill="#EE1515" opacity="0.9"/>
    <rect width="600" height="20" y="20" fill="#EE1515" opacity="0.9"/>
    <text x="300" y="21" font-family="'Courier New',monospace" font-size="13" font-weight="900"
          fill="#FFE566" text-anchor="middle" letter-spacing="4">✦ TRAINER CARD ✦</text>

    <!-- Divider lines -->
    <line x1="20" y1="70"  x2="580" y2="70"  stroke="#F5C518" stroke-width="0.5" class="card-line"/>
    <line x1="20" y1="110" x2="580" y2="110" stroke="#F5C518" stroke-width="0.5" class="card-line"/>

    <!-- Name -->
    <text x="30" y="58" font-family="'Courier New',monospace" font-size="10" fill="#AAAACC" letter-spacing="2">TRAINER NAME</text>
    <text x="30" y="90" font-family="'Courier New',monospace" font-size="26" font-weight="900"
          fill="url(#goldText)" letter-spacing="3" filter="url(#glowGold)" class="title-glow">GOKULAN</text>
    <text x="310" y="58" font-family="'Courier New',monospace" font-size="10" fill="#AAAACC" letter-spacing="2">ALIAS</text>
    <text x="310" y="90" font-family="'Courier New',monospace" font-size="26" font-weight="900"
          fill="#FF4444" letter-spacing="3">RKIVLN</text>

    <!-- Stats row -->
    <text x="30"  y="130" font-family="'Courier New',monospace" font-size="10" fill="#88AAFF" letter-spacing="1">CLASS</text>
    <text x="30"  y="148" font-family="'Courier New',monospace" font-size="13" font-weight="700" fill="#FFFFFF">B.Tech CSBS</text>

    <text x="160" y="130" font-family="'Courier New',monospace" font-size="10" fill="#88AAFF" letter-spacing="1">REGION</text>
    <text x="160" y="148" font-family="'Courier New',monospace" font-size="13" font-weight="700" fill="#FFFFFF">Pondicherry</text>

    <text x="310" y="130" font-family="'Courier New',monospace" font-size="10" fill="#88AAFF" letter-spacing="1">GUILD</text>
    <text x="310" y="148" font-family="'Courier New',monospace" font-size="13" font-weight="700" fill="#FFE566">⚡ Volt Media</text>

    <text x="460" y="130" font-family="'Courier New',monospace" font-size="10" fill="#88AAFF" letter-spacing="1">STATUS</text>
    <text x="460" y="148" font-family="'Courier New',monospace" font-size="13" font-weight="700" fill="#4CAF50">● ACTIVE</text>
  </g>
</svg>


<br/>
<br/>

<!-- ═══════════════════ QUICK TYPE BADGES ══════════════════ -->

![React](https://img.shields.io/badge/React-WATER%20TYPE-61DAFB?style=for-the-badge&logo=react&logoColor=61DAFB&labelColor=0D1B2E)
![Next.js](https://img.shields.io/badge/Next.js-NORMAL%20TYPE-FFFFFF?style=for-the-badge&logo=next.js&logoColor=FFFFFF&labelColor=0D0D0D)
![TailwindCSS](https://img.shields.io/badge/Tailwind-ICE%20TYPE-38BDF8?style=for-the-badge&logo=tailwindcss&logoColor=38BDF8&labelColor=0D1B2E)
![Python](https://img.shields.io/badge/Python-ELECTRIC%20TYPE-FFD43B?style=for-the-badge&logo=python&logoColor=FFD43B&labelColor=1A1A0D)
![Figma](https://img.shields.io/badge/Figma-FIRE%20TYPE-F24E1E?style=for-the-badge&logo=figma&logoColor=F24E1E&labelColor=1A0D0D)
![AWS](https://img.shields.io/badge/AWS-FLYING%20TYPE-FF9900?style=for-the-badge&logo=amazonaws&logoColor=FF9900&labelColor=1A1000)

<br/>
<br/>

<!-- ═══════════════════ MOVE SET / SKILLS ══════════════════ -->

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 860 180" width="860" height="180">
  <defs>
    <linearGradient id="bg2" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#1A1A2E"/>
      <stop offset="100%" stop-color="#0F0F1A"/>
    </linearGradient>

    <!-- Bar gradients per type colour -->
    <linearGradient id="barReact"    x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#61DAFB"/><stop offset="100%" stop-color="#21B8D6"/></linearGradient>
    <linearGradient id="barNext"     x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#FFFFFF"/><stop offset="100%" stop-color="#AAAAAA"/></linearGradient>
    <linearGradient id="barNode"     x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#68A063"/><stop offset="100%" stop-color="#3D7A36"/></linearGradient>
    <linearGradient id="barTailwind" x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#38BDF8"/><stop offset="100%" stop-color="#0EA5E9"/></linearGradient>
    <linearGradient id="barPython"   x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#FFD43B"/><stop offset="100%" stop-color="#F5A623"/></linearGradient>
    <linearGradient id="barFigma"    x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#F24E1E"/><stop offset="100%" stop-color="#C03015"/></linearGradient>
    <linearGradient id="barAWS"      x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#FF9900"/><stop offset="100%" stop-color="#CC7700"/></linearGradient>
    <linearGradient id="barUIUX"     x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#A855F7"/><stop offset="100%" stop-color="#7C3AED"/></linearGradient>

    <style>
      .bar-react    { animation: growBar 2s ease-out 0.1s both; }
      .bar-next     { animation: growBar 2s ease-out 0.2s both; }
      .bar-node     { animation: growBar 2s ease-out 0.3s both; }
      .bar-tailwind { animation: growBar 2s ease-out 0.4s both; }
      .bar-python   { animation: growBar 2s ease-out 0.5s both; }
      .bar-figma    { animation: growBar 2s ease-out 0.6s both; }
      .bar-aws      { animation: growBar 2s ease-out 0.7s both; }
      .bar-uiux     { animation: growBar 2s ease-out 0.8s both; }
      .badge        { animation: badgePop 0.5s ease-out both; }
      .b1 { animation-delay:0.05s; }
      .b2 { animation-delay:0.10s; }
      .b3 { animation-delay:0.15s; }
      .b4 { animation-delay:0.20s; }
      .b5 { animation-delay:0.25s; }
      .b6 { animation-delay:0.30s; }
      .b7 { animation-delay:0.35s; }
      .b8 { animation-delay:0.40s; }
      .border-pulse { animation: borderPulse 3s ease-in-out infinite; }

      @keyframes growBar {
        from { transform: scaleX(0); }
        to   { transform: scaleX(1); }
      }
      @keyframes badgePop {
        0%   { opacity:0; transform:scale(0.5); }
        80%  { transform:scale(1.05); }
        100% { opacity:1; transform:scale(1); }
      }
      @keyframes borderPulse {
        0%,100% { stroke:#EE1515; stroke-opacity:0.6; }
        50%     { stroke:#FF4444; stroke-opacity:1;   }
      }
    </style>
  </defs>

  <!-- Background -->
  <rect width="860" height="180" fill="url(#bg2)" rx="14"/>
  <rect width="858" height="178" x="1" y="1" fill="none" stroke="#EE1515" stroke-width="1.5" rx="13" class="border-pulse"/>

  <!-- Section title -->
  <text x="430" y="28" font-family="'Courier New',monospace" font-size="13" font-weight="900"
        fill="#F5C518" text-anchor="middle" letter-spacing="5">⚔ MOVE SET  /  TECH ABILITIES ⚔</text>
  <line x1="30" y1="36" x2="830" y2="36" stroke="#F5C518" stroke-width="0.5" opacity="0.3"/>

  <!-- ── Left column ── -->
  <!-- React -->
  <g class="badge b1">
    <rect x="20" y="50" width="70" height="20" rx="10" fill="#61DAFB" opacity="0.2"/>
    <rect x="20" y="50" width="70" height="20" rx="10" fill="none" stroke="#61DAFB" stroke-width="1"/>
    <text x="55" y="64" font-family="'Courier New',monospace" font-size="10" font-weight="700" fill="#61DAFB" text-anchor="middle">REACT</text>
  </g>
  <rect x="100" y="54" width="290" height="12" rx="6" fill="#1E1E3F"/>
  <g style="transform-origin:100px 60px">
    <rect x="100" y="54" width="261" height="12" rx="6" fill="url(#barReact)" class="bar-react"/>
  </g>
  <text x="402" y="64" font-family="'Courier New',monospace" font-size="10" fill="#61DAFB" text-anchor="end">90</text>

  <!-- Next.js -->
  <g class="badge b2">
    <rect x="20" y="80" width="70" height="20" rx="10" fill="#FFFFFF" opacity="0.1"/>
    <rect x="20" y="80" width="70" height="20" rx="10" fill="none" stroke="#FFFFFF" stroke-width="1"/>
    <text x="55" y="94" font-family="'Courier New',monospace" font-size="10" font-weight="700" fill="#FFFFFF" text-anchor="middle">NEXT.JS</text>
  </g>
  <rect x="100" y="84" width="290" height="12" rx="6" fill="#1E1E3F"/>
  <g style="transform-origin:100px 90px">
    <rect x="100" y="84" width="245" height="12" rx="6" fill="url(#barNext)" class="bar-next"/>
  </g>
  <text x="402" y="94" font-family="'Courier New',monospace" font-size="10" fill="#FFFFFF" text-anchor="end">85</text>

  <!-- Node.js -->
  <g class="badge b3">
    <rect x="20" y="110" width="70" height="20" rx="10" fill="#68A063" opacity="0.2"/>
    <rect x="20" y="110" width="70" height="20" rx="10" fill="none" stroke="#68A063" stroke-width="1"/>
    <text x="55" y="124" font-family="'Courier New',monospace" font-size="10" font-weight="700" fill="#68A063" text-anchor="middle">NODE</text>
  </g>
  <rect x="100" y="114" width="290" height="12" rx="6" fill="#1E1E3F"/>
  <g style="transform-origin:100px 120px">
    <rect x="100" y="114" width="232" height="12" rx="6" fill="url(#barNode)" class="bar-node"/>
  </g>
  <text x="402" y="124" font-family="'Courier New',monospace" font-size="10" fill="#68A063" text-anchor="end">80</text>

  <!-- Tailwind -->
  <g class="badge b4">
    <rect x="20" y="140" width="70" height="20" rx="10" fill="#38BDF8" opacity="0.2"/>
    <rect x="20" y="140" width="70" height="20" rx="10" fill="none" stroke="#38BDF8" stroke-width="1"/>
    <text x="55" y="154" font-family="'Courier New',monospace" font-size="9" font-weight="700" fill="#38BDF8" text-anchor="middle">TAILWIND</text>
  </g>
  <rect x="100" y="144" width="290" height="12" rx="6" fill="#1E1E3F"/>
  <g style="transform-origin:100px 150px">
    <rect x="100" y="144" width="275" height="12" rx="6" fill="url(#barTailwind)" class="bar-tailwind"/>
  </g>
  <text x="402" y="154" font-family="'Courier New',monospace" font-size="10" fill="#38BDF8" text-anchor="end">95</text>

  <!-- ── Right column ── -->
  <!-- Python -->
  <g class="badge b5">
    <rect x="440" y="50" width="70" height="20" rx="10" fill="#FFD43B" opacity="0.2"/>
    <rect x="440" y="50" width="70" height="20" rx="10" fill="none" stroke="#FFD43B" stroke-width="1"/>
    <text x="475" y="64" font-family="'Courier New',monospace" font-size="10" font-weight="700" fill="#FFD43B" text-anchor="middle">PYTHON</text>
  </g>
  <rect x="520" y="54" width="290" height="12" rx="6" fill="#1E1E3F"/>
  <g style="transform-origin:520px 60px">
    <rect x="520" y="54" width="220" height="12" rx="6" fill="url(#barPython)" class="bar-python"/>
  </g>
  <text x="822" y="64" font-family="'Courier New',monospace" font-size="10" fill="#FFD43B" text-anchor="end">76</text>

  <!-- Figma -->
  <g class="badge b6">
    <rect x="440" y="80" width="70" height="20" rx="10" fill="#F24E1E" opacity="0.2"/>
    <rect x="440" y="80" width="70" height="20" rx="10" fill="none" stroke="#F24E1E" stroke-width="1"/>
    <text x="475" y="94" font-family="'Courier New',monospace" font-size="10" font-weight="700" fill="#F24E1E" text-anchor="middle">FIGMA</text>
  </g>
  <rect x="520" y="84" width="290" height="12" rx="6" fill="#1E1E3F"/>
  <g style="transform-origin:520px 90px">
    <rect x="520" y="84" width="261" height="12" rx="6" fill="url(#barFigma)" class="bar-figma"/>
  </g>
  <text x="822" y="94" font-family="'Courier New',monospace" font-size="10" fill="#F24E1E" text-anchor="end">90</text>

  <!-- AWS -->
  <g class="badge b7">
    <rect x="440" y="110" width="70" height="20" rx="10" fill="#FF9900" opacity="0.2"/>
    <rect x="440" y="110" width="70" height="20" rx="10" fill="none" stroke="#FF9900" stroke-width="1"/>
    <text x="475" y="124" font-family="'Courier New',monospace" font-size="10" font-weight="700" fill="#FF9900" text-anchor="middle">AWS</text>
  </g>
  <rect x="520" y="114" width="290" height="12" rx="6" fill="#1E1E3F"/>
  <g style="transform-origin:520px 120px">
    <rect x="520" y="114" width="203" height="12" rx="6" fill="url(#barAWS)" class="bar-aws"/>
  </g>
  <text x="822" y="124" font-family="'Courier New',monospace" font-size="10" fill="#FF9900" text-anchor="end">70</text>

  <!-- UI/UX -->
  <g class="badge b8">
    <rect x="440" y="140" width="70" height="20" rx="10" fill="#A855F7" opacity="0.2"/>
    <rect x="440" y="140" width="70" height="20" rx="10" fill="none" stroke="#A855F7" stroke-width="1"/>
    <text x="475" y="154" font-family="'Courier New',monospace" font-size="10" font-weight="700" fill="#A855F7" text-anchor="middle">UI / UX</text>
  </g>
  <rect x="520" y="144" width="290" height="12" rx="6" fill="#1E1E3F"/>
  <g style="transform-origin:520px 150px">
    <rect x="520" y="144" width="275" height="12" rx="6" fill="url(#barUIUX)" class="bar-uiux"/>
  </g>
  <text x="822" y="154" font-family="'Courier New',monospace" font-size="10" fill="#A855F7" text-anchor="end">95</text>

  <!-- Divider between columns -->
  <line x1="430" y1="44" x2="430" y2="168" stroke="#F5C518" stroke-width="0.5" opacity="0.2"/>
</svg>


<br/>
<br/>

<!-- ════════════════════ POKÉDEX / PROJECTS ════════════════ -->

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 860 230" width="860" height="230">
  <defs>
    <linearGradient id="bg3" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#1A1A2E"/>
      <stop offset="100%" stop-color="#0F0F1A"/>
    </linearGradient>
    <linearGradient id="card1" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#1A3A5C"/>
      <stop offset="100%" stop-color="#0D1B2E"/>
    </linearGradient>
    <linearGradient id="card2" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#2D1B4E"/>
      <stop offset="100%" stop-color="#150D2A"/>
    </linearGradient>
    <linearGradient id="card3" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#1A3A1A"/>
      <stop offset="100%" stop-color="#0D1E0D"/>
    </linearGradient>
    <linearGradient id="card4" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#3A1A1A"/>
      <stop offset="100%" stop-color="#1E0D0D"/>
    </linearGradient>
    <filter id="cardGlow1" x="-10%" y="-10%" width="120%" height="120%">
      <feGaussianBlur in="SourceAlpha" stdDeviation="3" result="b"/>
      <feFlood flood-color="#61DAFB" flood-opacity="0.4" result="c"/>
      <feComposite in="c" in2="b" operator="in" result="shadow"/>
      <feMerge><feMergeNode in="shadow"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="cardGlow2" x="-10%" y="-10%" width="120%" height="120%">
      <feGaussianBlur in="SourceAlpha" stdDeviation="3" result="b"/>
      <feFlood flood-color="#A855F7" flood-opacity="0.4" result="c"/>
      <feComposite in="c" in2="b" operator="in" result="shadow"/>
      <feMerge><feMergeNode in="shadow"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="cardGlow3" x="-10%" y="-10%" width="120%" height="120%">
      <feGaussianBlur in="SourceAlpha" stdDeviation="3" result="b"/>
      <feFlood flood-color="#4CAF50" flood-opacity="0.4" result="c"/>
      <feComposite in="c" in2="b" operator="in" result="shadow"/>
      <feMerge><feMergeNode in="shadow"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <filter id="cardGlow4" x="-10%" y="-10%" width="120%" height="120%">
      <feGaussianBlur in="SourceAlpha" stdDeviation="3" result="b"/>
      <feFlood flood-color="#FF4444" flood-opacity="0.4" result="c"/>
      <feComposite in="c" in2="b" operator="in" result="shadow"/>
      <feMerge><feMergeNode in="shadow"/><feMergeNode in="SourceGraphic"/></feMerge>
    </filter>
    <style>
      .card { animation: cardFloat 3s ease-in-out infinite; }
      .c1 { animation-delay: 0s;    }
      .c2 { animation-delay: 0.75s; }
      .c3 { animation-delay: 1.5s;  }
      .c4 { animation-delay: 2.25s; }
      .border-pulse { animation: borderPulse 3s ease-in-out infinite; }
      .hp-bar { animation: hpFill 1.5s ease-out both; }
      .hp1 { animation-delay:0.2s; }
      .hp2 { animation-delay:0.4s; }
      .hp3 { animation-delay:0.6s; }
      .hp4 { animation-delay:0.8s; }

      @keyframes cardFloat {
        0%,100% { transform: translateY(0); }
        50%     { transform: translateY(-5px); }
      }
      @keyframes borderPulse {
        0%,100% { stroke:#EE1515; stroke-opacity:0.6; }
        50%     { stroke:#FF4444; stroke-opacity:1; }
      }
      @keyframes hpFill {
        from { transform: scaleX(0); }
        to   { transform: scaleX(1); }
      }
    </style>
  </defs>

  <rect width="860" height="230" fill="url(#bg3)" rx="14"/>
  <rect width="858" height="228" x="1" y="1" fill="none" stroke="#EE1515" stroke-width="1.5" rx="13" class="border-pulse"/>

  <!-- Title -->
  <text x="430" y="26" font-family="'Courier New',monospace" font-size="13" font-weight="900"
        fill="#F5C518" text-anchor="middle" letter-spacing="5">◉ POKÉDEX  /  MY PROJECTS ◉</text>
  <line x1="30" y1="34" x2="830" y2="34" stroke="#F5C518" stroke-width="0.5" opacity="0.3"/>

  <!-- ── Card 1: Pit Wall / WATER type ── -->
  <g transform="translate(20, 46)" class="card c1" filter="url(#cardGlow1)">
    <rect width="190" height="170" rx="10" fill="url(#card1)"/>
    <rect width="190" height="170" rx="10" fill="none" stroke="#61DAFB" stroke-width="1.5"/>
    <!-- Type pill -->
    <rect x="8" y="8" width="50" height="16" rx="8" fill="#61DAFB" opacity="0.3"/>
    <rect x="8" y="8" width="50" height="16" rx="8" fill="none" stroke="#61DAFB" stroke-width="1"/>
    <text x="33" y="20" font-family="'Courier New',monospace" font-size="9" font-weight="700" fill="#61DAFB" text-anchor="middle">WATER</text>
    <!-- Pokédex number -->
    <text x="182" y="20" font-family="'Courier New',monospace" font-size="9" fill="#61DAFB" text-anchor="end" opacity="0.7">#001</text>
    <!-- Big emoji icon -->
    <text x="95" y="88" font-size="44" text-anchor="middle">🏎</text>
    <!-- HP bar -->
    <text x="10" y="118" font-family="'Courier New',monospace" font-size="8" fill="#AAAACC">HP</text>
    <rect x="28" y="110" width="130" height="8" rx="4" fill="#0D1B2E"/>
    <g style="transform-origin:28px 114px">
      <rect x="28" y="110" width="117" height="8" rx="4" fill="#61DAFB" class="hp-bar hp1"/>
    </g>
    <text x="162" y="118" font-family="'Courier New',monospace" font-size="8" fill="#61DAFB">90</text>
    <!-- Name -->
    <text x="95" y="136" font-family="'Courier New',monospace" font-size="13" font-weight="900" fill="#FFFFFF" text-anchor="middle">PIT WALL</text>
    <!-- Description -->
    <text x="95" y="150" font-family="'Courier New',monospace" font-size="8" fill="#8899BB" text-anchor="middle">F1 2026 Dashboard</text>
    <text x="95" y="162" font-family="'Courier New',monospace" font-size="8" fill="#8899BB" text-anchor="middle">React · SVG · Live Data</text>
  </g>

  <!-- ── Card 2: Volt Media / ELECTRIC type ── -->
  <g transform="translate(230, 46)" class="card c2" filter="url(#cardGlow2)">
    <rect width="190" height="170" rx="10" fill="url(#card2)"/>
    <rect width="190" height="170" rx="10" fill="none" stroke="#F5C518" stroke-width="1.5"/>
    <rect x="8" y="8" width="66" height="16" rx="8" fill="#F5C518" opacity="0.3"/>
    <rect x="8" y="8" width="66" height="16" rx="8" fill="none" stroke="#F5C518" stroke-width="1"/>
    <text x="41" y="20" font-family="'Courier New',monospace" font-size="9" font-weight="700" fill="#F5C518" text-anchor="middle">ELECTRIC</text>
    <text x="182" y="20" font-family="'Courier New',monospace" font-size="9" fill="#F5C518" text-anchor="end" opacity="0.7">#002</text>
    <text x="95" y="88" font-size="44" text-anchor="middle">⚡</text>
    <text x="10" y="118" font-family="'Courier New',monospace" font-size="8" fill="#AAAACC">HP</text>
    <rect x="28" y="110" width="130" height="8" rx="4" fill="#150D2A"/>
    <g style="transform-origin:28px 114px">
      <rect x="28" y="110" width="124" height="8" rx="4" fill="#F5C518" class="hp-bar hp2"/>
    </g>
    <text x="162" y="118" font-family="'Courier New',monospace" font-size="8" fill="#F5C518">95</text>
    <text x="95" y="136" font-family="'Courier New',monospace" font-size="13" font-weight="900" fill="#FFFFFF" text-anchor="middle">VOLT MEDIA</text>
    <text x="95" y="150" font-family="'Courier New',monospace" font-size="8" fill="#998877" text-anchor="middle">Creative Digital Brand</text>
    <text x="95" y="162" font-family="'Courier New',monospace" font-size="8" fill="#998877" text-anchor="middle">Next.js · GSAP · Design</text>
  </g>

  <!-- ── Card 3: MediBridge / GRASS type ── -->
  <g transform="translate(440, 46)" class="card c3" filter="url(#cardGlow3)">
    <rect width="190" height="170" rx="10" fill="url(#card3)"/>
    <rect width="190" height="170" rx="10" fill="none" stroke="#4CAF50" stroke-width="1.5"/>
    <rect x="8" y="8" width="50" height="16" rx="8" fill="#4CAF50" opacity="0.3"/>
    <rect x="8" y="8" width="50" height="16" rx="8" fill="none" stroke="#4CAF50" stroke-width="1"/>
    <text x="33" y="20" font-family="'Courier New',monospace" font-size="9" font-weight="700" fill="#4CAF50" text-anchor="middle">GRASS</text>
    <text x="182" y="20" font-family="'Courier New',monospace" font-size="9" fill="#4CAF50" text-anchor="end" opacity="0.7">#003</text>
    <text x="95" y="88" font-size="44" text-anchor="middle">🏥</text>
    <text x="10" y="118" font-family="'Courier New',monospace" font-size="8" fill="#AAAACC">HP</text>
    <rect x="28" y="110" width="130" height="8" rx="4" fill="#0D1E0D"/>
    <g style="transform-origin:28px 114px">
      <rect x="28" y="110" width="110" height="8" rx="4" fill="#4CAF50" class="hp-bar hp3"/>
    </g>
    <text x="162" y="118" font-family="'Courier New',monospace" font-size="8" fill="#4CAF50">85</text>
    <text x="95" y="136" font-family="'Courier New',monospace" font-size="13" font-weight="900" fill="#FFFFFF" text-anchor="middle">MEDIBRIDGE</text>
    <text x="95" y="150" font-family="'Courier New',monospace" font-size="8" fill="#88AA88" text-anchor="middle">Rural AI Healthcare</text>
    <text x="95" y="162" font-family="'Courier New',monospace" font-size="8" fill="#88AA88" text-anchor="middle">Python · AI · WhatsApp</text>
  </g>

  <!-- ── Card 4: PlateShare / FIRE type ── -->
  <g transform="translate(650, 46)" class="card c4" filter="url(#cardGlow4)">
    <rect width="190" height="170" rx="10" fill="url(#card4)"/>
    <rect width="190" height="170" rx="10" fill="none" stroke="#FF4444" stroke-width="1.5"/>
    <rect x="8" y="8" width="42" height="16" rx="8" fill="#FF4444" opacity="0.3"/>
    <rect x="8" y="8" width="42" height="16" rx="8" fill="none" stroke="#FF4444" stroke-width="1"/>
    <text x="29" y="20" font-family="'Courier New',monospace" font-size="9" font-weight="700" fill="#FF4444" text-anchor="middle">FIRE</text>
    <text x="182" y="20" font-family="'Courier New',monospace" font-size="9" fill="#FF4444" text-anchor="end" opacity="0.7">#004</text>
    <text x="95" y="88" font-size="44" text-anchor="middle">🍽</text>
    <text x="10" y="118" font-family="'Courier New',monospace" font-size="8" fill="#AAAACC">HP</text>
    <rect x="28" y="110" width="130" height="8" rx="4" fill="#1E0D0D"/>
    <g style="transform-origin:28px 114px">
      <rect x="28" y="110" width="104" height="8" rx="4" fill="#FF4444" class="hp-bar hp4"/>
    </g>
    <text x="162" y="118" font-family="'Courier New',monospace" font-size="8" fill="#FF4444">80</text>
    <text x="95" y="136" font-family="'Courier New',monospace" font-size="13" font-weight="900" fill="#FFFFFF" text-anchor="middle">PLATESHARE</text>
    <text x="95" y="150" font-family="'Courier New',monospace" font-size="8" fill="#AA8888" text-anchor="middle">Food Waste Marketplace</text>
    <text x="95" y="162" font-family="'Courier New',monospace" font-size="8" fill="#AA8888" text-anchor="middle">React · Node · MongoDB</text>
  </g>
</svg>


<br/>
<br/>

<!-- ════════════════════ GITHUB STATS ══════════════════════ -->

```
◈━━━━━━━━━━━━━━━━━━━━━━ BATTLE RECORD ━━━━━━━━━━━━━━━━━━━━━◈
```

<img height="170"
     src="https://github-readme-stats.vercel.app/api?username=gokulan&show_icons=true&theme=midnight-purple&hide_border=true&bg_color=0D0D1A&title_color=F5C518&icon_color=EE1515&text_color=CCCCFF&border_radius=10"
     alt="GitHub Stats"/>
&nbsp;
<img height="170"
     src="https://github-readme-stats.vercel.app/api/top-langs/?username=gokulan&layout=compact&theme=midnight-purple&hide_border=true&bg_color=0D0D1A&title_color=F5C518&text_color=CCCCFF&border_radius=10"
     alt="Top Languages"/>

<br/>
<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=gokulan&theme=midnight-purple&hide_border=true&background=0D0D1A&stroke=EE1515&ring=F5C518&fire=EE1515&currStreakLabel=F5C518&border_radius=10"
     alt="Streak Stats"
     width="600"/>

<br/>
<br/>

<!-- ═══════════════════ CONTRIBUTION MAP ═══════════════════ -->

```
◈━━━━━━━━━━━━━━━━━━━━ WILD ENCOUNTERS ━━━━━━━━━━━━━━━━━━━━━◈
```

<img src="https://github-readme-activity-graph.vercel.app/graph?username=gokulan&bg_color=0D0D1A&color=F5C518&line=EE1515&point=F5C518&area=true&area_color=EE151520&hide_border=true&border_radius=10"
     alt="Activity Graph"
     width="860"/>

<br/>
<br/>

<!-- ══════════════════ PAC-MAN / SNAKE ═════════════════════ -->

```
◈━━━━━━━━━━━━━━━━━━━ POKÉMON BATTLE FIELD ━━━━━━━━━━━━━━━━━◈
```

<picture>
  <source media="(prefers-color-scheme: dark)"
          srcset="https://raw.githubusercontent.com/gokulan/gokulan/output/github-contribution-grid-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)"
          srcset="https://raw.githubusercontent.com/gokulan/gokulan/output/github-contribution-grid-snake.svg"/>
  <img alt="Contribution Snake"
       src="https://raw.githubusercontent.com/gokulan/gokulan/output/github-contribution-grid-snake-dark.svg"
       width="860"/>
</picture>

<br/>
<br/>

<!-- ══════════════════ TROPHIES ════════════════════════════ -->

```
◈━━━━━━━━━━━━━━━━━━━━━━━━ GYM BADGES ━━━━━━━━━━━━━━━━━━━━━━◈
```

<img src="https://github-profile-trophy.vercel.app/?username=gokulan&theme=darkhub&no-frame=true&no-bg=true&column=7&margin-w=6"
     alt="Trophies"
     width="860"/>

<br/>
<br/>

<!-- ══════════════════ CONNECT ══════════════════════════════ -->

```
◈━━━━━━━━━━━━━━━━━━━━━━━ TRAINER LINKS ━━━━━━━━━━━━━━━━━━━━◈
```

[![GitHub](https://img.shields.io/badge/GitHub-gokulan-F5C518?style=for-the-badge&logo=github&logoColor=F5C518&labelColor=0D0D1A)](https://github.com/gokulan)
[![Instagram](https://img.shields.io/badge/Instagram-@voltmedia.in-EE1515?style=for-the-badge&logo=instagram&logoColor=EE1515&labelColor=0D0D1A)](https://instagram.com/voltmedia.in)
[![Email](https://img.shields.io/badge/Email-gokulan.rkivln-61DAFB?style=for-the-badge&logo=gmail&logoColor=61DAFB&labelColor=0D0D1A)](mailto:gokulan.rkivln@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Gokulan-A855F7?style=for-the-badge&logo=linkedin&logoColor=A855F7&labelColor=0D0D1A)](https://linkedin.com/in/gokulan)

<br/>
<br/>

<!-- ══════════════════ FOOTER ══════════════════════════════ -->

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 860 100" width="860" height="100">
  <defs>
    <linearGradient id="bg4" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#1A1A2E"/>
      <stop offset="100%" stop-color="#0A0A15"/>
    </linearGradient>
    <radialGradient id="r1" cx="50%" cy="40%" r="60%"><stop offset="0%" stop-color="#FF4444"/><stop offset="100%" stop-color="#CC0000"/></radialGradient>
    <radialGradient id="r2" cx="50%" cy="40%" r="60%"><stop offset="0%" stop-color="#FFE566"/><stop offset="100%" stop-color="#F5C518"/></radialGradient>
    <radialGradient id="r3" cx="50%" cy="40%" r="60%"><stop offset="0%" stop-color="#61DAFB"/><stop offset="100%" stop-color="#0EA5E9"/></radialGradient>
    <radialGradient id="r4" cx="50%" cy="40%" r="60%"><stop offset="0%" stop-color="#4CAF50"/><stop offset="100%" stop-color="#2E7D32"/></radialGradient>
    <radialGradient id="r5" cx="50%" cy="40%" r="60%"><stop offset="0%" stop-color="#A855F7"/><stop offset="100%" stop-color="#7C3AED"/></radialGradient>
    <radialGradient id="wh" cx="50%" cy="40%" r="60%"><stop offset="0%" stop-color="#FFFFFF"/><stop offset="100%" stop-color="#CCCCCC"/></radialGradient>
    <style>
      .spin1 { animation: spinBall 4s linear infinite; transform-origin: 20px 20px; }
      .spin2 { animation: spinBall 3s linear infinite 0.5s; transform-origin: 20px 20px; }
      .spin3 { animation: spinBall 5s linear infinite 1s; transform-origin: 20px 20px; }
      .spin4 { animation: spinBall 3.5s linear infinite 1.5s; transform-origin: 20px 20px; }
      .spin5 { animation: spinBall 4.5s linear infinite 0.3s; transform-origin: 20px 20px; }
      .quote { animation: quoteFade 4s ease-in-out infinite; }
      .border-pulse { animation: borderPulse 3s ease-in-out infinite; }
      @keyframes spinBall {
        from { transform: rotate(0deg); }
        to   { transform: rotate(360deg); }
      }
      @keyframes quoteFade {
        0%,100% { opacity:0.7; }
        50%     { opacity:1; }
      }
      @keyframes borderPulse {
        0%,100% { stroke:#EE1515; stroke-opacity:0.6; }
        50%     { stroke:#FF4444; stroke-opacity:1; }
      }
    </style>
  </defs>

  <rect width="860" height="100" fill="url(#bg4)" rx="14"/>
  <rect width="858" height="98" x="1" y="1" fill="none" stroke="#EE1515" stroke-width="1.5" rx="13" class="border-pulse"/>

  <!-- Spinning Pokéballs row -->
  <!-- Ball 1 (Red) -->
  <g transform="translate(70, 30)" class="spin1">
    <path d="M 0,20 A 20,20 0 0,1 40,20 Z" fill="url(#r1)"/>
    <path d="M 0,20 A 20,20 0 0,0 40,20 Z" fill="url(#wh)"/>
    <rect x="0" y="18" width="40" height="4" fill="#111"/>
    <circle cx="20" cy="20" r="6" fill="#333"/>
    <circle cx="20" cy="20" r="4" fill="url(#wh)"/>
  </g>

  <!-- Ball 2 (Yellow) -->
  <g transform="translate(200, 30)" class="spin2">
    <path d="M 0,20 A 20,20 0 0,1 40,20 Z" fill="url(#r2)"/>
    <path d="M 0,20 A 20,20 0 0,0 40,20 Z" fill="url(#wh)"/>
    <rect x="0" y="18" width="40" height="4" fill="#111"/>
    <circle cx="20" cy="20" r="6" fill="#333"/>
    <circle cx="20" cy="20" r="4" fill="url(#wh)"/>
  </g>

  <!-- Ball 3 (Cyan) -->
  <g transform="translate(330, 30)" class="spin3">
    <path d="M 0,20 A 20,20 0 0,1 40,20 Z" fill="url(#r3)"/>
    <path d="M 0,20 A 20,20 0 0,0 40,20 Z" fill="url(#wh)"/>
    <rect x="0" y="18" width="40" height="4" fill="#111"/>
    <circle cx="20" cy="20" r="6" fill="#333"/>
    <circle cx="20" cy="20" r="4" fill="url(#wh)"/>
  </g>

  <!-- Ball 4 (Green) -->
  <g transform="translate(460, 30)" class="spin4">
    <path d="M 0,20 A 20,20 0 0,1 40,20 Z" fill="url(#r4)"/>
    <path d="M 0,20 A 20,20 0 0,0 40,20 Z" fill="url(#wh)"/>
    <rect x="0" y="18" width="40" height="4" fill="#111"/>
    <circle cx="20" cy="20" r="6" fill="#333"/>
    <circle cx="20" cy="20" r="4" fill="url(#wh)"/>
  </g>

  <!-- Ball 5 (Purple) -->
  <g transform="translate(590, 30)" class="spin5">
    <path d="M 0,20 A 20,20 0 0,1 40,20 Z" fill="url(#r5)"/>
    <path d="M 0,20 A 20,20 0 0,0 40,20 Z" fill="url(#wh)"/>
    <rect x="0" y="18" width="40" height="4" fill="#111"/>
    <circle cx="20" cy="20" r="6" fill="#333"/>
    <circle cx="20" cy="20" r="4" fill="url(#wh)"/>
  </g>

  <!-- Ball 6 (Red again) -->
  <g transform="translate(720, 30)" class="spin1">
    <path d="M 0,20 A 20,20 0 0,1 40,20 Z" fill="url(#r1)"/>
    <path d="M 0,20 A 20,20 0 0,0 40,20 Z" fill="url(#wh)"/>
    <rect x="0" y="18" width="40" height="4" fill="#111"/>
    <circle cx="20" cy="20" r="6" fill="#333"/>
    <circle cx="20" cy="20" r="4" fill="url(#wh)"/>
  </g>

  <!-- Quote -->
  <text x="430" y="84" font-family="'Courier New',monospace" font-size="11" fill="#F5C518"
        text-anchor="middle" letter-spacing="1" class="quote">
    ✦ Gotta Build Em All · RKIVLN · Volt Media · 2026 ✦
  </text>
</svg>


<br/>

![Profile Views](https://komarev.com/ghpvc/?username=gokulan&color=EE1515&style=for-the-badge&label=TRAINERS+VISITED&labelColor=0D0D1A)

</div>


