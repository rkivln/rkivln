<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Gokulan Anbalagan – F1 Edition</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;600;700;900&family=Barlow:wght@400;500;600&family=Share+Tech+Mono&display=swap" rel="stylesheet"/>
<style>
:root {
  --f1-red: #E8002D;
  --f1-dark: #0a0a0f;
  --f1-darker: #050508;
  --f1-mid: #111118;
  --f1-card: #14141e;
  --f1-border: #2a2a3a;
  --f1-muted: #5a5a7a;
  --f1-text: #e8e8f0;
  --f1-dim: #9090b0;
  --f1-accent: #E8002D;
  --f1-gold: #FFD700;
  --f1-silver: #C0C0C0;
  --f1-bronze: #CD7F32;
  --font-display: 'Barlow Condensed', sans-serif;
  --font-body: 'Barlow', sans-serif;
  --font-mono: 'Share Tech Mono', monospace;
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
body{background:var(--f1-darker);color:var(--f1-text);font-family:var(--font-body);font-size:16px;line-height:1.6;overflow-x:hidden}
a{color:var(--f1-red);text-decoration:none}
a:hover{text-decoration:underline}

/* ── HERO ── */
.hero{position:relative;background:var(--f1-darker);overflow:hidden;padding:0}
.hero-inner{max-width:960px;margin:0 auto;padding:60px 32px 40px;position:relative;z-index:2}
.hero-grid{display:grid;grid-template-columns:1fr auto;gap:32px;align-items:center}
.hero-name{font-family:var(--font-display);font-weight:900;font-size:clamp(48px,8vw,96px);line-height:0.9;letter-spacing:-1px;color:#fff;text-transform:uppercase}
.hero-name span{color:var(--f1-red)}
.hero-role{font-family:var(--font-display);font-size:22px;font-weight:600;color:var(--f1-dim);text-transform:uppercase;letter-spacing:3px;margin-top:12px}
.hero-number{font-family:var(--font-display);font-weight:900;font-size:200px;color:rgba(232,0,45,0.08);line-height:1;letter-spacing:-8px;user-select:none}
.helmet-row{display:flex;gap:16px;margin-top:28px;flex-wrap:wrap}
.badge{display:inline-flex;align-items:center;gap:6px;background:var(--f1-card);border:1px solid var(--f1-border);border-radius:4px;padding:6px 14px;font-family:var(--font-display);font-size:14px;font-weight:600;letter-spacing:1px;text-transform:uppercase;color:var(--f1-dim);transition:border-color .2s,color .2s}
.badge:hover{border-color:var(--f1-red);color:var(--f1-text)}
.badge .dot{width:8px;height:8px;border-radius:50%;flex-shrink:0}

/* Hero stripe */
.hero-stripe{height:6px;background:linear-gradient(90deg,var(--f1-red) 0%,var(--f1-red) 40%,#222 40%)}

/* ── SECTION LABELS ── */
.section{max-width:960px;margin:0 auto;padding:0 32px 60px}
.section-label{display:flex;align-items:center;gap:16px;margin-bottom:32px;padding-top:48px}
.section-label-text{font-family:var(--font-display);font-size:13px;font-weight:700;letter-spacing:3px;text-transform:uppercase;color:var(--f1-red)}
.section-label-line{flex:1;height:1px;background:var(--f1-border)}
.section-title{font-family:var(--font-display);font-size:36px;font-weight:900;text-transform:uppercase;color:#fff;margin-bottom:8px}
.section-sub{color:var(--f1-dim);font-size:15px;margin-bottom:32px}

/* ── F1 CAR SVG ── */
.car-showcase{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;padding:32px;margin-bottom:40px;overflow:hidden;position:relative}
.car-showcase::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:var(--f1-red)}

/* ── TEAM GRID ── */
.teams-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:16px}
.team-card{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;padding:20px;display:flex;flex-direction:column;align-items:flex-start;gap:12px;transition:border-color .2s,transform .15s;position:relative;overflow:hidden}
.team-card:hover{border-color:var(--tc,var(--f1-red));transform:translateY(-2px)}
.team-card::after{content:'';position:absolute;bottom:0;left:0;right:0;height:3px;background:var(--tc,var(--f1-red))}
.team-logo-svg{width:100%;height:36px}
.team-name{font-family:var(--font-display);font-size:16px;font-weight:700;text-transform:uppercase;letter-spacing:1px;color:#fff}
.team-role{font-size:13px;color:var(--f1-dim);font-family:var(--font-mono)}
.team-tech{display:flex;flex-wrap:wrap;gap:6px;margin-top:4px}
.tech-pill{background:rgba(255,255,255,0.05);border:1px solid var(--f1-border);border-radius:3px;padding:2px 8px;font-size:11px;font-family:var(--font-mono);color:var(--f1-dim)}

/* ── DRIVER CARD / PROJECT POKEDEX ── */
.pokedex-grid{display:grid;gap:16px}
.project-card{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;display:grid;grid-template-columns:auto 1fr;gap:0;overflow:hidden;transition:border-color .2s}
.project-card:hover{border-color:var(--pc,var(--f1-red))}
.project-num{width:72px;background:var(--pc,var(--f1-red));display:flex;align-items:center;justify-content:center;flex-direction:column;gap:4px;flex-shrink:0}
.project-num-text{font-family:var(--font-display);font-size:36px;font-weight:900;color:#fff;line-height:1}
.project-num-sub{font-family:var(--font-display);font-size:10px;font-weight:600;color:rgba(255,255,255,0.6);letter-spacing:2px;text-transform:uppercase}
.project-body{padding:20px 24px}
.project-title{font-family:var(--font-display);font-size:22px;font-weight:900;text-transform:uppercase;color:#fff}
.project-type{font-size:12px;color:var(--pc,var(--f1-red));font-family:var(--font-mono);letter-spacing:1px;text-transform:uppercase;margin-bottom:6px}
.project-desc{font-size:14px;color:var(--f1-dim);margin-bottom:12px}
.project-links{display:flex;gap:12px;font-size:13px;font-family:var(--font-display);font-weight:600;text-transform:uppercase;letter-spacing:1px}
.project-links a{color:var(--f1-dim);border:1px solid var(--f1-border);padding:4px 12px;border-radius:3px;transition:color .2s,border-color .2s}
.project-links a:hover{color:#fff;border-color:var(--pc,var(--f1-red));text-decoration:none}

/* ── STATS ── */
.stats-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:16px;margin-bottom:24px}
.stat-card{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;padding:20px;position:relative;overflow:hidden}
.stat-card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:var(--f1-red)}
.stat-label{font-family:var(--font-display);font-size:11px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--f1-muted);margin-bottom:8px}
.stat-value{font-family:var(--font-display);font-size:40px;font-weight:900;color:#fff;line-height:1}
.stat-sub{font-size:12px;color:var(--f1-dim);margin-top:4px;font-family:var(--font-mono)}

/* ── STREAK ── */
.streak-bar{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;padding:24px;margin-bottom:24px}
.streak-label{font-family:var(--font-display);font-size:12px;font-weight:700;letter-spacing:3px;text-transform:uppercase;color:var(--f1-muted);margin-bottom:16px}
.streak-row{display:flex;gap:8px;flex-wrap:wrap}
.streak-dot{width:14px;height:14px;border-radius:2px;background:var(--f1-border);flex-shrink:0}
.streak-dot.hot{background:var(--f1-red)}
.streak-dot.warm{background:#a00020}
.streak-dot.cool{background:#600015}

/* ── TROPHIES ── */
.trophy-row{display:flex;gap:16px;flex-wrap:wrap;margin-bottom:40px}
.trophy{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;padding:16px 20px;text-align:center;flex:1;min-width:120px}
.trophy-icon{font-size:28px;margin-bottom:6px}
.trophy-name{font-family:var(--font-display);font-size:13px;font-weight:700;text-transform:uppercase;letter-spacing:1px;color:var(--f1-dim)}
.trophy-count{font-family:var(--font-display);font-size:22px;font-weight:900;color:#fff}

/* ── CONNECT ── */
.connect-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:16px}
.connect-card{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;padding:20px;display:flex;align-items:center;gap:14px;transition:border-color .2s,transform .15s}
.connect-card:hover{border-color:var(--f1-red);transform:translateX(3px);text-decoration:none}
.connect-icon{width:40px;height:40px;border-radius:4px;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.connect-name{font-family:var(--font-display);font-size:16px;font-weight:700;text-transform:uppercase;letter-spacing:1px;color:#fff}
.connect-handle{font-size:12px;color:var(--f1-dim);font-family:var(--font-mono)}

/* ── ACTIVITY GRID ── */
.activity-track{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;padding:24px;margin-bottom:40px;overflow-x:auto}
.activity-grid{display:flex;gap:3px;align-items:flex-end}
.activity-week{display:flex;flex-direction:column;gap:3px}
.activity-cell{width:12px;height:12px;border-radius:2px;background:var(--f1-border)}
.activity-cell.lvl1{background:#600015}
.activity-cell.lvl2{background:#9c001f}
.activity-cell.lvl3{background:#cc0028}
.activity-cell.lvl4{background:var(--f1-red)}
.month-labels{display:flex;gap:3px;margin-bottom:8px;padding-left:0}
.month-label{font-family:var(--font-mono);font-size:10px;color:var(--f1-muted);width:auto;white-space:nowrap}

/* ── FOOTER ── */
.footer{border-top:1px solid var(--f1-border);padding:40px 32px;text-align:center;background:var(--f1-darker)}
.footer-text{font-family:var(--font-display);font-size:18px;font-weight:700;text-transform:uppercase;letter-spacing:3px;color:var(--f1-muted)}
.footer-sub{font-family:var(--font-mono);font-size:12px;color:var(--f1-border);margin-top:8px}
.footer-logo{font-family:var(--font-display);font-size:48px;font-weight:900;color:rgba(232,0,45,0.12);letter-spacing:-2px;margin:16px 0}

/* ── TOP STRIPE ── */
.topbar{height:4px;background:var(--f1-red);width:100%}

/* ── LANGUAGE BAR ── */
.lang-bar-wrap{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;padding:24px;margin-bottom:24px}
.lang-bar-track{height:8px;border-radius:4px;display:flex;overflow:hidden;gap:2px;margin-bottom:16px}
.lang-seg{height:100%;border-radius:2px;transition:flex .4s}
.lang-legend{display:flex;flex-wrap:wrap;gap:16px}
.lang-item{display:flex;align-items:center;gap:6px;font-size:13px;font-family:var(--font-mono);color:var(--f1-dim)}
.lang-dot{width:10px;height:10px;border-radius:50%;flex-shrink:0}

/* ── SCROLLBAR ── */
::-webkit-scrollbar{width:6px;height:6px}
::-webkit-scrollbar-track{background:var(--f1-darker)}
::-webkit-scrollbar-thumb{background:var(--f1-border);border-radius:3px}
::-webkit-scrollbar-thumb:hover{background:var(--f1-red)}

/* ── RACE POSITION BANNER ── */
.race-banner{background:var(--f1-red);padding:10px 32px;display:flex;align-items:center;gap:24px;overflow:hidden;white-space:nowrap}
.race-ticker{font-family:var(--font-display);font-size:13px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:#fff;animation:ticker 30s linear infinite}
@keyframes ticker{0%{transform:translateX(0)}100%{transform:translateX(-50%)}}
.race-flag{font-size:16px;margin-right:4px}

/* ── MOVESET / SKILL ── */
.skill-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(160px,1fr));gap:12px}
.skill-card{background:var(--f1-card);border:1px solid var(--f1-border);border-radius:8px;padding:16px;transition:border-color .2s}
.skill-card:hover{border-color:var(--sc,var(--f1-red))}
.skill-name{font-family:var(--font-display);font-size:15px;font-weight:700;text-transform:uppercase;letter-spacing:1px;color:#fff;margin-bottom:6px}
.skill-bar-track{height:4px;background:var(--f1-border);border-radius:2px;overflow:hidden}
.skill-bar{height:100%;border-radius:2px;background:var(--sc,var(--f1-red))}
.skill-type{font-size:11px;color:var(--sc,var(--f1-dim));font-family:var(--font-mono);text-transform:uppercase;letter-spacing:1px;margin-top:6px}

/* ── RESPONSIVE ── */
@media(max-width:600px){
  .hero-grid{grid-template-columns:1fr}
  .hero-number{display:none}
  .project-card{grid-template-columns:1fr}
  .project-num{width:100%;padding:12px;flex-direction:row;justify-content:flex-start}
}
</style>
</head>
<body>

<!-- Top stripe -->
<div class="topbar"></div>

<!-- Race ticker -->
<div class="race-banner">
  <div class="race-ticker">
    <span class="race-flag">🏁</span> FULL THROTTLE DEVELOPER &nbsp;&nbsp;&nbsp;
    <span class="race-flag">⚡</span> REACT · NEXT.JS · TAILWIND · PYTHON · FIGMA · AWS &nbsp;&nbsp;&nbsp;
    <span class="race-flag">🔴</span> GOKULAN ANBALAGAN · CONSTRUCTOR CHAMPIONSHIP LEADER &nbsp;&nbsp;&nbsp;
    <span class="race-flag">🏁</span> FULL THROTTLE DEVELOPER &nbsp;&nbsp;&nbsp;
    <span class="race-flag">⚡</span> REACT · NEXT.JS · TAILWIND · PYTHON · FIGMA · AWS &nbsp;&nbsp;&nbsp;
    <span class="race-flag">🔴</span> GOKULAN ANBALAGAN · CONSTRUCTOR CHAMPIONSHIP LEADER &nbsp;&nbsp;&nbsp;
  </div>
</div>

<!-- ══════════════════════════ HERO ══════════════════════════ -->
<div class="hero">
  <div class="hero-inner">
    <div class="hero-grid">
      <div>
        <div class="hero-name">Gokulan<br/><span>Anbalagan</span></div>
        <div class="hero-role">Full-Stack Developer · UI/UX Designer</div>
        <div class="helmet-row">
          <span class="badge"><span class="dot" style="background:#E8002D"></span>React</span>
          <span class="badge"><span class="dot" style="background:#fff"></span>Next.js</span>
          <span class="badge"><span class="dot" style="background:#38BDF8"></span>Tailwind</span>
          <span class="badge"><span class="dot" style="background:#FFD43B"></span>Python</span>
          <span class="badge"><span class="dot" style="background:#F24E1E"></span>Figma</span>
          <span class="badge"><span class="dot" style="background:#FF9900"></span>AWS</span>
        </div>
      </div>
      <div class="hero-number">44</div>
    </div>
  </div>

  <!-- F1 Car SVG -->
  <div class="car-showcase" style="margin:0;border-radius:0;border-left:none;border-right:none;border-bottom:none">
    <svg viewBox="0 0 960 220" width="100%" xmlns="http://www.w3.org/2000/svg" style="display:block">
      <!-- Track background lines -->
      <line x1="0" y1="180" x2="960" y2="180" stroke="#1a1a2a" stroke-width="1"/>
      <line x1="0" y1="185" x2="960" y2="185" stroke="#1a1a2a" stroke-width="0.5"/>

      <!-- === F1 CAR (centered) === -->
      <g transform="translate(150,30)">
        <!-- Shadow -->
        <ellipse cx="330" cy="175" rx="260" ry="12" fill="rgba(0,0,0,0.5)"/>

        <!-- REAR WING -->
        <rect x="30" y="68" width="90" height="8" rx="2" fill="#cc0020"/>
        <rect x="30" y="58" width="90" height="7" rx="2" fill="#e8002d"/>
        <rect x="50" y="76" width="6" height="30" rx="1" fill="#555"/>
        <rect x="94" y="76" width="6" height="30" rx="1" fill="#555"/>

        <!-- REAR DIFFUSER -->
        <path d="M80 158 L120 148 L200 145 L200 158 Z" fill="#111"/>
        <path d="M80 158 L120 148 L120 158 Z" fill="#1a1a2a"/>
        <path d="M120 148 L160 145 L160 158 L120 158 Z" fill="#222"/>

        <!-- MAIN BODY - sidepods -->
        <path d="M130 100 Q160 88 240 85 L500 85 Q530 88 560 100 L560 150 Q530 160 500 158 L240 158 Q160 160 130 150 Z" fill="#E8002D"/>

        <!-- Body highlight -->
        <path d="M150 95 Q200 87 280 85 L480 85 Q520 87 550 95 L540 100 Q500 92 480 90 L280 90 Q200 92 160 100 Z" fill="rgba(255,255,255,0.08)"/>

        <!-- NOSE CONE -->
        <path d="M500 108 L620 100 L640 118 L620 136 L500 128 Z" fill="#cc0020"/>
        <path d="M500 108 L620 100 L625 108 L500 118 Z" fill="rgba(255,255,255,0.05)"/>
        <!-- Nose tip -->
        <path d="M620 100 L660 110 L660 126 L620 136 Z" fill="#999"/>
        <path d="M655 110 L675 116 L675 120 L655 126 Z" fill="#bbb"/>

        <!-- COCKPIT / HALO -->
        <path d="M350 85 Q380 60 420 58 Q460 58 480 85 Z" fill="#1a1a2a"/>
        <path d="M355 85 Q383 64 420 62 Q455 63 475 85 Z" fill="#0a0a12"/>
        <!-- Halo arch -->
        <path d="M345 85 Q390 52 430 50 Q470 50 490 85" fill="none" stroke="#333" stroke-width="6" stroke-linecap="round"/>
        <path d="M345 85 Q390 52 430 50 Q470 50 490 85" fill="none" stroke="#555" stroke-width="3" stroke-linecap="round"/>
        <!-- Visor -->
        <path d="M375 78 Q400 66 430 65 Q460 66 460 78 Q445 72 430 70 Q410 70 375 78 Z" fill="#1a3a6a" opacity="0.8"/>

        <!-- SIDEPODS detail lines -->
        <line x1="180" y1="100" x2="500" y2="100" stroke="rgba(0,0,0,0.3)" stroke-width="1"/>
        <line x1="180" y1="110" x2="500" y2="110" stroke="rgba(0,0,0,0.2)" stroke-width="0.5"/>

        <!-- NUMBER on sidepod -->
        <text x="260" y="135" font-family="Barlow Condensed,sans-serif" font-size="32" font-weight="900" fill="white" opacity="0.9">01</text>

        <!-- GOKULAN text -->
        <text x="320" y="130" font-family="Barlow Condensed,sans-serif" font-size="14" font-weight="700" fill="rgba(255,255,255,0.5)" letter-spacing="3">GOKULAN</text>

        <!-- FRONT WING -->
        <!-- Main plane -->
        <rect x="520" y="140" width="130" height="7" rx="1" fill="#cc0020"/>
        <rect x="520" y="148" width="130" height="5" rx="1" fill="#aaa"/>
        <!-- End plates -->
        <rect x="520" y="130" width="5" height="30" rx="1" fill="#999"/>
        <rect x="645" y="130" width="5" height="30" rx="1" fill="#999"/>
        <!-- Additional flaps -->
        <path d="M525 140 L650 136 L650 140 L525 144 Z" fill="rgba(255,255,255,0.1)"/>

        <!-- FRONT SUSPENSION -->
        <line x1="580" y1="155" x2="590" y2="168" stroke="#444" stroke-width="3"/>
        <line x1="600" y1="155" x2="590" y2="168" stroke="#444" stroke-width="3"/>

        <!-- REAR SUSPENSION -->
        <line x1="160" y1="155" x2="150" y2="168" stroke="#444" stroke-width="3"/>
        <line x1="180" y1="155" x2="150" y2="168" stroke="#444" stroke-width="3"/>

        <!-- === WHEELS === -->
        <!-- Rear Left -->
        <circle cx="150" cy="168" r="28" fill="#222" stroke="#444" stroke-width="2"/>
        <circle cx="150" cy="168" r="20" fill="#333"/>
        <circle cx="150" cy="168" r="12" fill="#555"/>
        <circle cx="150" cy="168" r="5" fill="#888"/>
        <!-- Rear tyre detail -->
        <path d="M128 148 A28 28 0 0 1 172 148" fill="none" stroke="#e8002d" stroke-width="3" stroke-linecap="round"/>

        <!-- Rear Right -->
        <circle cx="150" cy="168" r="28" fill="#222" stroke="#444" stroke-width="2"/>
        <!-- (same wheel, hidden behind body) -->

        <!-- Front Right -->
        <circle cx="590" cy="168" r="24" fill="#222" stroke="#444" stroke-width="2"/>
        <circle cx="590" cy="168" r="16" fill="#333"/>
        <circle cx="590" cy="168" r="9" fill="#555"/>
        <circle cx="590" cy="168" r="4" fill="#888"/>
        <!-- Front tyre detail -->
        <path d="M570 150 A24 24 0 0 1 610 150" fill="none" stroke="#e8002d" stroke-width="3" stroke-linecap="round"/>

        <!-- Front Left (visible) -->
        <circle cx="590" cy="168" r="24" fill="#222" stroke="#444" stroke-width="2"/>

        <!-- FRONT BARGE BOARDS / TURNING VANES -->
        <path d="M510 130 L520 125 L520 140 L510 140 Z" fill="#aaa"/>
        <path d="M505 120 L515 116 L515 128 L505 128 Z" fill="#888"/>

        <!-- AIR INTAKE -->
        <rect x="405" y="72" width="30" height="14" rx="3" fill="#0a0a12"/>
        <rect x="407" y="74" width="26" height="10" rx="2" fill="#050508"/>

        <!-- DRS / ENGINE COVER detail -->
        <path d="M340 85 L490 85 L490 100 L340 100 Z" fill="rgba(0,0,0,0.2)"/>
        <line x1="360" y1="85" x2="360" y2="100" stroke="rgba(255,255,255,0.05)" stroke-width="1"/>
        <line x1="400" y1="85" x2="400" y2="100" stroke="rgba(255,255,255,0.05)" stroke-width="1"/>
        <line x1="440" y1="85" x2="440" y2="100" stroke="rgba(255,255,255,0.05)" stroke-width="1"/>

        <!-- EXHAUST -->
        <circle cx="120" cy="108" r="6" fill="#222" stroke="#555" stroke-width="1"/>
        <!-- Heat shimmer lines -->
        <line x1="105" y1="100" x2="95" y2="85" stroke="#ff6030" stroke-width="1" opacity="0.3"/>
        <line x1="110" y1="98" x2="98" y2="80" stroke="#ff8040" stroke-width="0.5" opacity="0.2"/>
        <line x1="100" y1="102" x2="88" y2="86" stroke="#ff4020" stroke-width="0.5" opacity="0.2"/>
      </g>

      <!-- Track marks -->
      <rect x="0" y="190" width="960" height="2" fill="#1a1a28"/>
      <rect x="0" y="194" width="960" height="30" fill="#0d0d18"/>

      <!-- Circuit dots/curbs -->
      <rect x="40" y="192" width="20" height="4" fill="#E8002D" rx="1"/>
      <rect x="70" y="192" width="20" height="4" fill="white" rx="1"/>
      <rect x="100" y="192" width="20" height="4" fill="#E8002D" rx="1"/>
      <rect x="130" y="192" width="20" height="4" fill="white" rx="1"/>
      <rect x="800" y="192" width="20" height="4" fill="#E8002D" rx="1"/>
      <rect x="830" y="192" width="20" height="4" fill="white" rx="1"/>
      <rect x="860" y="192" width="20" height="4" fill="#E8002D" rx="1"/>
      <rect x="890" y="192" width="20" height="4" fill="white" rx="1"/>

      <!-- PIT BOARD (right side) -->
      <rect x="855" y="30" width="80" height="100" rx="4" fill="#111" stroke="#333" stroke-width="1"/>
      <rect x="855" y="30" width="80" height="28" rx="4" fill="#E8002D"/>
      <text x="895" y="49" font-family="Barlow Condensed,sans-serif" font-size="14" font-weight="900" fill="white" text-anchor="middle">LAP</text>
      <text x="895" y="80" font-family="Barlow Condensed,sans-serif" font-size="28" font-weight="900" fill="white" text-anchor="middle">01</text>
      <text x="895" y="100" font-family="Barlow Condensed,sans-serif" font-size="11" font-weight="600" fill="#aaa" text-anchor="middle">P1 +0.000</text>
      <text x="895" y="118" font-family="Barlow Condensed,sans-serif" font-size="10" font-weight="600" fill="#FFD700" text-anchor="middle">PURPLE</text>

      <!-- Traffic lights (left) -->
      <rect x="25" y="25" width="30" height="110" rx="4" fill="#111" stroke="#333" stroke-width="1"/>
      <circle cx="40" cy="50" r="10" fill="#cc0000"/>
      <circle cx="40" cy="75" r="10" fill="#cc0000"/>
      <circle cx="40" cy="100" r="10" fill="#cc0000"/>
      <circle cx="40" cy="125" r="10" fill="#333"/>
      <circle cx="40" cy="50" r="7" fill="#ff2020" opacity="0.9"/>
      <circle cx="40" cy="75" r="7" fill="#ff2020" opacity="0.7"/>
      <circle cx="40" cy="100" r="7" fill="#ff2020" opacity="0.4"/>
    </svg>
  </div>
</div>
<div class="hero-stripe"></div>

<!-- ══════════════════════ CONSTRUCTORS (TECH SKILLS) ══════════════════════ -->
<div class="section">
  <div class="section-label">
    <div class="section-label-text">Constructors Championship</div>
    <div class="section-label-line"></div>
  </div>
  <div class="section-title">Tech Stack</div>
  <div class="section-sub">Each constructor represents a core technology — full points for mastery</div>

  <div class="teams-grid">

    <!-- Red Bull / React -->
    <div class="team-card" style="--tc:#0600EF">
      <svg class="team-logo-svg" viewBox="0 0 200 36" xmlns="http://www.w3.org/2000/svg">
        <!-- Red Bull logo approximation -->
        <circle cx="18" cy="18" r="16" fill="#0600EF"/>
        <circle cx="18" cy="18" r="10" fill="#CC0000"/>
        <text x="38" y="23" font-family="Barlow Condensed,sans-serif" font-size="20" font-weight="900" fill="#0600EF" letter-spacing="1">RED BULL</text>
        <text x="38" y="34" font-family="Barlow Condensed,sans-serif" font-size="11" font-weight="600" fill="#555" letter-spacing="2">RACING</text>
      </svg>
      <div class="team-name">React</div>
      <div class="team-role">WATER TYPE · FRONTEND</div>
      <div class="team-tech">
        <span class="tech-pill">Hooks</span>
        <span class="tech-pill">Context</span>
        <span class="tech-pill">Redux</span>
      </div>
    </div>

    <!-- Mercedes / Next.js -->
    <div class="team-card" style="--tc:#00D2BE">
      <svg class="team-logo-svg" viewBox="0 0 200 36" xmlns="http://www.w3.org/2000/svg">
        <circle cx="18" cy="18" r="16" fill="#00D2BE" opacity="0.15" stroke="#00D2BE" stroke-width="1.5"/>
        <path d="M18 6 L18 30 M10 12 L18 6 L26 12" stroke="#00D2BE" stroke-width="2.5" fill="none" stroke-linecap="round"/>
        <text x="38" y="23" font-family="Barlow Condensed,sans-serif" font-size="20" font-weight="900" fill="#00D2BE" letter-spacing="1">MERCEDES</text>
        <text x="38" y="34" font-family="Barlow Condensed,sans-serif" font-size="11" font-weight="600" fill="#555" letter-spacing="2">AMG PETRONAS</text>
      </svg>
      <div class="team-name">Next.js</div>
      <div class="team-role">NORMAL TYPE · FULLSTACK</div>
      <div class="team-tech">
        <span class="tech-pill">SSR</span>
        <span class="tech-pill">API Routes</span>
        <span class="tech-pill">ISR</span>
      </div>
    </div>

    <!-- Ferrari / Python -->
    <div class="team-card" style="--tc:#DC0000">
      <svg class="team-logo-svg" viewBox="0 0 200 36" xmlns="http://www.w3.org/2000/svg">
        <!-- Ferrari horse approximation -->
        <rect x="4" y="4" width="28" height="28" rx="2" fill="#DC0000"/>
        <text x="18" y="23" font-family="Barlow Condensed,sans-serif" font-size="20" font-weight="900" fill="#FFD700" text-anchor="middle">SF</text>
        <text x="38" y="23" font-family="Barlow Condensed,sans-serif" font-size="20" font-weight="900" fill="#DC0000" letter-spacing="1">FERRARI</text>
        <text x="38" y="34" font-family="Barlow Condensed,sans-serif" font-size="11" font-weight="600" fill="#555" letter-spacing="2">SCUDERIA</text>
      </svg>
      <div class="team-name">Python</div>
      <div class="team-role">ELECTRIC TYPE · BACKEND</div>
      <div class="team-tech">
        <span class="tech-pill">FastAPI</span>
        <span class="tech-pill">NumPy</span>
        <span class="tech-pill">Pandas</span>
      </div>
    </div>

    <!-- McLaren / TailwindCSS -->
    <div class="team-card" style="--tc:#FF8000">
      <svg class="team-logo-svg" viewBox="0 0 200 36" xmlns="http://www.w3.org/2000/svg">
        <path d="M4 28 Q18 4 32 28" fill="none" stroke="#FF8000" stroke-width="3" stroke-linecap="round"/>
        <path d="M4 28 Q18 10 32 28" fill="rgba(255,128,0,0.1)"/>
        <text x="38" y="23" font-family="Barlow Condensed,sans-serif" font-size="20" font-weight="900" fill="#FF8000" letter-spacing="1">McLAREN</text>
        <text x="38" y="34" font-family="Barlow Condensed,sans-serif" font-size="11" font-weight="600" fill="#555" letter-spacing="2">FORMULA 1</text>
      </svg>
      <div class="team-name">Tailwind CSS</div>
      <div class="team-role">ICE TYPE · STYLING</div>
      <div class="team-tech">
        <span class="tech-pill">Responsive</span>
        <span class="tech-pill">Dark Mode</span>
        <span class="tech-pill">JIT</span>
      </div>
    </div>

    <!-- Alpine / Figma -->
    <div class="team-card" style="--tc:#0090FF">
      <svg class="team-logo-svg" viewBox="0 0 200 36" xmlns="http://www.w3.org/2000/svg">
        <path d="M4 28 L18 6 L32 28 Z" fill="none" stroke="#0090FF" stroke-width="2" stroke-linejoin="round"/>
        <path d="M10 28 L18 14 L26 28 Z" fill="#0090FF" opacity="0.3"/>
        <text x="38" y="23" font-family="Barlow Condensed,sans-serif" font-size="20" font-weight="900" fill="#0090FF" letter-spacing="1">ALPINE</text>
        <text x="38" y="34" font-family="Barlow Condensed,sans-serif" font-size="11" font-weight="600" fill="#555" letter-spacing="2">BWT · F1 TEAM</text>
      </svg>
      <div class="team-name">Figma</div>
      <div class="team-role">FIRE TYPE · DESIGN</div>
      <div class="team-tech">
        <span class="tech-pill">Prototyping</span>
        <span class="tech-pill">Design Sys</span>
        <span class="tech-pill">Auto Layout</span>
      </div>
    </div>

    <!-- Aston Martin / AWS -->
    <div class="team-card" style="--tc:#006F62">
      <svg class="team-logo-svg" viewBox="0 0 200 36" xmlns="http://www.w3.org/2000/svg">
        <rect x="4" y="10" width="28" height="18" rx="3" fill="none" stroke="#006F62" stroke-width="2"/>
        <text x="18" y="23" font-family="Barlow Condensed,sans-serif" font-size="11" font-weight="900" fill="#006F62" text-anchor="middle">AMF1</text>
        <text x="38" y="23" font-family="Barlow Condensed,sans-serif" font-size="20" font-weight="900" fill="#006F62" letter-spacing="1">ASTON</text>
        <text x="38" y="34" font-family="Barlow Condensed,sans-serif" font-size="11" font-weight="600" fill="#555" letter-spacing="2">MARTIN</text>
      </svg>
      <div class="team-name">AWS</div>
      <div class="team-role">FLYING TYPE · CLOUD</div>
      <div class="team-tech">
        <span class="tech-pill">EC2</span>
        <span class="tech-pill">S3</span>
        <span class="tech-pill">Lambda</span>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════════════ MOVE SET (SKILLS) ══════════════════════ -->
<div class="section">
  <div class="section-label">
    <div class="section-label-text">Driver's Move Set</div>
    <div class="section-label-line"></div>
  </div>
  <div class="section-title">Skills &amp; Abilities</div>
  <div class="section-sub">Performance metrics — each lap of practice sharpens the edge</div>

  <div class="skill-grid">
    <div class="skill-card" style="--sc:#61DAFB">
      <div class="skill-name">React</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:95%"></div></div>
      <div class="skill-type">Hydro Blast</div>
    </div>
    <div class="skill-card" style="--sc:#fff">
      <div class="skill-name">Next.js</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:88%;background:#fff"></div></div>
      <div class="skill-type">Normal Beam</div>
    </div>
    <div class="skill-card" style="--sc:#38BDF8">
      <div class="skill-name">Tailwind</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:92%;background:#38BDF8"></div></div>
      <div class="skill-type">Ice Fang</div>
    </div>
    <div class="skill-card" style="--sc:#FFD43B">
      <div class="skill-name">Python</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:80%;background:#FFD43B"></div></div>
      <div class="skill-type">Thunder Strike</div>
    </div>
    <div class="skill-card" style="--sc:#F24E1E">
      <div class="skill-name">Figma</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:90%;background:#F24E1E"></div></div>
      <div class="skill-type">Fire Spin</div>
    </div>
    <div class="skill-card" style="--sc:#FF9900">
      <div class="skill-name">AWS</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:75%;background:#FF9900"></div></div>
      <div class="skill-type">Sky Attack</div>
    </div>
    <div class="skill-card" style="--sc:#3178C6">
      <div class="skill-name">TypeScript</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:85%;background:#3178C6"></div></div>
      <div class="skill-type">Precision Strike</div>
    </div>
    <div class="skill-card" style="--sc:#4DB33D">
      <div class="skill-name">MongoDB</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:70%;background:#4DB33D"></div></div>
      <div class="skill-type">Grass Knot</div>
    </div>
    <div class="skill-card" style="--sc:#336791">
      <div class="skill-name">PostgreSQL</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:78%;background:#336791"></div></div>
      <div class="skill-type">Aqua Tail</div>
    </div>
    <div class="skill-card" style="--sc:#E8002D">
      <div class="skill-name">Node.js</div>
      <div class="skill-bar-track"><div class="skill-bar" style="width:82%"></div></div>
      <div class="skill-type">Overdrive</div>
    </div>
  </div>
</div>

<!-- ══════════════════════ PROJECTS (POKEDEX) ══════════════════════ -->
<div class="section">
  <div class="section-label">
    <div class="section-label-text">Race Results · Projects</div>
    <div class="section-label-line"></div>
  </div>
  <div class="section-title">Grand Prix Wins</div>
  <div class="section-sub">From the circuit to the codebase — every race is a shipped feature</div>

  <div class="pokedex-grid">

    <div class="project-card" style="--pc:#0600EF">
      <div class="project-num">
        <div class="project-num-text">P1</div>
        <div class="project-num-sub">Bahrain GP</div>
      </div>
      <div class="project-body">
        <div class="project-type">🌱 Grass Type · Full Stack</div>
        <div class="project-title">Project One</div>
        <div class="project-desc">Short description of what it does and the problem it solves — a full-stack application built with performance and scalability in mind.</div>
        <div class="project-tech" style="display:flex;gap:6px;flex-wrap:wrap;margin-bottom:12px">
          <span class="tech-pill">React</span><span class="tech-pill">Node.js</span><span class="tech-pill">PostgreSQL</span>
        </div>
        <div class="project-links">
          <a href="#">Live Demo</a>
          <a href="#">Repo</a>
        </div>
      </div>
    </div>

    <div class="project-card" style="--pc:#DC0000">
      <div class="project-num" style="background:#DC0000">
        <div class="project-num-text">P2</div>
        <div class="project-num-sub">Monaco GP</div>
      </div>
      <div class="project-body">
        <div class="project-type">🔥 Fire Type · Frontend</div>
        <div class="project-title">Project Two</div>
        <div class="project-desc">Short description of what it does and the problem it solves — crafted with bleeding-edge Next.js features and seamless UX.</div>
        <div class="project-tech" style="display:flex;gap:6px;flex-wrap:wrap;margin-bottom:12px">
          <span class="tech-pill">Next.js</span><span class="tech-pill">Tailwind</span><span class="tech-pill">Prisma</span>
        </div>
        <div class="project-links">
          <a href="#" style="--pc:#DC0000">Live Demo</a>
          <a href="#">Repo</a>
        </div>
      </div>
    </div>

    <div class="project-card" style="--pc:#00D2BE">
      <div class="project-num" style="background:#00D2BE">
        <div class="project-num-text">P3</div>
        <div class="project-num-sub">Silverstone GP</div>
      </div>
      <div class="project-body">
        <div class="project-type">💧 Water Type · Backend</div>
        <div class="project-title">Project Three</div>
        <div class="project-desc">Short description of what it does and the problem it solves — a cloud-native API built on Python FastAPI with AWS infrastructure.</div>
        <div class="project-tech" style="display:flex;gap:6px;flex-wrap:wrap;margin-bottom:12px">
          <span class="tech-pill">Python</span><span class="tech-pill">FastAPI</span><span class="tech-pill">AWS</span>
        </div>
        <div class="project-links">
          <a href="#">Live Demo</a>
          <a href="#">Repo</a>
        </div>
      </div>
    </div>

    <div class="project-card" style="--pc:#FF8000">
      <div class="project-num" style="background:#FF8000">
        <div class="project-num-text">P4</div>
        <div class="project-num-sub">Monza GP</div>
      </div>
      <div class="project-body">
        <div class="project-type">⚡ Electric Type · UI/UX</div>
        <div class="project-title">Project Four</div>
        <div class="project-desc">Short description of what it does and the problem it solves — a polished Figma-designed product shipped to Vercel at full throttle.</div>
        <div class="project-tech" style="display:flex;gap:6px;flex-wrap:wrap;margin-bottom:12px">
          <span class="tech-pill">TypeScript</span><span class="tech-pill">Figma</span><span class="tech-pill">Vercel</span>
        </div>
        <div class="project-links">
          <a href="#">Live Demo</a>
          <a href="#">Repo</a>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- ══════════════════════ BATTLE RECORD (GITHUB STATS) ══════════════════════ -->
<div class="section">
  <div class="section-label">
    <div class="section-label-text">Battle Record · GitHub Stats</div>
    <div class="section-label-line"></div>
  </div>
  <div class="section-title">Season Statistics</div>
  <div class="section-sub">Telemetry data from the pit wall — every commit counts</div>

  <div class="stats-grid">
    <div class="stat-card">
      <div class="stat-label">Total Commits</div>
      <div class="stat-value">1,247</div>
      <div class="stat-sub">+142 this season</div>
    </div>
    <div class="stat-card">
      <div class="stat-label">Pull Requests</div>
      <div class="stat-value">384</div>
      <div class="stat-sub">96% merge rate</div>
    </div>
    <div class="stat-card">
      <div class="stat-label">Issues Closed</div>
      <div class="stat-value">512</div>
      <div class="stat-sub">avg 1.4 days</div>
    </div>
    <div class="stat-card">
      <div class="stat-label">Repos</div>
      <div class="stat-value">48</div>
      <div class="stat-sub">12 public</div>
    </div>
  </div>

  <!-- Language Bar -->
  <div class="lang-bar-wrap">
    <div class="lang-bar-track">
      <div class="lang-seg" style="flex:38;background:#61DAFB"></div>
      <div class="lang-seg" style="flex:22;background:#FFD43B"></div>
      <div class="lang-seg" style="flex:18;background:#3178C6"></div>
      <div class="lang-seg" style="flex:12;background:#F24E1E"></div>
      <div class="lang-seg" style="flex:10;background:#4DB33D"></div>
    </div>
    <div class="lang-legend">
      <div class="lang-item"><span class="lang-dot" style="background:#61DAFB"></span>JavaScript / JSX 38%</div>
      <div class="lang-item"><span class="lang-dot" style="background:#FFD43B"></span>Python 22%</div>
      <div class="lang-item"><span class="lang-dot" style="background:#3178C6"></span>TypeScript 18%</div>
      <div class="lang-item"><span class="lang-dot" style="background:#F24E1E"></span>CSS / HTML 12%</div>
      <div class="lang-item"><span class="lang-dot" style="background:#4DB33D"></span>Other 10%</div>
    </div>
  </div>

  <!-- Streak -->
  <div class="streak-bar">
    <div class="streak-label">Commit Streak — Current: 47 days 🔥</div>
    <div class="streak-row" id="streakDots"></div>
  </div>

  <!-- Activity Grid -->
  <div class="activity-track">
    <div class="streak-label" style="margin-bottom:8px">Wild Encounters — Contribution Map</div>
    <div class="month-labels" id="monthLabels"></div>
    <div class="activity-grid" id="activityGrid"></div>
  </div>
</div>

<!-- ══════════════════════ TROPHIES (GYM BADGES) ══════════════════════ -->
<div class="section">
  <div class="section-label">
    <div class="section-label-text">Gym Badges · Trophies</div>
    <div class="section-label-line"></div>
  </div>
  <div class="section-title">Championship Trophies</div>
  <div class="section-sub">Hardware collected from circuits around the world</div>

  <div class="trophy-row">
    <div class="trophy">
      <div class="trophy-icon" style="color:#FFD700">🏆</div>
      <div class="trophy-count" style="color:#FFD700">7</div>
      <div class="trophy-name">Multi Star</div>
    </div>
    <div class="trophy">
      <div class="trophy-icon" style="color:#C0C0C0">⭐</div>
      <div class="trophy-count">3</div>
      <div class="trophy-name">Long Streak</div>
    </div>
    <div class="trophy">
      <div class="trophy-icon" style="color:#E8002D">🔴</div>
      <div class="trophy-count">12</div>
      <div class="trophy-name">Commits</div>
    </div>
    <div class="trophy">
      <div class="trophy-icon" style="color:#FF8000">🏅</div>
      <div class="trophy-count">48</div>
      <div class="trophy-name">Repos</div>
    </div>
    <div class="trophy">
      <div class="trophy-icon" style="color:#00D2BE">⚡</div>
      <div class="trophy-count">2</div>
      <div class="trophy-name">Ancient</div>
    </div>
    <div class="trophy">
      <div class="trophy-icon" style="color:#9B59B6">👾</div>
      <div class="trophy-count">1</div>
      <div class="trophy-name">All‑In</div>
    </div>
    <div class="trophy">
      <div class="trophy-icon" style="color:#CD7F32">🔥</div>
      <div class="trophy-count">5</div>
      <div class="trophy-name">Joined</div>
    </div>
  </div>
</div>

<!-- ══════════════════════ CONNECT ══════════════════════ -->
<div class="section">
  <div class="section-label">
    <div class="section-label-text">Trainer Links · Connect</div>
    <div class="section-label-line"></div>
  </div>
  <div class="section-title">Pit Lane Contacts</div>
  <div class="section-sub">Come on in — the radio is open</div>

  <div class="connect-grid">
    <a class="connect-card" href="https://github.com/gokulan">
      <div class="connect-icon" style="background:#24292e">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="#fff"><path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/></svg>
      </div>
      <div>
        <div class="connect-name">GitHub</div>
        <div class="connect-handle">@gokulan</div>
      </div>
    </a>

    <a class="connect-card" href="https://linkedin.com/in/gokulan">
      <div class="connect-icon" style="background:#0077B5">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="#fff"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 01-2.063-2.065 2.064 2.064 0 112.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
      </div>
      <div>
        <div class="connect-name">LinkedIn</div>
        <div class="connect-handle">Gokulan Anbalagan</div>
      </div>
    </a>

    <a class="connect-card" href="https://instagram.com/voltmedia.in">
      <div class="connect-icon" style="background:radial-gradient(circle at 30% 107%,#fdf497 0%,#fd5949 45%,#d6249f 60%,#285AEB 90%)">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="#fff"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"/></svg>
      </div>
      <div>
        <div class="connect-name">Instagram</div>
        <div class="connect-handle">@voltmedia.in</div>
      </div>
    </a>

    <a class="connect-card" href="mailto:gokulan.rkivln@gmail.com">
      <div class="connect-icon" style="background:#EA4335">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="#fff"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 010 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
      </div>
      <div>
        <div class="connect-name">Email</div>
        <div class="connect-handle">gokulan.rkivln@gmail.com</div>
      </div>
    </a>
  </div>
</div>

<!-- ══════════════════════ FOOTER ══════════════════════ -->
<div class="footer">
  <div class="footer-logo">F1</div>
  <div class="footer-text">Gotta Build 'Em All</div>
  <div class="footer-sub" style="margin-top:12px;color:var(--f1-muted);font-family:var(--font-mono);font-size:13px">
    TRAINERS VISITED &nbsp; <strong style="color:var(--f1-red)">1,247</strong> &nbsp;·&nbsp; SEASON 2025
  </div>

  <!-- Evolution line of mini F1 cars -->
  <div style="display:flex;justify-content:center;gap:12px;margin-top:24px;flex-wrap:wrap">
    <!-- Mini cars SVG row -->
    <svg viewBox="0 0 600 60" width="600" style="max-width:100%" xmlns="http://www.w3.org/2000/svg">
      <!-- Car 1 - Red Bull blue -->
      <g transform="translate(10,8) scale(0.55)">
        <ellipse cx="90" cy="58" rx="80" ry="5" fill="rgba(0,0,0,0.3)"/>
        <path d="M20 35 Q30 28 80 26 L160 26 Q170 28 175 35 L175 50 Q170 55 160 53 L80 53 Q30 55 20 50 Z" fill="#0600EF"/>
        <path d="M160 35 L185 32 L188 40 L185 48 L160 44 Z" fill="#1a00aa"/>
        <circle cx="45" cy="55" r="10" fill="#222" stroke="#444" stroke-width="1"/>
        <circle cx="170" cy="55" r="8" fill="#222" stroke="#444" stroke-width="1"/>
        <text x="95" y="44" font-family="Barlow Condensed,sans-serif" font-size="12" font-weight="900" fill="white">RB</text>
      </g>
      <!-- Car 2 - Ferrari red -->
      <g transform="translate(115,8) scale(0.55)">
        <ellipse cx="90" cy="58" rx="80" ry="5" fill="rgba(0,0,0,0.3)"/>
        <path d="M20 35 Q30 28 80 26 L160 26 Q170 28 175 35 L175 50 Q170 55 160 53 L80 53 Q30 55 20 50 Z" fill="#DC0000"/>
        <path d="M160 35 L185 32 L188 40 L185 48 L160 44 Z" fill="#aa0000"/>
        <circle cx="45" cy="55" r="10" fill="#222" stroke="#444" stroke-width="1"/>
        <circle cx="170" cy="55" r="8" fill="#222" stroke="#444" stroke-width="1"/>
        <text x="95" y="44" font-family="Barlow Condensed,sans-serif" font-size="12" font-weight="900" fill="white">SF</text>
      </g>
      <!-- Car 3 - Mercedes silver -->
      <g transform="translate(220,8) scale(0.55)">
        <ellipse cx="90" cy="58" rx="80" ry="5" fill="rgba(0,0,0,0.3)"/>
        <path d="M20 35 Q30 28 80 26 L160 26 Q170 28 175 35 L175 50 Q170 55 160 53 L80 53 Q30 55 20 50 Z" fill="#00D2BE"/>
        <path d="M160 35 L185 32 L188 40 L185 48 L160 44 Z" fill="#00a090"/>
        <circle cx="45" cy="55" r="10" fill="#222" stroke="#444" stroke-width="1"/>
        <circle cx="170" cy="55" r="8" fill="#222" stroke="#444" stroke-width="1"/>
        <text x="95" y="44" font-family="Barlow Condensed,sans-serif" font-size="12" font-weight="900" fill="white">AMG</text>
      </g>
      <!-- Car 4 - McLaren orange -->
      <g transform="translate(325,8) scale(0.55)">
        <ellipse cx="90" cy="58" rx="80" ry="5" fill="rgba(0,0,0,0.3)"/>
        <path d="M20 35 Q30 28 80 26 L160 26 Q170 28 175 35 L175 50 Q170 55 160 53 L80 53 Q30 55 20 50 Z" fill="#FF8000"/>
        <path d="M160 35 L185 32 L188 40 L185 48 L160 44 Z" fill="#cc6600"/>
        <circle cx="45" cy="55" r="10" fill="#222" stroke="#444" stroke-width="1"/>
        <circle cx="170" cy="55" r="8" fill="#222" stroke="#444" stroke-width="1"/>
        <text x="95" y="44" font-family="Barlow Condensed,sans-serif" font-size="12" font-weight="900" fill="white">MCL</text>
      </g>
      <!-- Car 5 - Alpine blue -->
      <g transform="translate(430,8) scale(0.55)">
        <ellipse cx="90" cy="58" rx="80" ry="5" fill="rgba(0,0,0,0.3)"/>
        <path d="M20 35 Q30 28 80 26 L160 26 Q170 28 175 35 L175 50 Q170 55 160 53 L80 53 Q30 55 20 50 Z" fill="#0090FF"/>
        <path d="M160 35 L185 32 L188 40 L185 48 L160 44 Z" fill="#0070cc"/>
        <circle cx="45" cy="55" r="10" fill="#222" stroke="#444" stroke-width="1"/>
        <circle cx="170" cy="55" r="8" fill="#222" stroke="#444" stroke-width="1"/>
        <text x="95" y="44" font-family="Barlow Condensed,sans-serif" font-size="12" font-weight="900" fill="white">ALP</text>
      </g>
    </svg>
  </div>

  <div style="font-family:var(--font-mono);font-size:10px;color:var(--f1-border);margin-top:24px;letter-spacing:2px">
    LIGHTS OUT AND AWAY WE GO · GOKULAN ANBALAGAN © 2025
  </div>
</div>

<script>
// Generate streak dots
const streakEl = document.getElementById('streakDots');
const levels = ['','cool','warm','hot','hot','hot'];
for(let i=0;i<84;i++){
  const d = document.createElement('div');
  d.className='streak-dot';
  const streak = i>36 ? levels[Math.floor(Math.random()*5)+1] : (Math.random()>0.4 ? levels[Math.floor(Math.random()*3)+1] : '');
  if(streak) d.classList.add(streak);
  streakEl.appendChild(d);
}

// Generate activity grid
const gridEl = document.getElementById('activityGrid');
const months=['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
const monthLabelsEl = document.getElementById('monthLabels');

for(let m=0;m<6;m++){
  const sp=document.createElement('span');
  sp.className='month-label';
  sp.textContent=months[m+6];
  sp.style.flex='1';
  monthLabelsEl.appendChild(sp);
}

for(let w=0;w<26;w++){
  const week=document.createElement('div');
  week.className='activity-week';
  for(let d=0;d<7;d++){
    const cell=document.createElement('div');
    cell.className='activity-cell';
    const r=Math.random();
    if(r>0.85) cell.classList.add('lvl4');
    else if(r>0.65) cell.classList.add('lvl3');
    else if(r>0.45) cell.classList.add('lvl2');
    else if(r>0.3) cell.classList.add('lvl1');
    week.appendChild(cell);
  }
  gridEl.appendChild(week);
}
</script>
</body>
</html>
