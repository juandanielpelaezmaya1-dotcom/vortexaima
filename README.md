
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vortex Aima — Agencia de Marketing e Inteligencia Artificial</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box}
:root{--navy:#060834;--blue:#305aa3;--silver:#d4d5d5;--white:#fff;--off:#f4f5f8;--muted:#8a90a8;--border:#e2e4eb;--font-d:'Bebas Neue',sans-serif;--font-b:'Inter',sans-serif}
body{background:var(--off);color:var(--navy);font-family:var(--font-b);overflow-x:hidden}
nav{position:fixed;top:0;left:0;right:0;z-index:100;display:flex;align-items:center;justify-content:space-between;padding:1rem 2.5rem;background:var(--navy);border-bottom:1px solid rgba(255,255,255,0.08)}
.nav-logo{display:flex;align-items:center;gap:0.6rem}
.nav-logo-mark{width:26px;height:26px;background:var(--blue);display:flex;align-items:center;justify-content:center;font-family:var(--font-d);font-size:0.9rem;color:var(--white)}
.nav-logo-text{font-family:var(--font-d);font-size:1.2rem;letter-spacing:0.08em;color:var(--white)}
.nav-logo-text span{color:var(--silver)}
.nav-links{display:flex;gap:0.3rem}
.nav-links button{background:none;border:none;color:rgba(255,255,255,0.6);font-family:var(--font-b);font-size:0.78rem;cursor:pointer;padding:0.45rem 0.9rem;letter-spacing:0.06em;text-transform:uppercase;transition:all 0.2s;border-radius:3px}
.nav-links button:hover,.nav-links button.active{color:var(--white);background:rgba(48,90,163,0.35)}
.nav-cta{background:var(--blue);color:var(--white);border:none;font-family:var(--font-b);font-weight:600;font-size:0.78rem;padding:0.5rem 1.2rem;cursor:pointer;letter-spacing:0.06em;text-transform:uppercase;border-radius:3px;transition:opacity 0.2s}
.nav-cta:hover{opacity:0.85}
.page{display:none;min-height:100vh;padding-top:4.2rem}
.page.active{display:block;animation:fadeUp 0.3s ease}
@keyframes fadeUp{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:translateY(0)}}

