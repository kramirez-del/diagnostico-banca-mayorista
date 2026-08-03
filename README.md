[Uploading Diagnostico_Est<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Diagnóstico Estratégico Banca Mayorista · Consubanco</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Merriweather:wght@400;700;900&family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --navy:#1B355D;
  --navy2:#253F72;
  --teal:#7DACE3;
  --teal2:#5B9AD4;
  --gold:#E75301;
  --gold-light:#E75301;
  --slate:#666666;
  --border:#D9D9D9;
  --bg:#F5F5F5;
  --white:#FFFFFF;
  --text:#1B355D;
  --muted:#666666;
  --orange:#E75301;
  --red:#983920;
  --green:#007A29;
  --radius:8px;
  --radius-lg:14px;
}
html{scroll-behavior:smooth}
body{font-family:'Inter',sans-serif;color:var(--text);background:var(--bg);line-height:1.6;font-size:15px;-webkit-font-smoothing:antialiased}

/* ── NAV ─────────────────────────────────────────── */
.nav{position:sticky;top:0;z-index:100;background:rgba(27,43,75,0.97);backdrop-filter:blur(12px);border-bottom:1px solid rgba(255,255,255,0.07);display:flex;align-items:center;padding:0 40px;height:54px;overflow-x:auto;scrollbar-width:none;gap:0}
.nav::-webkit-scrollbar{display:none}
.nav-brand{font-family:'Merriweather',serif;font-size:12px;font-weight:700;color:rgba(255,255,255,0.85);white-space:nowrap;margin-right:32px;padding-right:32px;border-right:1px solid rgba(255,255,255,0.12)}
.nav a{font-size:12px;font-weight:500;color:rgba(255,255,255,0.5);text-decoration:none;white-space:nowrap;padding:0 14px;height:54px;display:flex;align-items:center;letter-spacing:.02em;transition:color .15s,border-color .15s;border-bottom:2px solid transparent}
.nav a:hover{color:rgba(255,255,255,.9);border-bottom-color:rgba(231,83,1,.6)}

/* ── PROGRESS BAR ─────────────────────────────────── */
.progress-bar{position:fixed;top:0;left:0;height:3px;background:var(--gold-light);z-index:200;width:0%;transition:width .1s linear}

/* ── HERO ─────────────────────────────────────────── */
.hero{background:var(--navy);min-height:92vh;display:flex;flex-direction:column;justify-content:center;padding:80px 72px 64px;position:relative;overflow:hidden}
.hero::before{content:'';position:absolute;top:0;right:0;width:55%;height:100%;background:linear-gradient(135deg,transparent 40%,rgba(231,83,1,0.06) 100%);pointer-events:none}
.hero::after{content:'';position:absolute;bottom:-160px;left:-160px;width:500px;height:500px;border-radius:50%;border:1px solid rgba(255,255,255,0.04);pointer-events:none}
.hero-tag{font-size:11px;font-weight:700;letter-spacing:.2em;text-transform:uppercase;color:#F2A07A;margin-bottom:48px;display:flex;align-items:center;gap:12px}
.hero-tag::after{content:'';flex:1;max-width:100px;height:1px;background:rgba(231,83,1,0.4)}
.hero h1{font-family:'Merriweather',serif;font-size:52px;font-weight:900;color:var(--white);line-height:1.06;letter-spacing:-.02em;margin-bottom:22px;max-width:680px}
.hero h1 em{font-style:italic;font-weight:300;color:rgba(255,255,255,0.65)}
.hero-sub{font-size:17px;font-weight:300;color:rgba(255,255,255,0.55);max-width:500px;line-height:1.75;margin-bottom:56px}
.hero-kpis{display:flex;gap:0;border-top:1px solid rgba(255,255,255,0.1)}
.kpi-item{padding:22px 28px 0;border-right:1px solid rgba(255,255,255,0.08)}
.kpi-item:first-child{padding-left:0}
.kpi-item:last-child{border-right:none}
.kpi-num{font-family:'Merriweather',serif;font-size:34px;font-weight:700;color:#F2A07A;line-height:1}
.kpi-label{font-size:12px;color:rgba(255,255,255,0.45);margin-top:5px;line-height:1.4}
.hero-bottom{position:absolute;bottom:36px;right:72px;text-align:right}
.hero-bottom span{font-size:11px;color:rgba(255,255,255,.3);letter-spacing:.06em;text-transform:uppercase}

/* ── SECTIONS ─────────────────────────────────────── */
.section{padding:72px 72px}
.section.light{background:var(--white)}
.section.dark{background:var(--navy)}
.section.teal{background:var(--teal)}
.eyebrow{font-size:11px;font-weight:700;letter-spacing:.18em;text-transform:uppercase;color:var(--orange);margin-bottom:14px;display:flex;align-items:center;gap:10px}
.eyebrow::before{content:'';width:20px;height:2px;background:var(--orange);flex-shrink:0}
.eyebrow.light-eye{color:#F2A07A}
.eyebrow.light-eye::before{background:#F2A07A}
.sec-title{font-family:'Merriweather',serif;font-size:34px;font-weight:700;color:var(--navy);line-height:1.18;letter-spacing:-.01em;margin-bottom:14px}
.sec-title.white{color:var(--white)}
.sec-lead{font-size:16px;color:var(--muted);max-width:640px;line-height:1.75;margin-bottom:48px}
.sec-lead.white{color:rgba(255,255,255,0.6)}

/* ── HALLAZGO PRINCIPAL ──────────────────────────── */
.hallazgo-box{background:linear-gradient(135deg,rgba(231,83,1,0.06),rgba(27,43,75,0.04));border-left:4px solid var(--orange);border-radius:0 var(--radius-lg) var(--radius-lg) 0;padding:28px 32px;margin-bottom:40px}
.hallazgo-label{font-size:11px;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:var(--orange);margin-bottom:10px}
.hallazgo-text{font-size:16px;font-weight:500;color:var(--navy);line-height:1.65}

/* ── TABLA DE 4 COLUMNAS ─────────────────────────── */
.tabla-4{width:100%;border-collapse:separate;border-spacing:0;border:1px solid var(--border);border-radius:var(--radius-lg);overflow:hidden;margin-bottom:40px}
.tabla-4 th{background:var(--navy);color:rgba(255,255,255,.82);font-size:13px;font-weight:700;padding:14px 20px;text-align:left;letter-spacing:.03em}
.tabla-4 td{padding:16px 20px;font-size:14px;color:var(--text);border-bottom:1px solid var(--border);vertical-align:top;line-height:1.6;background:var(--white)}
.tabla-4 tr:last-child td{border-bottom:none}
.tabla-4 tr:hover td{background:var(--bg)}

/* ── CARDS HALLAZGOS ─────────────────────────────── */
.cards-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-bottom:40px}
.cards-grid.two{grid-template-columns:repeat(2,1fr)}
.card{background:var(--white);border:1px solid var(--border);border-radius:var(--radius-lg);padding:26px 24px;position:relative;overflow:hidden;transition:all .2s ease}
.card:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(27,43,75,.1)}
.card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:var(--border)}
.card.gold::before{background:var(--orange)}
.card.navy::before{background:var(--navy)}
.card.teal::before{background:var(--teal)}
.card.red::before{background:var(--red)}
.card.green::before{background:var(--green)}
.card-num{font-family:'Merriweather',serif;font-size:40px;font-weight:700;color:rgba(27,43,75,.1);margin-bottom:14px;line-height:1}
.card-label{font-size:11px;font-weight:700;letter-spacing:.1em;text-transform:uppercase;color:var(--orange);margin-bottom:6px}
.card-title{font-size:15px;font-weight:800;color:var(--navy);margin-bottom:8px;line-height:1.3}
.card-body{font-size:13px;color:var(--muted);line-height:1.65}
.card-tag{display:inline-block;font-size:11px;font-weight:700;padding:3px 10px;border-radius:10px;margin-top:12px;background:rgba(27,43,75,.07);color:var(--navy)}

/* ── PATRONES ─────────────────────────────────────── */
.patron-list{display:flex;flex-direction:column;gap:1px;background:var(--border);border:1px solid var(--border);border-radius:var(--radius-lg);overflow:hidden}
.patron-row{background:var(--white);padding:22px 26px;display:grid;grid-template-columns:52px 1fr auto;gap:16px;align-items:center;transition:background .12s}
.patron-row:hover{background:var(--bg)}
.patron-idx{font-family:'Merriweather',serif;font-size:20px;font-weight:700;color:rgba(168,120,48,.3);text-align:center}
.patron-name{font-size:15px;font-weight:800;color:var(--navy);margin-bottom:4px}
.patron-desc{font-size:13px;color:var(--muted);line-height:1.55}
.patron-badge{font-size:11px;font-weight:700;padding:5px 12px;border-radius:10px;white-space:nowrap;flex-shrink:0}
.pb-gold{background:rgba(231,83,1,.1);color:var(--orange)}
.pb-navy{background:rgba(27,43,75,.08);color:var(--navy)}
.pb-red{background:rgba(184,48,48,.1);color:var(--red)}
.pb-teal{background:rgba(30,107,114,.1);color:var(--teal)}

/* ── DIMENSIONES ──────────────────────────────────── */
.dim-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;margin-bottom:40px}
.dim-card{background:var(--white);border:1px solid var(--border);border-radius:var(--radius-lg);padding:24px 20px;text-align:center}
.dim-pct{font-family:'Merriweather',serif;font-size:36px;font-weight:700;color:var(--navy);line-height:1}
.dim-name{font-size:12px;font-weight:700;color:var(--muted);margin-top:6px;line-height:1.4}
.dim-bar-track{height:6px;background:var(--border);border-radius:3px;overflow:hidden;margin-top:12px}
.dim-bar-fill{height:100%;border-radius:3px}