/* HERO */
.hero{background:var(--navy);padding:4.5rem 2.5rem 3.5rem;position:relative;overflow:hidden}
.hero::before{content:'';position:absolute;width:500px;height:500px;border-radius:50%;background:radial-gradient(circle,rgba(48,90,163,0.22) 0%,transparent 70%);top:-120px;right:-80px;pointer-events:none}
.hero-badge{display:inline-flex;align-items:center;gap:0.5rem;background:rgba(48,90,163,0.2);border:1px solid rgba(48,90,163,0.45);color:var(--silver);font-size:0.68rem;font-weight:600;letter-spacing:0.14em;text-transform:uppercase;padding:0.35rem 0.9rem;border-radius:2px;margin-bottom:1.6rem}
.badge-dot{width:6px;height:6px;border-radius:50%;background:#4ade80;animation:pulse 2s infinite}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:0.3}}
.hero h1{font-family:var(--font-d);font-size:clamp(3rem,6vw,5rem);line-height:0.92;color:var(--white);margin-bottom:1.3rem}
.hero h1 .sl{color:var(--silver)}
.hero h1 .bl{color:#5b8de8}
.hero-sub{color:rgba(212,213,213,0.72);font-size:0.95rem;line-height:1.75;max-width:540px;margin-bottom:2.2rem;font-weight:300}
.hero-sub strong{color:var(--silver);font-weight:600}
.hero-actions{display:flex;gap:0.8rem;flex-wrap:wrap;margin-bottom:3rem}
.btn-p{background:var(--blue);color:var(--white);border:none;font-family:var(--font-b);font-weight:600;font-size:0.82rem;padding:0.8rem 1.7rem;cursor:pointer;letter-spacing:0.06em;text-transform:uppercase;border-radius:3px;transition:all 0.2s}
.btn-p:hover{background:#3d6fc0;transform:translateY(-1px)}
.btn-o{background:transparent;border:1px solid rgba(212,213,213,0.25);color:var(--silver);font-family:var(--font-b);font-size:0.82rem;padding:0.8rem 1.7rem;cursor:pointer;letter-spacing:0.06em;text-transform:uppercase;border-radius:3px;transition:all 0.2s}
.btn-o:hover{border-color:var(--silver);color:var(--white)}
.stats-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:rgba(255,255,255,0.08);border:1px solid rgba(255,255,255,0.08)}
.stat-b{background:var(--navy);padding:1.3rem;text-align:center}
.stat-n{font-family:var(--font-d);font-size:2rem;color:var(--white);line-height:1}
.stat-n span{color:#5b8de8}
.stat-l{color:var(--muted);font-size:0.65rem;letter-spacing:0.1em;text-transform:uppercase;margin-top:0.25rem}

/* BANNER GRATIS */
.free-banner{background:linear-gradient(135deg,#1a2a6e 0%,var(--blue) 100%);border:1px solid rgba(91,141,232,0.4);padding:1.8rem 2.5rem;display:flex;align-items:center;justify-content:space-between;gap:2rem}
.free-banner-left{display:flex;align-items:center;gap:1.2rem}
.free-icon{width:52px;height:52px;background:rgba(255,255,255,0.12);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1.5rem;flex-shrink:0}
.free-banner h3{font-family:var(--font-d);font-size:1.4rem;color:var(--white);line-height:1;margin-bottom:0.25rem}
.free-banner p{color:rgba(255,255,255,0.7);font-size:0.78rem;line-height:1.5}
.free-banner p strong{color:var(--white)}
.badge-free{display:inline-block;background:#4ade80;color:#052e16;font-size:0.62rem;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;padding:0.25rem 0.7rem;border-radius:2px;margin-bottom:0.4rem}
.btn-free{background:var(--white);color:var(--blue);border:none;font-family:var(--font-b);font-weight:700;font-size:0.8rem;padding:0.75rem 1.5rem;cursor:pointer;letter-spacing:0.06em;text-transform:uppercase;border-radius:3px;white-space:nowrap;transition:all 0.2s;flex-shrink:0}
.btn-free:hover{background:var(--silver)}

/* SECTIONS */
.section{padding:3.5rem 2.5rem}
.section.white{background:var(--white)}
.section.navy{background:var(--navy)}
.section.off{background:var(--off)}
.s-eye{font-size:0.65rem;font-weight:700;letter-spacing:0.2em;text-transform:uppercase;color:var(--blue);margin-bottom:0.5rem}
.s-eye.light{color:var(--silver)}
.s-h2{font-family:var(--font-d);font-size:clamp(1.8rem,3.5vw,2.8rem);color:var(--navy);line-height:1.02;margin-bottom:0.7rem}
.s-h2.light{color:var(--white)}
.s-sub{color:var(--muted);font-size:0.88rem;line-height:1.7;max-width:520px}
.val-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:1rem;margin-top:2rem}
.val-c{background:var(--off);border:1px solid var(--border);border-left:3px solid var(--blue);padding:1.5rem;border-radius:4px;transition:all 0.2s}
.val-c:hover{transform:translateY(-2px);border-color:var(--blue)}
.val-icon{font-size:1.4rem;margin-bottom:0.6rem}
.val-title{font-weight:700;font-size:0.88rem;color:var(--navy);margin-bottom:0.3rem}
.val-desc{color:var(--muted);font-size:0.78rem;line-height:1.6}
.diff-wrap{display:grid;grid-template-columns:1fr 1fr;gap:3rem;align-items:start}
.diff-quote{background:rgba(48,90,163,0.15);border:1px solid rgba(48,90,163,0.3);border-left:3px solid var(--blue);padding:1.2rem 1.4rem;border-radius:3px;margin:1.2rem 0}
.diff-quote p{color:rgba(212,213,213,0.85);font-size:0.85rem;line-height:1.7;font-style:italic}
.diff-list{display:flex;flex-direction:column;gap:1px;background:rgba(255,255,255,0.07);margin-top:0.5rem}
.diff-i{background:var(--navy);padding:1.1rem 1.3rem;border-left:2px solid transparent;transition:border-color 0.2s}
.diff-i:hover{border-left-color:var(--blue)}
.diff-i-t{font-weight:600;font-size:0.85rem;color:var(--white);margin-bottom:0.2rem}
.diff-i-d{font-size:0.76rem;color:rgba(212,213,213,0.5);line-height:1.5}
.team-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1rem;margin-top:2rem}
.team-c{background:var(--white);border:1px solid var(--border);padding:1.4rem 1rem;text-align:center;border-radius:6px;transition:all 0.2s}
.team-c:hover{border-color:var(--blue);transform:translateY(-2px)}
.team-av{width:52px;height:52px;border-radius:50%;background:var(--navy);border:2px solid var(--blue);display:flex;align-items:center;justify-content:center;font-family:var(--font-d);font-size:1.2rem;color:var(--white);margin:0 auto 0.8rem}
.team-name{font-weight:700;font-size:0.85rem;color:var(--navy)}
.team-role{color:var(--blue);font-size:0.68rem;letter-spacing:0.07em;text-transform:uppercase;font-weight:600;margin-top:0.15rem}
.cta-strip{background:var(--blue);padding:2.8rem 2.5rem;display:flex;align-items:center;justify-content:space-between;gap:2rem}
.cta-strip h2{font-family:var(--font-d);font-size:1.9rem;color:var(--white);line-height:1.05}
.cta-strip p{color:rgba(255,255,255,0.7);font-size:0.82rem;margin-top:0.3rem}
.btn-w{background:var(--white);color:var(--blue);border:none;font-family:var(--font-b);font-weight:700;font-size:0.82rem;padding:0.8rem 1.7rem;cursor:pointer;letter-spacing:0.06em;text-transform:uppercase;border-radius:3px;white-space:nowrap;transition:all 0.2s}
.btn-w:hover{background:var(--silver)}

/* BLOG */
.blog-head{background:var(--navy);padding:4rem 2.5rem 2.5rem}
.blog-cats{display:flex;gap:0.4rem;flex-wrap:wrap;margin-bottom:1rem}
.bcat{font-size:0.65rem;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;padding:0.28rem 0.7rem;border-radius:2px}
.bcat.p{background:var(--blue);color:var(--white)}
.bcat.s{background:rgba(212,213,213,0.1);color:var(--silver);border:1px solid rgba(212,213,213,0.15)}
.blog-head h1{font-family:var(--font-d);font-size:clamp(2rem,4.5vw,3.2rem);color:var(--white);line-height:0.94;max-width:760px;margin-bottom:1rem}
.blog-meta{display:flex;gap:1.5rem;color:rgba(212,213,213,0.45);font-size:0.72rem;letter-spacing:0.06em;text-transform:uppercase}
.blog-layout{display:grid;grid-template-columns:1fr 290px;gap:2.5rem;padding:2.5rem;background:var(--off)}
article{background:var(--white);border:1px solid var(--border);border-radius:6px;padding:2rem}
article h2{font-family:var(--font-d);font-size:1.6rem;color:var(--navy);margin:1.8rem 0 0.6rem}
article p{color:#4a5270;font-size:0.88rem;line-height:1.8;margin-bottom:0.8rem}
article strong{color:var(--navy)}
.art-intro{font-size:0.95rem;color:var(--navy);line-height:1.75;border-left:3px solid var(--blue);padding-left:1rem;margin-bottom:1.5rem}
.hl-box{background:var(--off);border:1px solid var(--border);border-radius:4px;padding:1.1rem 1.3rem;margin:1.1rem 0}
.hl-box p{margin:0;color:var(--navy);font-size:0.85rem}
.poem-grid{display:grid;grid-template-columns:1fr 1fr 1fr;gap:1px;background:var(--border);border:1px solid var(--border);border-radius:4px;overflow:hidden;margin:1.1rem 0}
.poem-col{background:var(--white);padding:1rem}
.poem-head{font-size:0.65rem;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;margin-bottom:0.6rem;padding-bottom:0.4rem;border-bottom:2px solid}
.poem-col.paid .poem-head{color:#e05c2a;border-color:#e05c2a}
.poem-col.owned .poem-head{color:var(--blue);border-color:var(--blue)}
.poem-col.earned .poem-head{color:#0e9f6e;border-color:#0e9f6e}
.poem-col li{font-size:0.76rem;color:#5a6180;padding:0.18rem 0;list-style:none;border-bottom:1px solid var(--border)}
.poem-col li:last-child{border:none}
.traf-list{display:flex;flex-direction:column;gap:0.6rem;margin:1rem 0}
.traf-i{padding:0.9rem 1rem;border-radius:4px;border:1px solid var(--border)}
.traf-i.cold{border-left:3px solid #378add}
.traf-i.warm{border-left:3px solid #f59e0b}
.traf-i.hot{border-left:3px solid #ef4444}
.traf-l{font-size:0.8rem;font-weight:700;color:var(--navy);margin-bottom:0.2rem}
.traf-d{font-size:0.76rem;color:var(--muted);line-height:1.5}
.art-cta{background:var(--navy);border-radius:4px;padding:1.5rem;text-align:center;margin-top:1.5rem}
.art-cta p{color:var(--silver);font-size:0.85rem;margin-bottom:0.8rem}
aside{display:flex;flex-direction:column;gap:1rem;position:sticky;top:5.5rem}
.sb-card{background:var(--white);border:1px solid var(--border);border-radius:6px;padding:1.1rem}
.sb-card h4{font-size:0.65rem;font-weight:700;letter-spacing:0.12em;text-transform:uppercase;color:var(--blue);margin-bottom:0.8rem;padding-bottom:0.4rem;border-bottom:1px solid var(--border)}
.sb-card p{font-size:0.8rem;color:var(--muted);line-height:1.6}
.sb-tag{font-size:0.65rem;font-weight:600;padding:0.2rem 0.5rem;background:var(--off);border:1px solid var(--border);color:var(--navy);border-radius:2px;display:inline-block;margin:0.15rem}

/* CONTACTO */
.ticker{background:var(--blue);padding:0.55rem 2.5rem;font-size:0.72rem;color:var(--white);letter-spacing:0.07em;font-weight:600}
.contact-head{background:var(--navy);padding:3.5rem 2.5rem 2.5rem}
.contact-head h1{font-family:var(--font-d);font-size:clamp(2.8rem,5.5vw,4.2rem);color:var(--white);line-height:0.92;margin-bottom:0.8rem}
.contact-head h1 em{color:var(--silver);font-style:normal}
.contact-head p{color:rgba(212,213,213,0.65);font-size:0.88rem;line-height:1.7;max-width:500px}
.free-offer{background:rgba(74,222,128,0.08);border:1px solid rgba(74,222,128,0.3);border-radius:4px;padding:1.2rem 1.4rem;margin-top:1.2rem;display:flex;align-items:center;gap:1rem}
.free-offer-icon{font-size:1.8rem;flex-shrink:0}
.free-offer h4{font-weight:700;font-size:0.9rem;color:#4ade80;margin-bottom:0.2rem}
.free-offer p{font-size:0.78rem;color:rgba(212,213,213,0.7);line-height:1.5}
.contact-body{display:grid;grid-template-columns:1fr 1fr;gap:2rem;padding:2.5rem;background:var(--off);align-items:start}
.svc-list{background:var(--white);border:1px solid var(--border);border-radius:6px;overflow:hidden}
.svc-i{display:flex;align-items:flex-start;gap:0.9rem;padding:1.1rem 1.3rem;border-bottom:1px solid var(--border);transition:background 0.15s}
.svc-i:hover{background:var(--off)}
.svc-i:last-child{border:none}
.svc-num{font-family:var(--font-d);font-size:1.5rem;color:var(--blue);line-height:1;min-width:30px}
.svc-t{font-weight:700;font-size:0.85rem;color:var(--navy);margin-bottom:0.2rem}
.svc-d{font-size:0.75rem;color:var(--muted);line-height:1.5}
.cb-section-label{font-size:0.65rem;font-weight:700;letter-spacing:0.15em;text-transform:uppercase;color:var(--blue);margin-bottom:0.6rem}
.cb-free-teaser{background:rgba(48,90,163,0.08);border:1px solid rgba(48,90,163,0.25);border-radius:4px;padding:0.9rem 1rem;margin-bottom:0.8rem;display:flex;align-items:center;gap:0.8rem}
.cb-free-teaser span{font-size:1.2rem}
.cb-free-teaser p{font-size:0.78rem;color:var(--navy);line-height:1.4}
.cb-free-teaser p strong{color:var(--blue)}
.cb-wrap{background:var(--white);border:1px solid var(--border);border-radius:6px;overflow:hidden;display:flex;flex-direction:column;height:460px}
.cb-h{background:var(--navy);padding:0.9rem 1.1rem;display:flex;align-items:center;gap:0.8rem}
.cb-av{width:32px;height:32px;background:var(--blue);display:flex;align-items:center;justify-content:center;font-family:var(--font-d);font-size:0.95rem;color:var(--white);border-radius:3px;flex-shrink:0}
.cb-name{font-weight:700;font-size:0.85rem;color:var(--white)}
.cb-status{font-size:0.65rem;color:#4ade80;letter-spacing:0.05em;text-transform:uppercase;margin-top:1px}
.cb-msgs{flex:1;overflow-y:auto;padding:0.9rem;display:flex;flex-direction:column;gap:0.65rem;background:var(--off)}
.msg{max-width:84%;padding:0.65rem 0.9rem;font-size:0.82rem;line-height:1.5;border-radius:4px}
.msg.bot{background:var(--white);border:1px solid var(--border);align-self:flex-start;color:var(--navy)}
.msg.user{background:var(--blue);color:var(--white);align-self:flex-end}
.cb-opts{display:flex;flex-direction:column;gap:0.3rem;align-self:flex-start;max-width:90%}
.cb-opt{background:var(--white);border:1px solid var(--blue);color:var(--blue);font-family:var(--font-b);font-size:0.75rem;font-weight:600;padding:0.38rem 0.8rem;cursor:pointer;border-radius:3px;text-align:left;transition:all 0.15s}
.cb-opt:hover{background:var(--blue);color:var(--white)}
.cb-ir{display:flex;gap:0.5rem;padding:0.7rem;border-top:1px solid var(--border);background:var(--white)}
.cb-ir input{flex:1;background:var(--off);border:1px solid var(--border);color:var(--navy);font-family:var(--font-b);font-size:0.82rem;padding:0.55rem 0.8rem;border-radius:3px;outline:none}
.cb-ir input:focus{border-color:var(--blue)}
.cb-send{background:var(--blue);border:none;color:var(--white);font-weight:700;font-size:0.75rem;padding:0.55rem 0.9rem;cursor:pointer;border-radius:3px;letter-spacing:0.04em;text-transform:uppercase}
footer{background:var(--navy);padding:1.8rem 2.5rem;display:flex;align-items:center;justify-content:space-between;border-top:1px solid rgba(255,255,255,0.06)}
.foot-logo{font-family:var(--font-d);font-size:1.1rem;color:var(--white);letter-spacing:0.06em}
.foot-logo span{color:var(--silver)}
footer p{color:rgba(212,213,213,0.3);font-size:0.72rem}
@media(max-width:768px){
  nav{padding:0.8rem 1rem}
  .nav-logo-text{font-size:1rem}
  .nav-links button{font-size:0.65rem;padding:0.35rem 0.6rem}
  .nav-cta{font-size:0.65rem;padding:0.4rem 0.8rem}
  .hero{padding:2.5rem 1rem 2rem}
  .hero h1{font-size:2.4rem}
  .stats-grid{grid-template-columns:1fr 1fr}
  .free-banner{flex-direction:column;padding:1.5rem 1rem}
  .section{padding:2rem 1rem}
  .val-grid{grid-template-columns:1fr}
  .diff-wrap{grid-template-columns:1fr}
  .team-grid{grid-template-columns:1fr 1fr}
  .cta-strip{flex-direction:column;text-align:center;padding:2rem 1rem}
  .blog-layout{grid-template-columns:1fr;padding:1.2rem}
  .blog-head{padding:2.5rem 1rem 1.5rem}
  .contact-body{grid-template-columns:1fr;padding:1.2rem}
  .contact-head{padding:2.5rem 1rem 1.5rem}
  .ticker{padding:0.5rem 1rem}
  footer{flex-direction:column;gap:0.5rem;text-align:center;padding:1.2rem}
}
</style>
</head>
<body>

<nav>
  <div class="nav-logo">
    <div class="nav-logo-mark">V</div>
    <div class="nav-logo-text">VORTEX <span>AIMA</span></div>
  </div>
  <div class="nav-links">
    <button class="active" onclick="showPage('landing',this)">Inicio</button>
    <button onclick="showPage('blog',this)">Blog</button>
    <button onclick="showPage('contacto',this)">Contacto</button>
  </div>
  <button class="nav-cta" onclick="showPage('contacto',null)">Consultoría Gratis →</button>
</nav>

<!-- PAGE 1: LANDING -->
<div class="page active" id="landing">
  <div class="hero">
    <div class="hero-badge"><span class="badge-dot"></span>Agencia de Marketing e Inteligencia Artificial — Pasto</div>
    <h1>EL EQUIPO DE <span class="sl">MARKETING</span> E <span class="bl">INTELIGENCIA ARTIFICIAL</span> QUE TU NEGOCIO NECESITA.</h1>
    <p class="hero-sub">Crece <strong>sin depender de que el dueño esté pendiente de todo.</strong> Estrategia, automatización con IA y producción de alto impacto para que cada peso trabaje por ti.</p>
    <div class="hero-actions">
      <button class="btn-p" onclick="showPage('blog',null)">Leer nuestro blog →</button>
      <button class="btn-o" onclick="showPage('contacto',null)">Ver servicios</button>
    </div>
    <div class="stats-grid">
      <div class="stat-b"><div class="stat-n"><span>6</span>X</div><div class="stat-l">ROI promedio</div></div>
      <div class="stat-b"><div class="stat-n">IA<span>+</span></div><div class="stat-l">Marketing integrado</div></div>
      <div class="stat-b"><div class="stat-n"><span>24</span>/7</div><div class="stat-l">Automatización activa</div></div>
      <div class="stat-b"><div class="stat-n">Gen<span>Z</span></div><div class="stat-l">Audiencia objetivo</div></div>
    </div>
  </div>

  <div class="free-banner">
    <div class="free-banner-left">
      <div class="free-icon">🎁</div>
      <div>
        <div class="badge-free">Por tiempo limitado</div>
        <h3>CONSULTORÍA DIGITAL 100% GRATIS</h3>
        <p>Agenda hoy y recibe <strong>24 horas de asesoría estratégica sin costo.</strong> Analizamos tu negocio y te entregamos un plan de acción real.</p>
      </div>
    </div>
    <button class="btn-free" onclick="showPage('contacto',null)">¡La quiero gratis! →</button>
  </div>

  <div class="section white">
    <div class="s-eye">↳ Nuestra propuesta de valor</div>
    <div class="s-h2">Somos la primera AIMA en la región.</div>
    <p class="s-sub">No solo hacemos marketing. Integramos inteligencia artificial para que tu negocio sea más eficiente, rentable y escalable.</p>
    <div class="val-grid">
      <div class="val-c"><div class="val-icon">🎯</div><div class="val-title">Contenido que convierte</div><div class="val-desc">Video, diseño y copy con estrategia. Cada pieza tiene un objetivo claro dentro del embudo de conversión.</div></div>
      <div class="val-c"><div class="val-icon">🤖</div><div class="val-title">Marketing + Automatización con IA</div><div class="val-desc">Chatbots, flujos automáticos y CRM potenciados con IA. Tu negocio vende mientras duermes.</div></div>
      <div class="val-c"><div class="val-icon">👥</div><div class="val-title">El consumidor como epicentro</div><div class="val-desc">Todo parte del cliente. Entendemos sus comportamientos y motivaciones antes de crear cualquier campaña.</div></div>
      <div class="val-c"><div class="val-icon">📊</div><div class="val-title">Enfocados en resultados</div><div class="val-desc">$200K invertidos → $1.2M en facturación por canal digital. Números reales, no promesas vacías.</div></div>
    </div>
  </div>

  <div class="section navy">
    <div class="diff-wrap">
      <div>
        <div class="s-eye light">↳ Por qué elegirnos</div>
        <div class="s-h2 light">DEJA DE TIRAR TU PRESUPUESTO A LA BASURA.</div>
        <div class="diff-quote"><p>"El error es creer que pautar es solo hundir un botón. En Vortex combinamos experiencia técnica con producción de alta calidad para que cada anuncio sea una herramienta de venta — no un gasto más."</p></div>
      </div>
      <div class="diff-list">
        <div class="diff-i"><div class="diff-i-t">Estrategia antes de ejecución</div><div class="diff-i-d">Analizamos mercado, audiencia y competencia antes de invertir un peso.</div></div>
        <div class="diff-i"><div class="diff-i-t">IA integrada en cada proceso</div><div class="diff-i-d">Automatizamos lo repetitivo para enfocarnos en lo creativo y estratégico.</div></div>
        <div class="diff-i"><div class="diff-i-t">Resultados medibles y trazables</div><div class="diff-i-d">Dashboards en tiempo real. Sabes exactamente qué retorna cada peso invertido.</div></div>
        <div class="diff-i"><div class="diff-i-t">Producción de alto nivel</div><div class="diff-i-d">Video, foto y diseño que detiene el scroll. Especialmente para Gen Z.</div></div>
        <div class="diff-i"><div class="diff-i-t">Acompañamiento continuo</div><div class="diff-i-d">No somos proveedores. Somos parte de tu equipo de crecimiento.</div></div>
      </div>
    </div>
  </div>

  <div class="section off">
    <div class="s-eye">↳ El equipo</div>
    <div class="s-h2">Conoce a Vortex Aima.</div>
    <div class="team-grid">
      <div class="team-c"><div class="team-av">AR</div><div class="team-name">Alejandra Rivera</div><div class="team-role">Estrategia & Branding</div></div>
      <div class="team-c"><div class="team-av">SQ</div><div class="team-name">Sebastian Quiroz</div><div class="team-role">Pauta & Performance</div></div>
      <div class="team-c"><div class="team-av">D</div><div class="team-name">Danilo</div><div class="team-role">Producción de Contenido</div></div>
      <div class="team-c"><div class="team-av">DP</div><div class="team-name">Daniel Peláez</div><div class="team-role">IA & Automatización</div></div>
    </div>
  </div>

  <div class="cta-strip">
    <div>
      <h2>¿LISTO PARA ESCALAR TU NEGOCIO HOY?</h2>
      <p>Agenda tu cita gratis y recibe 24 horas de consultoría estratégica sin costo.</p>
    </div>
    <button class="btn-w" onclick="showPage('contacto',null)">¡Quiero mi consultoría gratis! →</button>
  </div>

  <footer>
    <div class="foot-logo">VORTEX <span>AIMA</span></div>
    <p>© 2025 Vortex Aima · Agencia de Marketing e Inteligencia Artificial · Pasto, Colombia</p>
  </footer>
</div>

<!-- PAGE 2: BLOG -->
<div class="page" id="blog">
  <div class="blog-head">
    <div class="blog-cats">
      <span class="bcat p">Marketing Digital</span>
      <span class="bcat s">Plan de Marketing</span>
      <span class="bcat s">Gen Z</span>
    </div>
    <h1>QUÉ ES UN PLAN DE MARKETING DIGITAL: ESTRATEGIAS Y TÁCTICAS PARA POSICIONAR TU MARCA</h1>
    <div class="blog-meta"><span>✍ Vortex Aima</span><span>📅 2025</span><span>⏱ 8 min de lectura</span></div>
  </div>
  <div class="blog-layout">
    <article>
      <p class="art-intro">Si pagas pauta pero no conviertes, si publicas en redes pero el engagement no llega — lo que te falta no es presupuesto. Te falta un <strong>plan de marketing digital.</strong></p>
      <h2>¿QUÉ ES UN PLAN DE MARKETING DIGITAL?</h2>
      <p>Es el documento estratégico que define hacia dónde va tu marca en el entorno digital y cómo va a llegar ahí. Es la brújula que alinea contenido, pauta, SEO y comunidad hacia un mismo objetivo de negocio.</p>
      <div class="hl-box"><p>💡 Un buen plan responde: ¿Dónde estás ahora? ¿Dónde quieres estar? ¿Cómo vas a llegar?</p></div>
      <h2>MODELO POEM: PAID, OWNED & EARNED</h2>
      <p>Así usamos los medios <strong>Pagados, Propios y Ganados</strong> para llegar a la Gen Z:</p>
      <div class="poem-grid">
        <div class="poem-col paid"><div class="poem-head">Paid Media</div><li>TikTok Ads</li><li>Instagram Ads</li><li>YouTube Pre-roll</li><li>Google Search</li><li>Influencer pagado</li></div>
        <div class="poem-col owned"><div class="poem-head">Owned Media</div><li>Sitio web</li><li>Blog educativo</li><li>Instagram</li><li>Canal TikTok</li><li>Email marketing</li></div>
        <div class="poem-col earned"><div class="poem-head">Earned Media</div><li>Reseñas clientes</li><li>UGC en redes</li><li>Shares orgánicos</li><li>Menciones prensa</li><li>Boca a boca</li></div>
      </div>
      <h2>TEMPERATURAS DEL TRÁFICO</h2>
      <div class="traf-list">
        <div class="traf-i cold"><div class="traf-l">🔵 Tráfico Frío — Captar atención</div><div class="traf-d">No te conocen. TikTok e Instagram Reels para aparecer ante la Gen Z sin interrumpir.</div></div>
        <div class="traf-i warm"><div class="traf-l">🟠 Tráfico Templado — Nutrir confianza</div><div class="traf-d">Ya te siguen. Blog, email y retargeting suave para generar confianza antes de vender.</div></div>
        <div class="traf-i hot"><div class="traf-l">🔴 Tráfico Caliente — Convertir</div><div class="traf-d">Listos para actuar. CTAs directos, chatbot IA y cierres. Aquí brilla la automatización de Vortex Aima.</div></div>
      </div>
      <h2>INBOUND MARKETING PARA GEN Z</h2>
      <p>La Gen Z no ve anuncios: los bloquea. Pero sí consume contenido auténtico y veloz. Por eso construimos embudos que atraen orgánicamente y convierten con inteligencia artificial.</p>
      <div class="hl-box"><p>🚀 Caso Vortex: $200.000 diarios invertidos → $1.200.000 en facturación por canal digital. Embudo bien construido, no pauta al azar.</p></div>
      <h2>BRECHAS GENERACIONALES</h2>
      <p>La <strong>Gen Z (1997–2012)</strong> exige autenticidad, velocidad y propósito. No les vendas — muéstrales resultados reales. En Vortex Aima adaptamos diseño, tono y canal según la generación objetivo.</p>
      <div class="art-cta">
        <p>¿Quieres un plan de marketing con IA para tu marca? Tu primera consultoría es completamente gratis.</p>
        <button class="btn-p" onclick="showPage('contacto',null)">¡Quiero mi consultoría gratis! →</button>
      </div>
    </article>
    <aside>
      <div class="sb-card">
        <h4>Generación objetivo</h4>
        <p style="font-weight:700;color:var(--navy);font-size:0.9rem;margin-bottom:0.3rem">Gen Z (1997–2012)</p>
        <p>Nativos digitales. Autenticidad, velocidad y propósito. TikTok e Instagram. Deciden rápido si el contenido los atrapa.</p>
      </div>
      <div class="sb-card" style="background:#f0fdf4;border-color:rgba(74,222,128,0.3)">
        <h4 style="color:#16a34a">Oferta especial</h4>
        <p style="font-weight:700;color:#15803d;font-size:0.85rem;margin-bottom:0.3rem">🎁 Consultoría 100% gratis</p>
        <p style="color:#166534">24 horas de asesoría estratégica sin ningún costo. Solo por tiempo limitado.</p>
        <button class="btn-p" style="width:100%;margin-top:0.8rem;background:#16a34a" onclick="showPage('contacto',null)">¡La quiero gratis! →</button>
      </div>
      <div class="sb-card">
        <h4>Temas</h4>
        <div><span class="sb-tag">Plan de marketing</span><span class="sb-tag">Modelo POEM</span><span class="sb-tag">Tráfico frío</span><span class="sb-tag">Inbound</span><span class="sb-tag">Gen Z</span><span class="sb-tag">IA</span></div>
      </div>
    </aside>
  </div>
  <footer>
    <div class="foot-logo">VORTEX <span>AIMA</span></div>
    <p>© 2025 Vortex Aima · Agencia de Marketing e Inteligencia Artificial</p>
  </footer>
</div>

<!-- PAGE 3: CONTACTO -->
<div class="page" id="contacto">
  <div class="ticker">$200K invertidos → $1.2M facturados · Primera AIMA en la región · Consultoría GRATIS por 24 horas</div>
  <div class="contact-head">
    <div class="s-eye light">↳ Trabaja con nosotros</div>
    <h1>ESCALA TU NEGOCIO. <em>HOY.</em></h1>
    <p>¿Listo para crecer con estrategia e inteligencia artificial? Agenda tu cita, cuéntanos tu reto y armamos el plan.</p>
    <div class="free-offer">
      <div class="free-offer-icon">🎁</div>
      <div>
        <h4>Consultoría estratégica 100% gratis</h4>
        <p>Chatea con Aima ahora, déjanos tu correo y recibe <strong style="color:#4ade80">24 horas de asesoría sin costo.</strong> Sin compromisos, sin letra pequeña.</p>
      </div>
    </div>
  </div>
  <div class="contact-body">
    <div>
      <div class="s-eye" style="margin-bottom:0.7rem">↳ Nuestros servicios</div>
      <div class="svc-list">
        <div class="svc-i"><div class="svc-num">01</div><div><div class="svc-t">Pauta digital & Performance</div><div class="svc-d">Meta, TikTok, Google Ads. ROI real y medible en cada campaña.</div></div></div>
        <div class="svc-i"><div class="svc-num">02</div><div><div class="svc-t">Contenido que convierte</div><div class="svc-d">Video, diseño y copy adaptado a tu audiencia y temperatura de tráfico.</div></div></div>
        <div class="svc-i"><div class="svc-num">03</div><div><div class="svc-t">Automatización con IA</div><div class="svc-d">Chatbots y flujos automáticos para vender 24/7 sin intervención constante.</div></div></div>
        <div class="svc-i"><div class="svc-num">04</div><div><div class="svc-t">Consultoría estratégica 360°</div><div class="svc-d">Plan completo: embudo, POEM, segmentación generacional y KPIs.</div></div></div>
        <div class="svc-i"><div class="svc-num">05</div><div><div class="svc-t">Activaciones BTL</div><div class="svc-d">Experiencias físicas que generan UGC, recordación y viralidad orgánica.</div></div></div>
      </div>
    </div>
    <div>
      <div class="cb-section-label">↳ Chatea con Aima · Asistente IA</div>
      <div class="cb-free-teaser">
        <span>🎁</span>
        <p>Chatea ahora y reclama tu <strong>consultoría gratis de 24 horas.</strong> Solo déjanos tu correo al final.</p>
      </div>
      <div class="cb-wrap">
        <div class="cb-h">
          <div class="cb-av">AI</div>
          <div><div class="cb-name">Aima · Asistente de Vortex</div><div class="cb-status">● En línea — IA activa</div></div>
        </div>
        <div class="cb-msgs" id="cbMsgs">
          <div class="msg bot">¡Hola! 👋 Soy Aima, el asistente IA de Vortex Aima. Si chateas conmigo hoy te regalamos una <strong>consultoría estratégica 100% gratis por 24 horas</strong> 🎁 ¿Empezamos?</div>
          <div class="cb-opts" id="opts0">
            <button class="cb-opt" onclick="botQ1('Sí, quiero mi consultoría gratis')">Sí, quiero mi consultoría gratis 🎁</button>
            <button class="cb-opt" onclick="botQ1('Solo quiero información')">Solo quiero información</button>
          </div>
        </div>
        <div class="cb-ir">
          <input type="text" id="cbInput" placeholder="Escribe tu mensaje..." onkeydown="if(event.key==='Enter')sendCb()"/>
          <button class="cb-send" onclick="sendCb()">Enviar</button>
        </div>
      </div>
    </div>
  </div>
  <footer>
    <div class="foot-logo">VORTEX <span>AIMA</span></div>
    <p>© 2025 Vortex Aima · Agencia de Marketing e Inteligencia Artificial · Pasto, Colombia</p>
  </footer>
</div>

<script>
function showPage(id,btn){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  document.querySelectorAll('.nav-links button').forEach(b=>b.classList.remove('active'));
  if(btn)btn.classList.add('active');
  window.scrollTo(0,0);
}
let cbPhase=0;
function addMsg(t,who){
  const c=document.getElementById('cbMsgs');
  const d=document.createElement('div');
  d.className='msg '+who;
  d.innerHTML=t;
  c.appendChild(d);
  c.scrollTop=c.scrollHeight;
}
function addOpts(opts,fn){
  const c=document.getElementById('cbMsgs');
  const w=document.createElement('div');
  w.className='cb-opts';
  opts.forEach(o=>{
    const b=document.createElement('button');
    b.className='cb-opt';
    b.textContent=o;
    b.onclick=()=>fn(o);
    w.appendChild(b);
  });
  c.appendChild(w);
  c.scrollTop=c.scrollHeight;
}
function addEmailInput(){
  const c=document.getElementById('cbMsgs');
  const w=document.createElement('div');
  w.style.cssText='display:flex;flex-direction:column;gap:0.4rem;align-self:flex-start;max-width:90%';
  w.innerHTML='<input id="emailIn" type="email" placeholder="tucorreo@email.com" style="background:#f4f5f8;border:1px solid #305aa3;color:#060834;font-family:Inter,sans-serif;font-size:0.78rem;padding:0.5rem 0.8rem;border-radius:3px;outline:none;width:220px"><button onclick="submitEmail()" style="background:#305aa3;border:none;color:#fff;font-family:Inter,sans-serif;font-weight:700;font-size:0.75rem;padding:0.45rem 1rem;cursor:pointer;border-radius:3px;letter-spacing:0.04em;text-transform:uppercase;width:fit-content">Enviar correo →</button>';
  c.appendChild(w);
  c.scrollTop=c.scrollHeight;
}
function submitEmail(){
  const v=document.getElementById('emailIn').value.trim();
  if(!v)return;
  const parent=document.getElementById('emailIn').parentElement;
  parent.remove();
  addMsg(v,'user');
  cbPhase=3;
  setTimeout(()=>{
    addMsg('¡Perfecto! 🚀 Hemos registrado tu correo <strong style="color:#305aa3">'+v+'</strong>. En menos de 24 horas un estratega de Vortex Aima te contacta con tu consultoría gratuita. ¡Que empiece el crecimiento! 💪','bot');
  },600);
}
function botQ1(v){
  document.getElementById('opts0').remove();
  addMsg(v,'user');
  cbPhase=1;
  setTimeout(()=>{
    addMsg('Perfecto 🔥 ¿Cuál es el mayor reto de tu negocio ahora mismo?','bot');
    addOpts(['No consigo clientes online','Mi pauta no convierte','No sé por dónde empezar','Quiero automatizar con IA'],botQ2);
  },600);
}
function botQ2(v){
  addMsg(v,'user');
  cbPhase=2;
  setTimeout(()=>{
    addMsg('Entendido, ese reto lo resolvemos. 💡 Para enviarte tu consultoría gratis de 24 horas, ¿cuál es tu correo electrónico?','bot');
    addEmailInput();
  },600);
}
function sendCb(){
  const i=document.getElementById('cbInput');
  const t=i.value.trim();
  if(!t)return;
  if(cbPhase===2){
    const em=document.querySelector('#cbMsgs input[type="email"]');
    if(em){em.value=t;submitEmail();i.value='';return;}
  }
  addMsg(t,'user');
  i.value='';
  setTimeout(()=>{
    if(cbPhase===0)addMsg('¿Quieres tu consultoría gratis o solo buscas información?','bot');
    else if(cbPhase===1)addMsg('¿Cuál es el mayor reto de tu negocio ahora mismo?','bot');
    else if(cbPhase===3)addMsg('¡Ya estás registrado! En menos de 24h te contactamos. 🚀','bot');
  },700);
}
</script>
</body>
</html>