/* ── CICLO DE VIDA TIMELINE ───────────────────────── */
.ciclo-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--border);border:1px solid var(--border);border-radius:var(--radius-lg);overflow:hidden}
.ciclo-step{background:var(--white);padding:28px 22px}
.ciclo-num{font-size:11px;font-weight:700;letter-spacing:.1em;text-transform:uppercase;color:var(--orange);margin-bottom:10px}
.ciclo-name{font-size:14px;font-weight:800;color:var(--navy);margin-bottom:10px;line-height:1.3}
.ciclo-items{display:flex;flex-direction:column;gap:6px}
.ciclo-item{font-size:12.5px;color:var(--muted);line-height:1.5;padding-left:12px;position:relative}
.ciclo-item::before{content:'·';position:absolute;left:0;color:var(--orange)}
.ciclo-gap{background:rgba(184,48,48,.05);border-top:2px solid var(--red)}
.ciclo-gap-label{font-size:10px;font-weight:700;letter-spacing:.08em;text-transform:uppercase;color:var(--red);margin-bottom:8px}

/* ── CAPACIDADES TRANSVERSALES ───────────────────── */
.cap-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:16px}
.cap-card{background:rgba(255,255,255,0.05);border:1px solid rgba(255,255,255,0.1);border-radius:var(--radius-lg);padding:24px 22px}
.cap-card-title{font-size:14px;font-weight:800;color:var(--white);margin-bottom:8px}
.cap-card-body{font-size:12.5px;color:rgba(255,255,255,0.55);line-height:1.65}
.cap-card-tag{font-size:10px;font-weight:700;padding:3px 10px;border-radius:10px;margin-top:12px;display:inline-block;background:rgba(231,83,1,.2);color:#F2A07A}

/* ── CONTEXTO MERCADO ──────────────────────────────── */
.mercado-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.mercado-card{border:1px solid var(--border);border-radius:var(--radius-lg);padding:26px 22px;background:var(--white)}
.mercado-stat{font-family:'Merriweather',serif;font-size:32px;font-weight:700;color:var(--teal);margin-bottom:6px}
.mercado-title{font-size:14px;font-weight:800;color:var(--navy);margin-bottom:8px}
.mercado-body{font-size:13px;color:var(--muted);line-height:1.6}

/* ── OPORTUNIDADES ────────────────────────────────── */
.opor-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.opor-card{border-radius:var(--radius-lg);padding:28px 24px;position:relative;overflow:hidden}
.opor-card.navy{background:var(--navy)}
.opor-card.teal{background:var(--teal)}
.opor-card.gold{background:linear-gradient(135deg,var(--navy),#1E3060)}
.opor-tag{font-size:10px;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:rgba(255,255,255,0.5);margin-bottom:14px}
.opor-title{font-size:16px;font-weight:800;color:white;margin-bottom:10px;line-height:1.3}
.opor-body{font-size:12.5px;color:rgba(255,255,255,0.6);line-height:1.65}

/* ── ACORDEÓN ──────────────────────────────────────── */
.acord{border:1px solid var(--border);border-radius:var(--radius-lg);margin-bottom:10px;overflow:hidden;background:var(--white)}
.acord-hdr{display:flex;justify-content:space-between;align-items:center;padding:20px 26px;cursor:pointer;transition:background .12s}
.acord-hdr:hover{background:var(--bg)}
.acord-left{display:flex;align-items:center;gap:16px}
.acord-title{font-size:15px;font-weight:800;color:var(--navy)}
.acord-sub{font-size:12px;color:var(--muted);margin-top:2px}
.acord-icon{width:30px;height:30px;border-radius:50%;background:var(--bg);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;flex-shrink:0;transition:transform .2s,background .15s}
.acord.open .acord-icon{transform:rotate(180deg);background:var(--navy);border-color:var(--navy)}
.acord.open .acord-icon svg{stroke:white}
.acord-body{display:none;padding:4px 26px 26px}
.acord.open .acord-body{display:block;animation:fadeInAc .2s ease}
@keyframes fadeInAc{from{opacity:0;transform:translateY(-4px)}to{opacity:1;transform:translateY(0)}}

/* ── DIVIDER ──────────────────────────────────────── */
.divider{display:flex;align-items:center;gap:14px;margin:20px 0 18px}
.div-line{flex:1;height:1px;background:var(--border)}
.div-label{font-size:11px;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:var(--muted);padding:0 4px;white-space:nowrap}

/* ── CIERRE ───────────────────────────────────────── */
.cierre-box{background:linear-gradient(135deg,var(--navy),#0E1D35);border-radius:var(--radius-lg);padding:48px 44px;position:relative;overflow:hidden}
.cierre-box::before{content:'';position:absolute;top:-120px;right:-120px;width:320px;height:320px;border-radius:50%;border:40px solid rgba(231,83,1,0.07)}
.cierre-quote{font-family:'Merriweather',serif;font-size:22px;font-weight:400;color:white;line-height:1.6;font-style:italic;margin-bottom:32px;position:relative}
.cierre-quote b{font-weight:700;font-style:normal;color:var(--gold-light)}
.cierre-steps{display:grid;grid-template-columns:repeat(3,1fr);gap:1px;background:rgba(255,255,255,0.08);margin-top:32px;border-radius:var(--radius);overflow:hidden}
.cierre-step{padding:20px 22px}
.cierre-step-label{font-size:10px;font-weight:700;letter-spacing:.1em;text-transform:uppercase;color:#F2A07A;margin-bottom:6px}
.cierre-step-text{font-size:13px;color:rgba(255,255,255,0.7);line-height:1.55}

/* ── FOOTER ───────────────────────────────────────── */
.footer{background:var(--navy);padding:28px 72px;display:flex;align-items:center;justify-content:space-between;border-top:1px solid rgba(255,255,255,0.06)}
.footer-brand{font-family:'Merriweather',serif;font-size:13px;font-weight:700;color:rgba(255,255,255,.7)}
.footer-meta{font-size:11px;color:rgba(255,255,255,.3);letter-spacing:.04em}

/* ── CHALLENGE DIRECTOR ────────────────────────── */
.challenge-section{padding:72px 72px;background:var(--navy);position:relative;overflow:hidden}
.challenge-section::before{content:'';position:absolute;bottom:-200px;right:-200px;width:600px;height:600px;border-radius:50%;border:1px solid rgba(255,255,255,0.04)}
.challenge-grid-top{display:grid;grid-template-columns:1fr 1fr 1fr;gap:1px;background:rgba(255,255,255,0.08);border-radius:var(--radius-lg);overflow:hidden;margin-bottom:2px}
.challenge-col{padding:32px 28px}
.challenge-col-header{font-size:11px;font-weight:700;letter-spacing:.15em;text-transform:uppercase;color:#F2A07A;margin-bottom:6px}
.challenge-col-title{font-family:'Merriweather',serif;font-size:20px;font-weight:700;color:white;margin-bottom:18px;line-height:1.25}
.challenge-item{display:flex;gap:10px;align-items:flex-start;margin-bottom:12px}
.challenge-dot{width:6px;height:6px;border-radius:50%;flex-shrink:0;margin-top:6px;background:var(--orange)}
.challenge-dot.teal{background:var(--teal)}
.challenge-dot.green{background:#4CAF7D}
.challenge-item-text{font-size:13px;color:rgba(255,255,255,0.65);line-height:1.6}
.challenge-gap-row{display:grid;grid-template-columns:1fr 1fr 1fr;gap:1px;background:rgba(255,255,255,0.08);border-radius:var(--radius-lg);overflow:hidden;margin-bottom:20px}
.challenge-gap-col{padding:20px 28px;background:rgba(184,48,48,0.12)}
.challenge-gap-label{font-size:10px;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:#E07070;margin-bottom:8px}
.challenge-gap-item{font-size:12.5px;color:rgba(255,255,255,0.6);line-height:1.55;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06)}
.challenge-gap-item:last-child{border-bottom:none}
.pregunta-dir{background:rgba(231,83,1,0.12);border:1px solid rgba(231,83,1,0.25);border-radius:var(--radius-lg);padding:28px 32px;margin-top:20px}
.pregunta-dir-label{font-size:11px;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:var(--orange);margin-bottom:14px}
.pregunta-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.pregunta-card{background:rgba(255,255,255,0.05);border-radius:var(--radius);padding:18px 16px}
.pregunta-num{font-family:'Merriweather',serif;font-size:28px;font-weight:700;color:rgba(231,83,1,0.4);margin-bottom:8px}
.pregunta-text{font-size:13px;color:rgba(255,255,255,0.8);line-height:1.6;font-weight:500}
.pregunta-sub{font-size:12px;color:rgba(255,255,255,0.45);margin-top:6px;line-height:1.5}

</style>
</head>
<body>

<div class="progress-bar" id="pbar"></div>

<nav class="nav">
  <div class="nav-brand">Consubanco · Banca Mayorista</div>
  <a href="#contexto">Contexto</a>
  <a href="#metodologia">Metodología</a>
  <a href="#hallazgos">Hallazgos</a>
  <a href="#ciclo">Ciclo de vida</a>
  <a href="#capacidades">Capacidades</a>
  <a href="#mercado">Mercado</a>
  <a href="#oportunidades">Oportunidades</a><a href="#challenge">Síntesis para decisión</a>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-tag">Banca Mayorista · Diagnóstico Estratégico</div>
  <h1>Diagnóstico de capacidades para la evolución de la Banca Mayorista</h1>
  <p class="hero-sub">Síntesis de las necesidades de negocio, capacidades requeridas y brechas identificadas para la evolución de los segmentos PyME, Crédito Comercial y Banca de Gobierno.</p>
  <div class="hero-kpis">
    <div class="kpi-item">
      <div class="kpi-num">3</div>
      <div class="kpi-label">Segmentos analizados<br>PyME · Comercial · Gobierno</div>
    </div>
    <div class="kpi-item">
      <div class="kpi-num">5</div>
      <div class="kpi-label">Dimensiones<br>del diagnóstico</div>
    </div>
    <div class="kpi-item">
      <div class="kpi-num">4</div>
      <div class="kpi-label">Etapas del<br>ciclo de vida</div>
    </div>
    <div class="kpi-item">
      <div class="kpi-num">2031</div>
      <div class="kpi-label">Visión estratégica<br>Planeación Estratégica</div>
    </div>
  </div>
  <div class="hero-bottom">
    <span>Soluciones de Negocio · Dirección de Estrategia · 2026</span>
  </div>
</section>

<!-- ── CONTEXTO ──────────────────────────────────── -->
<section class="section light" id="contexto">
  <div class="eyebrow">Diagnóstico</div>
  <h2 class="sec-title">La Planeación 2027-2031 requiere definir un modelo de Banca Mayorista</h2>
  <p class="sec-lead">La Planeación Estratégica 2027-2031 amplió el alcance inicial del ejercicio para incorporar una visión de la Banca Mayorista. El diagnóstico identifica las necesidades comunes de los segmentos PyME, Crédito Comercial y Banca de Gobierno, así como las capacidades necesarias para atender sus diferencias de escala, complejidad y personalización.</p>

  <div class="hallazgo-box">
    <div class="hallazgo-label">Hallazgo central</div>
    <div class="hallazgo-text">Los tres segmentos comparten necesidades estructurales: digitalización del ciclo de vida, capacidad de decisión oportuna e integración de la relación con el cliente. La diferencia entre segmentos no radica en el tipo de necesidad, sino en el grado de complejidad y personalización requerido.</div>
  </div>

  <div class="tabla-4">
    <caption style="caption-side:top;font-size:13px;font-weight:800;color:var(--navy);text-align:left;padding:0 0 14px 0;letter-spacing:.01em">Principales conclusiones del levantamiento</caption>
    <thead>
      <tr>
        <th style="width:22%">Hallazgo clave</th>
        <th style="width:26%">Evidencia del levantamiento</th>
        <th style="width:26%">Lectura estratégica</th>
        <th style="width:26%">Implicación para Consubanco</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Los tres segmentos comparten necesidades estructurales.</strong></td>
        <td>Participantes de distintas áreas identificaron brechas coincidentes en la gestión del cliente, la oferta de productos y la operación.</td>
        <td>El modelo futuro no requiere soluciones independientes para cada segmento. Debe construirse sobre capacidades comunes que puedan configurarse de acuerdo con la complejidad y las necesidades específicas de cada banca.</td>
        <td>Diseñar una plataforma compartida y parametrizable permitiría aprovechar economías de escala, reducir la fragmentación tecnológica y acelerar la evolución de los tres segmentos.</td>
      </tr>
      <tr>
        <td><strong>La originación digital es una condición básica del modelo futuro.</strong></td>
        <td>El 100% de los participantes señaló que la originación de productos de crédito y captación debe realizarse de manera digital.</td>
        <td>Existe un mandato claro para reducir la dependencia de actividades presenciales en todas las etapas que puedan digitalizarse. La experiencia digital deja de ser un diferenciador y se convierte en el estándar mínimo esperado.</td>
        <td>El modelo operativo deberá diseñarse con la digitalización como ruta principal, incorporando atención asistida únicamente en los momentos que requieran acompañamiento o validaciones especializadas.</td>
      </tr>
      <tr>
        <td><strong>La decisión de crédito requiere dos rutas diferenciadas.</strong></td>
        <td>El levantamiento identificó una ruta paramétrica para créditos de menor monto y una ruta de comité para operaciones superiores a 4 millones de UDIS.</td>
        <td>El modelo de evaluación debe ser dual desde su diseño. Ambas rutas necesitan compartir información, controles y validaciones automatizadas, aunque el nivel de análisis y autorización sea diferente.</td>
        <td>Será prioritario desarrollar capacidades de scoring, integrar datos alternativos como CIEC y comportamiento previo, y automatizar las validaciones que anteceden tanto a la decisión paramétrica como al comité de crédito.</td>
      </tr>
    </tbody>
  </div>
</section>

<!-- ── METODOLOGÍA ───────────────────────────────── -->
<section class="section" id="metodologia">
  <div class="eyebrow">Enfoque de análisis</div>
  <h2 class="sec-title">El diagnóstico utilizó un marco común para comparar los tres segmentos</h2>
  <p class="sec-lead">El levantamiento se estructuró en cuatro dimensiones de análisis. Este enfoque permitió identificar capacidades comunes, diferencias específicas por segmento y brechas relevantes a lo largo del ciclo de vida.</p>

  <div class="cards-grid">
    <div class="card gold">
      <div class="card-label">Dimensión 1</div>
      <div class="card-title">Perfil y estructura del cliente</div>
      <div class="card-body">Caracterización del cliente, estructura organizacional, nivel de autonomía y forma de interacción con el banco. Resultado: definición de los perfiles de cliente por segmento y sus requisitos de personalización.</div>
      <div class="card-tag">PyME · Comercial · Gobierno</div>
    </div>
    <div class="card navy">
      <div class="card-label">Dimensión 2</div>
      <div class="card-title">Portafolio y estructura de producto</div>
      <div class="card-body">Identificación de los productos requeridos, condiciones configurables y nivel de estandarización esperado por segmento. Resultado: mapa de productos con grado de flexibilidad por segmento.</div>
      <div class="card-tag">Crédito · Captación · Servicios</div>
    </div>
    <div class="card teal">
      <div class="card-label">Dimensión 3</div>
      <div class="card-title">Ciclo de vida del producto</div>
      <div class="card-body">Análisis de actividades, validaciones, responsables y brechas en cada etapa del ciclo de vida. Resultado: mapa de capacidades requeridas por etapa: originación, evaluación, formalización y operación.</div>
      <div class="card-tag">4 etapas · Validaciones · Actividades clave</div>
    </div>
    <div class="card gold">
      <div class="card-label">Dimensión 4</div>
      <div class="card-title">Capacidades transversales</div>
      <div class="card-body">Identificación de las capacidades regulatorias, operativas, tecnológicas y de control compartidas por los tres segmentos. Resultado: mapa de capacidades habilitadoras del modelo operativo.</div>
      <div class="card-tag">CNBV · PLD · KYC · Core</div>
    </div>
    <div class="card navy">
      <div class="card-label">Alcance</div>
      <div class="card-title">Lo que esta sesión SÍ fue</div>
      <div class="card-body">Una conversación estratégica para identificar necesidades de negocio, no operativas.<br>Un espacio para entender diferencias y puntos comunes entre segmentos.<br>Una visualización de cómo queremos operar a futuro.</div>
      <div class="card-tag">Enfoque estratégico</div>
    </div>
    <div class="card red">
      <div class="card-label">Límites del ejercicio</div>
      <div class="card-title">Lo que esta sesión NO fue</div>
      <div class="card-body">No fue un levantamiento operativo tradicional.<br>No fue una revisión de tickets o dolores puntuales por área.<br>No fue un espacio para diseño funcional específico ni definición de soluciones.</div>
      <div class="card-tag">No es diseño funcional</div>
    </div>
  </div>
</section>

<!-- ── HALLAZGOS SEGMENTO POR SEGMENTO ────────────── -->
<section class="section light" id="hallazgos">
  <div class="eyebrow">Hallazgos transversales</div>
  <h2 class="sec-title">Cinco brechas estructurales limitan la evolución del modelo mayorista</h2>
  <p class="sec-lead">El levantamiento identificó brechas comunes en la información del cliente, la evaluación de crédito, la digitalización del proceso, las capacidades del core bancario y la experiencia empresarial. Estas brechas afectan a los tres segmentos, aunque su impacto y complejidad varían en cada uno. Su recurrencia en distintas áreas indica que corresponden al modelo operativo y no únicamente a procesos particulares.</p>

  <div class="patron-list">
    <div class="patron-row">
      <div class="patron-idx">01</div>
      <div>
        <div class="patron-name">El levantamiento identificó la necesidad de un expediente único y trazable</div>
        <div class="patron-desc">El levantamiento identificó la ausencia de una fuente única de información del cliente que conecte los sistemas. La información de originación, evaluación, formalización y operación vive en silos. El mismo dato se captura múltiples veces.</div>
      </div>
      <div class="patron-badge pb-red">Crítico</div>
    </div>
    <div class="patron-row">
      <div class="patron-idx">02</div>
      <div>
        <div class="patron-name">La evaluación de crédito carece de un modelo paramétrico formal</div>
        <div class="patron-desc">La aprobación depende de la intervención de analistas en la mayoría de las solicitudes. Se identificó consenso sobre la necesidad de una ruta paramétrica con datos alternativos (CIEC, comportamiento, buró) y una ruta de comité para créditos mayores.</div>
      </div>
      <div class="patron-badge pb-red">Crítico</div>
    </div>
    <div class="patron-row">
      <div class="patron-idx">03</div>
      <div>
        <div class="patron-name">La incorporación del cliente y la formalización presentan dependencias presenciales</div>
        <div class="patron-desc">El proceso de conocimiento del cliente (KYC), integración del expediente y formalización presenta etapas no digitalizadas que limitan la velocidad y la trazabilidad. Se pierde ventaja competitiva en el momento de mayor disposición del cliente.</div>
      </div>
      <div class="patron-badge pb-gold">Alto</div>
    </div>
    <div class="patron-row">
      <div class="patron-idx">04</div>
      <div>
        <div class="patron-name">El core bancario presenta limitaciones para el segmento empresarial</div>
        <div class="patron-desc">El core actual presenta limitaciones para administrar la complejidad del crédito comercial, que incluye múltiples disposiciones, devengamiento diferenciado, garantías cruzadas, prelación de pagos y reportería regulatoria diferenciada por segmento.</div>
      </div>
      <div class="patron-badge pb-gold">Alto</div>
    </div>
    <div class="patron-row">
      <div class="patron-idx">05</div>
      <div>
        <div class="patron-name">La experiencia del cliente se encuentra fragmentada entre productos</div>
        <div class="patron-desc">Los participantes señalaron la necesidad de mayor autonomía transaccional, visibilidad del portafolio y acceso integrado a los productos. Las capacidades actuales no cubren completamente estos requerimientos para el segmento mayorista.</div>
      </div>
      <div class="patron-badge pb-navy">Medio-Alto</div>
    </div>
  </div>

  <div class="divider" style="margin-top:40px">
    <div class="div-line"></div>
    <div class="div-label">Hallazgos por segmento</div>
    <div class="div-line"></div>
  </div>

  <div class="acord open">
    <div class="acord-hdr" onclick="this.closest('.acord').classList.toggle('open')">
      <div class="acord-left">
        <div>
          <div class="acord-title">PyME Segmento de mayor potencial de escala</div>
          <div class="acord-sub">Acceso limitado al crédito formal · Relevancia de la digitalización · Capital de trabajo como producto base</div>
        </div>
      </div>
      <div class="acord-icon"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="var(--navy)" stroke-width="2.5"><polyline points="6 9 12 15 18 9"/></svg></div>
    </div>
    <div class="acord-body">
      <div class="cards-grid" style="margin-bottom:0">
        <div class="card gold">
          <div class="card-label">Perfil</div>
          <div class="card-title">Persona Moral o PFAE con necesidad de crédito y administración de excedentes</div>
          <div class="card-body">Clientes con bajo historial crediticio formal pero con actividad empresarial real. Requieren operar desde banca digital. Buscan capital de trabajo de corto plazo, inversiones de excedentes y servicios de pago integrados.</div>
        </div>
        <div class="card teal">
          <div class="card-label">Necesidad de negocio</div>
          <div class="card-title">Crédito rápido, digital y sin fricciones de proceso</div>
          <div class="card-body">Proceso de crédito digital con menores tiempos de respuesta. Crédito revolvente y cuenta corriente como productos base. Modelo de evaluación paramétrico con CIEC y datos alternativos. Formalización digital post-aprobación. El tiempo hasta la disposición de los recursos es un factor relevante para la competitividad.</div>
        </div>
        <div class="card navy">
          <div class="card-label">Brecha principal</div>
          <div class="card-title">La evaluación actual no está diseñada para este perfil de riesgo</div>
          <div class="card-body">Con historial crediticio formal limitado, la evaluación paramétrica requiere incorporar datos alternativos. El proceso de análisis actual genera tiempos que pueden afectar la competitividad del segmento.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="acord">
    <div class="acord-hdr" onclick="this.closest('.acord').classList.toggle('open')">
      <div class="acord-left">
        <div>
          <div class="acord-title">Crédito Comercial Segmento de mayor complejidad técnica</div>
          <div class="acord-sub">Créditos estructurados · Garantías reales · Evaluación por comité · Múltiples disposiciones</div>
        </div>
      </div>
      <div class="acord-icon"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="var(--navy)" stroke-width="2.5"><polyline points="6 9 12 15 18 9"/></svg></div>
    </div>
    <div class="acord-body">
      <div class="cards-grid" style="margin-bottom:0">
        <div class="card gold">
          <div class="card-label">Perfil</div>
          <div class="card-title">Empresa mediana o grande con proyectos de fondeo e inversión productiva</div>
          <div class="card-body">Persona moral con necesidad de financiamiento estructurado. Dos productos típicos: capital de trabajo y crédito de inversión. Requiere autonomía transaccional y herramientas de tesorería.</div>
        </div>
        <div class="card teal">
          <div class="card-label">Necesidad de negocio</div>
          <div class="card-title">Flexibilidad de producto y análisis de crédito diferenciado</div>
          <div class="card-body">Tasas, plazos, amortización y garantías configurables. Ruta de comité para créditos mayores a 4 millones de UDIS. Integración con ERP del cliente. Reportería regulatoria separada de la administración operativa del crédito.</div>
        </div>
        <div class="card navy">
          <div class="card-label">Brecha principal</div>
          <div class="card-title">El core actual no soporta la complejidad del producto</div>
          <div class="card-body">Múltiples disposiciones, devengamiento diferenciado, garantías cruzadas entre productos y reportería regulatoria diferenciada son capacidades que el core actual tiene limitadas. Requiere modernización o capa de abstracción.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="acord">
    <div class="acord-hdr" onclick="this.closest('.acord').classList.toggle('open')">
      <div class="acord-left">
        <div>
          <div class="acord-title">Banca de Gobierno Segmento de mayor necesidad de servicio integral</div>
          <div class="acord-sub">Captación institucional · Dispersión de nómina · Requerimientos regulatorios diferenciados</div>
        </div>
      </div>
      <div class="acord-icon"><svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="var(--navy)" stroke-width="2.5"><polyline points="6 9 12 15 18 9"/></svg></div>
    </div>
    <div class="acord-body">
      <div class="cards-grid" style="margin-bottom:0">
        <div class="card gold">
          <div class="card-label">Perfil</div>
          <div class="card-title">Institución pública con necesidades de captación, dispersión y servicios financieros</div>
          <div class="card-body">Entidades gubernamentales con alta autonomía transaccional. Productos: cuentas productivas, dispersión de nómina, inversiones. Requieren cumplimiento regulatorio diferenciado y control de usuarios con atributos.</div>
        </div>
        <div class="card teal">
          <div class="card-label">Necesidad de negocio</div>
          <div class="card-title">Oferta integrada de servicios bancarios y transaccionales</div>
          <div class="card-body">Banca digital robusta con manejo de tesorería, pagos masivos y transferencias. Múltiples usuarios con niveles de autorización diferenciados. Reportería regulatoria de IPAB, CNBV e inversiones.</div>
        </div>
        <div class="card navy">
          <div class="card-label">Brecha principal</div>
          <div class="card-title">Las capacidades actuales no cubren completamente los requerimientos del segmento</div>
          <div class="card-body">Las capacidades actuales no cubren completamente los requerimientos del segmento en materia de herramientas de tesorería, visibilidad de flujos, pagos masivos y administración multiusuario.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── CICLO DE VIDA ──────────────────────────────── -->
<section class="section dark" id="ciclo">
  <div class="eyebrow light-eye">Brechas por etapa</div>
  <h2 class="sec-title white">Las brechas se presentan a lo largo de las cuatro etapas del ciclo de vida</h2>
  <p class="sec-lead white">El análisis comprendió las etapas de originación, evaluación y aprobación, formalización y activación, así como operación y administración. En cada una se identificaron capacidades requeridas y limitaciones del modelo actual.</p>

  <div class="ciclo-grid">
    <div class="ciclo-step">
      <div class="ciclo-num">Etapa 01</div>
      <div class="ciclo-name">Originación</div>
      <div class="ciclo-items">
        <div class="ciclo-item">Expediente de crédito y KYC digitales</div>
        <div class="ciclo-item">Onboarding multicanal (autoservicio y asistido)</div>
        <div class="ciclo-item">Datos alternativos desde el primer contacto</div>
        <div class="ciclo-item">Integración con SAT (CIEC) y buró legal</div>
        <div class="ciclo-item">Trazabilidad completa del expediente</div>
      </div>
      <div style="margin-top:16px;padding-top:14px;border-top:1px solid rgba(255,255,255,0.1)">
        <div style="font-size:11px;font-weight:700;letter-spacing:.08em;text-transform:uppercase;color:#F2A07A;margin-bottom:6px">Brecha identificada</div>
        <div style="font-size:12px;color:rgba(255,255,255,0.55);line-height:1.55">El proceso de incorporación del cliente no está digitalizado de extremo a extremo. El conocimiento del cliente (KYC) presenta etapas manuales y no se aprovechan sistemáticamente los datos de comportamiento previo.</div>
      </div>
    </div>
    <div class="ciclo-step">
      <div class="ciclo-num">Etapa 02</div>
      <div class="ciclo-name">Evaluación y aprobación</div>
      <div class="ciclo-items">
        <div class="ciclo-item">Ruta paramétrica para créditos menores</div>
        <div class="ciclo-item">Ruta de comité para operaciones superiores a 4 millones de UDIS</div>
        <div class="ciclo-item">Score con CIEC y datos alternativos</div>
        <div class="ciclo-item">PLD y listas negras automatizados</div>
        <div class="ciclo-item">Propietario real y CDD en tiempo real</div>
      </div>
      <div style="margin-top:16px;padding-top:14px;border-top:1px solid rgba(255,255,255,0.1)">
        <div style="font-size:11px;font-weight:700;letter-spacing:.08em;text-transform:uppercase;color:#F2A07A;margin-bottom:6px">Brecha identificada</div>
        <div style="font-size:12px;color:rgba(255,255,255,0.55);line-height:1.55">Actualmente no existe un modelo paramétrico formal y la evaluación depende de la intervención de analistas en la mayoría de las solicitudes. Los datos alternativos no se utilizan de forma sistemática.</div>
      </div>
    </div>
    <div class="ciclo-step">
      <div class="ciclo-num">Etapa 03</div>
      <div class="ciclo-name">Formalización y activación</div>
      <div class="ciclo-items">
        <div class="ciclo-item">Firma digital de contratos</div>
        <div class="ciclo-item">Cuenta Consubanco como requisito de dispersión</div>
        <div class="ciclo-item">Mesa de control eficiente</div>
        <div class="ciclo-item">Asignación correcta BP/BG/PyME</div>
        <div class="ciclo-item">Formalización rápida como ventaja competitiva</div>
      </div>
      <div style="margin-top:16px;padding-top:14px;border-top:1px solid rgba(255,255,255,0.1)">
        <div style="font-size:11px;font-weight:700;letter-spacing:.08em;text-transform:uppercase;color:#F2A07A;margin-bottom:6px">Brecha identificada</div>
        <div style="font-size:12px;color:rgba(255,255,255,0.55);line-height:1.55">La formalización posterior a la aprobación no está completamente digitalizada. El proceso de mesa de control genera tiempos de respuesta que afectan la competitividad del banco.</div>
      </div>
    </div>
    <div class="ciclo-step">
      <div class="ciclo-num">Etapa 04</div>
      <div class="ciclo-name">Operación y administración</div>
      <div class="ciclo-items">
        <div class="ciclo-item">Core bancario para gestión de cartera compleja</div>
        <div class="ciclo-item">Avisos automáticos de cobro y pago referenciado</div>
        <div class="ciclo-item">Reportería regulatoria diferenciada (CNBV, IPAB, Banxico)</div>
        <div class="ciclo-item">Recuperación administrativa y judicial</div>
        <div class="ciclo-item">Expediente único como fuente de verdad</div>
      </div>
      <div style="margin-top:16px;padding-top:14px;border-top:1px solid rgba(255,255,255,0.1)">
        <div style="font-size:11px;font-weight:700;letter-spacing:.08em;text-transform:uppercase;color:#F2A07A;margin-bottom:6px">Brecha identificada</div>
        <div style="font-size:12px;color:rgba(255,255,255,0.55);line-height:1.55">El core actual presenta limitaciones para administrar el crédito estructurado complejo. Parte de la reportería regulatoria requiere procesos manuales y no existe una integración generalizada con los sistemas ERP de los clientes.</div>
      </div>
    </div>
  </div>
</section>

<!-- ── CAPACIDADES TRANSVERSALES ─────────────────── -->
<section class="section" id="capacidades">
  <div class="eyebrow">Capacidades habilitadoras</div>
  <h2 class="sec-title">La evolución de los tres segmentos depende de capacidades comunes</h2>
  <p class="sec-lead">El diagnóstico identificó capacidades regulatorias, operativas, tecnológicas y de información que deben atenderse de forma común. Su configuración podrá variar por segmento, producto y nivel de complejidad.</p>

  <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-bottom:32px">
    <div class="card gold">
      <div class="card-label">Capacidad 1</div>
      <div class="card-title">Cumplimiento regulatorio</div>
      <div class="card-body">KYC/CDD desde el onboarding y en actualizaciones periódicas. Buró de crédito, listas negras (OFAC, CNBV), buró legal y propietario real. Reportes a CNBV, Banxico, SIC e IPAB diferenciados por tipo de producto. Cálculo de reservas por producto y parámetros de riesgo.</div>
      <div class="card-tag">CNBV · PLD · Banxico · IPAB</div>
    </div>
    <div class="card navy">
      <div class="card-label">Capacidad 2</div>
      <div class="card-title">Reglas de negocio</div>
      <div class="card-body">Motor de reglas centralizado que cubra elegibilidad, condiciones de producto, límites de autorización y flujos de aprobación. Debe permitir configurar reglas por segmento y producto sin intervención de TI para ajustes de parámetros. Vinculación con rentabilidad individual y de portafolio.</div>
      <div class="card-tag">Motor de reglas · Parametrización · Rentabilidad</div>
    </div>
    <div class="card teal">
      <div class="card-label">Capacidad 3</div>
      <div class="card-title">Seguridad</div>
      <div class="card-body">CVV dinámico y doble factor para banca digital. Control de acceso por usuario con atributos diferenciados dentro del cliente. Auditoría de cambios en sistemas con notificación a todas las áreas afectadas. Estándares de ciberseguridad en aplicaciones transaccionales.</div>
      <div class="card-tag">Autenticación · Control de acceso · Auditoría</div>
    </div>
    <div class="card gold">
      <div class="card-label">Capacidad 4</div>
      <div class="card-title">Capacidades operativas</div>
      <div class="card-body">Capacidad de core bancario que permita administrar de manera consistente los productos, operaciones e información requeridos por los segmentos. Automatización de procesos que permita escalar sin incrementar la plantilla. Incorporación de inteligencia artificial en los procesos que lo permitan, con cumplimiento regulatorio. Banca digital funcional para el cliente empresarial.</div>
      <div class="card-tag">Core · IA · Automatización · Escalabilidad</div>
    </div>
    <div class="card navy">
      <div class="card-label">Capacidad 5</div>
      <div class="card-title">Monitoreo y control</div>
      <div class="card-body">Flujo de actualización de expediente e información financiera en tiempo y forma. Conexiones con sistemas de PLD, prevención de fraudes y sanciones. Información en tiempo real para monitoreo de cartera. Integración con ERP del cliente para registro contable correcto.</div>
      <div class="card-tag">Tiempo real · PLD · ERP · Cartera</div>
    </div>
    <div class="card green">
      <div class="card-label">Prioridad transversal</div>
      <div class="card-title">Visión 360 del cliente</div>
      <div class="card-body">Sistema interno único donde las diferentes áreas visualicen la misma información del cliente, con el detalle apropiado a sus funciones. Vinculación entre productos para generar una relación integral y una propuesta de valor diferenciada por cliente.</div>
      <div class="card-tag">Cliente único · Visión integral · Ecosistema</div>
    </div>
  </div>
</section>

<!-- ── MERCADO ─────────────────────────────────────── -->
<section class="section light" id="mercado">
  <div class="eyebrow">Contexto de mercado</div>
  <h2 class="sec-title">La evolución del mercado eleva el estándar de servicio para la banca empresarial</h2>
  <p class="sec-lead">Las tendencias incluidas en el diagnóstico muestran una mayor adopción de modelos digitales, decisiones basadas en datos y modernización de plataformas bancarias. Este contexto incrementa las expectativas de velocidad, autonomía y disponibilidad de información de los clientes empresariales.</p>

  <div class="mercado-grid">
    <div class="mercado-card">
      <!-- VALIDAR FUENTE --><div class="mercado-stat">+20%</div>
      <div class="mercado-title">Crecimiento en originación de crédito PyME en banca tradicional, 2026</div>
      <div class="mercado-body">Instituciones del sector reportaron mayor dinamismo en la colocación de crédito a PyMEs, con el apoyo de garantías de segundo piso para clientes sin historial crediticio formal. La competencia cuenta con capacidades y niveles de escala que elevan el estándar del segmento.</div>
    </div>
    <div class="mercado-card">
      <!-- VALIDAR FUENTE --><div class="mercado-stat">40%</div>
      <div class="mercado-title">Mayor permanencia en PyMEs con herramientas digitales</div>
      <div class="mercado-body">Estudios del sector indican que las PyMEs que adoptaron financiamiento flexible y gestión digital presentaron mayores índices de permanencia que las que operaron en esquemas tradicionales. La adopción de herramientas digitales se relaciona con una mayor capacidad de adaptación de las empresas.</div>
    </div>
    <div class="mercado-card">
      <!-- VALIDAR FUENTE --><div class="mercado-stat">37.7%</div>
      <div class="mercado-title">Crecimiento anual del crédito digital en el segmento empresarial en México</div>
      <div class="mercado-body">El crédito B2B integrado, automatizado y basado en datos de operación real (CFDI, SPEI) crece 37.7% interanual. El nearshoring acelera la necesidad de capital de trabajo flexible para redes de proveedores.</div>
    </div>
    <div class="mercado-card">
      <div class="mercado-stat">30%</div>
      <div class="mercado-title">Incremento en eficiencia operativa bancaria con IA</div>
      <div class="mercado-body">BCG y Capgemini estiman que la banca es la industria con mayor potencial de productividad con IA generativa. Organizaciones con IA en cumplimiento reportan ahorros anuales superiores a 1 millón de dólares.</div>
    </div>
    <div class="mercado-card">
      <div class="mercado-stat">4/10</div>
      <div class="mercado-title">Clientes que cambiaron de banco en el último año</div>
      <div class="mercado-body">Casi 4 de cada 10 clientes que cambiaron de institución financiera en 2025 lo hicieron por razones relacionadas con experiencia digital. La experiencia digital influye de manera creciente en la permanencia y movilidad de los clientes.</div>
    </div>
    <div class="mercado-card">
      <div class="mercado-stat">2026</div>
      <div class="mercado-title">Core bancario como decisión estratégica, no técnica</div>
      <div class="mercado-body">BCG en CORETIC 2026: la modernización del core bancario dejó de ser un desafío tecnológico para convertirse en una decisión estratégica. Las plataformas heredadas enfrentan limitaciones para responder a servicios digitales y procesamiento en tiempo real.</div>
    </div>
  </div>
</section>

<!-- ── OPORTUNIDADES ──────────────────────────────── -->
<section class="section" id="oportunidades">
  <div class="eyebrow">Agenda estratégica</div>
  <h2 class="sec-title">El diagnóstico plantea una secuencia de tres capacidades prioritarias</h2>
  <p class="sec-lead">Las prioridades identificadas mantienen una relación de dependencia. La digitalización del ciclo de vida genera la información necesaria para fortalecer la decisión de crédito y, posteriormente, integrar una oferta más amplia para el cliente empresarial.</p>

  <div class="opor-grid">
    <div class="opor-card navy">
      <div class="opor-tag">Prioridad 01</div>
      <div class="opor-title">Digitalizar el ciclo de vida</div>
      <div class="opor-body">La originación, las validaciones de conocimiento del cliente, la evaluación, la formalización y la operación requieren una mayor integración digital. Esta capacidad es necesaria para reducir tiempos de respuesta, mejorar la trazabilidad y escalar el modelo operativo.</div>
    </div>
    <div class="opor-card teal">
      <div class="opor-tag">Prioridad 02</div>
      <div class="opor-title">Fortalecer la decisión paramétrica</div>
      <div class="opor-body">El desarrollo de modelos de evaluación basados en información financiera, comportamiento previo y datos alternativos permitiría diferenciar las solicitudes que pueden resolverse mediante reglas de aquellas que requieren análisis especializado o comité.</div>
    </div>
    <div class="opor-card gold">
      <div class="opor-tag">Prioridad 03</div>
      <div class="opor-title">Integrar la relación con el cliente empresarial</div>
      <div class="opor-body">La conexión entre crédito, captación, dispersión, tesorería y banca digital permitiría ofrecer una visión consolidada del cliente y desarrollar una relación de mayor alcance, con impacto en la retención y el valor de la relación con el cliente.</div>
    </div>
  </div>

  <div style="margin-top:32px">
    <div class="hallazgo-box">
      <div class="hallazgo-label">Secuencia recomendada</div>
      <div class="hallazgo-text">La digitalización del ciclo de vida permite generar información estructurada y trazable. Sobre esta base puede desarrollarse la evaluación paramétrica y, posteriormente, una oferta integrada para el cliente empresarial. La secuencia reduce dependencias y facilita una implementación progresiva.</div>
    </div>
  </div>

  <div class="divider">
    <div class="div-line"></div>
    <div class="div-label">Cierre ejecutivo</div>
    <div class="div-line"></div>
  </div>

  <div class="cierre-box">
    <div class="cierre-quote">
      El diagnóstico confirma que los tres segmentos comparten una base común de necesidades, pero requieren distintos niveles de configuración, análisis y servicio. La siguiente etapa consiste en definir el modelo operativo por etapa, las capacidades tecnológicas y de información necesarias, así como una secuencia de implementación alineada con la Planeación Estratégica 2027-2031.
    </div>
    <div class="cierre-steps">
      <div class="cierre-step">
        <div class="cierre-step-label">Conclusiones confirmadas</div>
        <div class="cierre-step-text">Los tres segmentos comparten necesidades estructurales y requieren capacidades comunes, con distintos niveles de configuración y complejidad por segmento.</div>
      </div>
      <div class="cierre-step">
        <div class="cierre-step-label">Siguiente etapa</div>
        <div class="cierre-step-text">Definir el modelo operativo detallado por etapa, las capacidades del core bancario requeridas, la arquitectura de datos y la hoja de ruta de implementación por segmento.</div>
      </div>
      <div class="cierre-step">
        <div class="cierre-step-label">Decisiones requeridas</div>
        <div class="cierre-step-text">Construir hacia 2031 una Banca Mayorista con identidad, P&L y modelo operativo propios capaz de competir en velocidad, personalización y experiencia de cliente.</div>
      </div>
    </div>
  </div>
</section>

<!-- ── CHALLENGE DEL DIRECTOR ─────────────────────── -->
<section class="challenge-section" id="challenge">
  <div class="eyebrow light-eye">Síntesis para la toma de decisiones</div>
  <h2 class="sec-title white" style="margin-bottom:10px">El diagnóstico permite precisar el punto de partida, el modelo futuro y las capacidades disponibles</h2>
  <p class="sec-lead white" style="margin-bottom:36px">La síntesis reúne la situación actual identificada, las características del modelo futuro y los activos o capacidades que pueden habilitar su evolución. Su propósito es facilitar la definición de prioridades y decisiones posteriores.</p>

  <div class="challenge-grid-top">
    <div class="challenge-col" style="background:rgba(27,53,93,0.6)">
      <div class="challenge-col-header">01</div>
      <div class="challenge-col-title">Situación actual</div>
      <div class="challenge-item"><div class="challenge-dot"></div><div class="challenge-item-text">Una Banca Mayorista con cartera real y clientes activos, pero sin un modelo operativo diseñado específicamente para el segmento empresarial</div></div>
      <div class="challenge-item"><div class="challenge-dot"></div><div class="challenge-item-text">Tres segmentos que operan con lógicas distintas: PyME, Crédito Comercial y Banca de Gobierno sin una plataforma que los unifique</div></div>
      <div class="challenge-item"><div class="challenge-dot"></div><div class="challenge-item-text">Evaluación de crédito manual para la gran mayoría de los casos, sin modelo paramétrico ni aprovechamiento de datos alternativos</div></div>
      <div class="challenge-item"><div class="challenge-dot"></div><div class="challenge-item-text">Onboarding y formalización con dependencias presenciales que limitan la velocidad y la escala de la operación</div></div>
      <div class="challenge-item"><div class="challenge-dot"></div><div class="challenge-item-text">Core bancario con capacidades insuficientes para la complejidad del crédito comercial estructurado</div></div>
    </div>
    <div class="challenge-col" style="background:rgba(27,53,93,0.4)">
      <div class="challenge-col-header">02</div>
      <div class="challenge-col-title">Modelo futuro</div>
      <div class="challenge-item"><div class="challenge-dot teal"></div><div class="challenge-item-text">Una Banca Mayorista con identidad propia, P&amp;L diferenciado y modelo operativo diseñado para servir a empresas e instituciones desde la digitalización</div></div>
      <div class="challenge-item"><div class="challenge-dot teal"></div><div class="challenge-item-text">Plataforma única compartida entre los tres segmentos, con parametrización por tipo de cliente y nivel de complejidad</div></div>
      <div class="challenge-item"><div class="challenge-dot teal"></div><div class="challenge-item-text">Evaluación de crédito con ruta paramétrica y ruta de comité: las dos operando sobre los mismos datos y controles automatizados</div></div>
      <div class="challenge-item"><div class="challenge-dot teal"></div><div class="challenge-item-text">Ciclo de vida completamente digital: desde el primer contacto con el cliente hasta la operación y administración del portafolio</div></div>
      <div class="challenge-item"><div class="challenge-dot teal"></div><div class="challenge-item-text">Ecosistema financiero que genera retención y crecimiento del valor del cliente: crédito, captación, dispersión y banca digital integrados en una sola relación</div></div>
    </div>
    <div class="challenge-col" style="background:rgba(27,53,93,0.25)">
      <div class="challenge-col-header">03</div>
      <div class="challenge-col-title">Capacidades y activos disponibles</div>
      <div class="challenge-item"><div class="challenge-dot green"></div><div class="challenge-item-text">Cartera activa en los tres segmentos y conocimiento real del mercado objetivo: PyMEs medianas con potencial de largo plazo</div></div>
      <div class="challenge-item"><div class="challenge-dot green"></div><!-- VALIDAR CONTENIDO: esta afirmación requiere confirmación del equipo --><div class="challenge-item-text">Infraestructura de pagos: SPEI, CoDi y dispersión activos en el sistema financiero mexicano</div></div>
      <div class="challenge-item"><div class="challenge-dot green"></div><div class="challenge-item-text">Líderes de negocio que entienden la oportunidad y participaron activamente en construir la visión futura durante el levantamiento</div></div>
      <div class="challenge-item"><div class="challenge-dot green"></div><!-- VALIDAR CONTENIDO: esta afirmación requiere confirmación del equipo --><div class="challenge-item-text">Posibilidad de avanzar con mayor agilidad hacia un modelo mayorista especializado, en función de la escala y la estructura actual del banco</div></div>
      <div class="challenge-item"><div class="challenge-dot green"></div><div class="challenge-item-text">Planeación Estratégica 2027–2031 ya posiciona a la Banca Mayorista como motor de crecimiento y diversificación de ingresos</div></div>
    </div>
  </div>

  <!-- Brechas críticas -->
  <div style="margin-top:20px;margin-bottom:4px">
    <div style="font-size:11px;font-weight:700;letter-spacing:.12em;text-transform:uppercase;color:rgba(255,255,255,0.4);margin-bottom:12px;padding:0 4px">Brechas que la dirección debe resolver</div>
  </div>
  <div class="challenge-gap-row">
    <div class="challenge-gap-col">
      <div class="challenge-gap-label">Brecha de capacidad de decisión</div>
      <div class="challenge-gap-item">Sin modelo paramétrico, el banco no puede escalar la colocación sin escalar el equipo de análisis</div>
      <div class="challenge-gap-item">Los datos alternativos (CIEC, SPEI, CFDI) no se están usando en la evaluación de riesgo</div>
      <!-- VALIDAR CONTENIDO: esta afirmación requiere confirmación del equipo --><div class="challenge-gap-item">Los tiempos de resolución actuales pueden representar una desventaja frente a competidores con modelos más ágiles</div>
    </div>
    <div class="challenge-gap-col">
      <div class="challenge-gap-label">Brecha de plataforma y core</div>
      <div class="challenge-gap-item">El core actual no soporta la complejidad del crédito estructurado: disposiciones múltiples, garantías cruzadas, devengamiento diferenciado</div>
      <div class="challenge-gap-item">No existe visión 360 del cliente compartida entre sistemas y áreas</div>
      <div class="challenge-gap-item">La banca digital empresarial no tiene las herramientas de autonomía transaccional que el segmento requiere</div>
    </div>
    <div class="challenge-gap-col">
      <div class="challenge-gap-label">Brecha de experiencia del cliente</div>
      <div class="challenge-gap-item">El onboarding no está digitalizado de extremo a extremo: el cliente percibe lentitud desde el primer contacto</div>
      <div class="challenge-gap-item">Formalización post-aprobación con dependencias presenciales que no son competitivas</div>
      <div class="challenge-gap-item">El cliente empresarial no tiene visibilidad de su portafolio completo desde un solo lugar</div>
    </div>
  </div>

  <!-- Las 3 preguntas que el director debe responder -->
  <div class="pregunta-dir">
    <div class="pregunta-dir-label">Decisiones que deberán abordarse en la siguiente etapa</div>
    <div class="pregunta-grid">
      <div class="pregunta-card">
        <div class="pregunta-num">01</div>
        <div class="pregunta-text">Ritmo y horizonte de implementación</div>
        <div class="pregunta-sub">Definir la velocidad de avance y los hitos necesarios para desarrollar las capacidades identificadas.</div>
      </div>
      <div class="pregunta-card">
        <div class="pregunta-num">02</div>
        <div class="pregunta-text">Estrategia de evolución del core</div>
        <div class="pregunta-sub">Evaluar las alternativas de modernización, evolución o incorporación de capas complementarias, considerando impacto, dependencias y tiempo de implementación.</div>
      </div>
      <div class="pregunta-card">
        <div class="pregunta-num">03</div>
        <div class="pregunta-text">Secuencia de atención por segmento</div>
        <div class="pregunta-sub">Establecer criterios de priorización por segmento con base en valor esperado, complejidad, riesgo, capacidades disponibles y alineación con la Planeación Estratégica 2027-2031.</div>
      </div>
    </div>
  </div>
</section>


<footer class="footer">
  <div class="footer-brand">Consubanco · Banca Mayorista</div>
  <div class="footer-meta">Diagnóstico Estratégico · Levantamiento de Necesidades y Capacidades · Soluciones de Negocio 2026</div>
</footer>

<script>
// Progress bar
window.addEventListener('scroll',function(){
  var h=document.documentElement,b=document.body;
  var pct=(h.scrollTop||b.scrollTop)/(h.scrollHeight-h.clientHeight)*100;
  document.getElementById('pbar').style.width=pct+'%';
});
// Nav active
var sections=document.querySelectorAll('section[id]');
var navLinks=document.querySelectorAll('.nav a');
var io=new IntersectionObserver(function(entries){
  entries.forEach(function(e){
    if(e.isIntersecting){
      navLinks.forEach(function(a){
        a.style.color='';a.style.borderBottomColor='';
      });
      var match=document.querySelector('.nav a[href="#'+e.target.id+'"]');
      if(match){match.style.color='rgba(255,255,255,.95)';match.style.borderBottomColor='rgba(231,83,1,.7)';}
    }
  });
},{threshold:0.4});
sections.forEach(function(s){io.observe(s);});
</script>
</body>
</html>
rategico_Banca_Mayorista_Consubanco_v1-0-4.html…]()
