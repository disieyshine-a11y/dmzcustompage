[index.html](https://github.com/user-attachments/files/34413220/index.html)
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="DMZ Custom — bengkel spesialis repaint, restorasi, custom paint dan airbrush motor di Yogyakarta.">
<title>DMZ Custom — Motorcycle Paint & Restoration</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Inter:wght@400;500;600;700;800&family=Playfair+Display:ital,wght@0,600;0,700;1,600;1,700&display=swap');

:root{
  --bg:#050605; --panel:rgba(18,21,16,.72); --line:rgba(202,255,45,.16);
  --lime:#c8ff38; --lime2:#9fdc22; --text:#f2f3ed; --muted:#9da397;
  --max:1240px;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--text);font-family:Inter,system-ui,sans-serif;overflow-x:hidden}
a{text-decoration:none;color:inherit}
button{font:inherit}
body:before{
 content:"";position:fixed;inset:-30%;z-index:-4;
 background:radial-gradient(circle at 50% 42%,rgba(188,255,35,.20),transparent 22%),
            radial-gradient(circle at 18% 65%,rgba(125,170,40,.10),transparent 24%),
            radial-gradient(circle at 85% 25%,rgba(255,255,255,.035),transparent 20%);
 filter:blur(30px);animation:ambient 9s ease-in-out infinite alternate;
}
@keyframes ambient{from{transform:scale(.95) translate3d(-1%,0,0)}to{transform:scale(1.07) translate3d(1%,-1%,0)}}
.noise{position:fixed;inset:0;pointer-events:none;z-index:20;opacity:.035;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.55'/%3E%3C/svg%3E")}
.container{width:min(var(--max),calc(100% - 48px));margin:auto}
nav{height:78px;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid rgba(255,255,255,.07);position:relative;z-index:10}
.brand{display:flex;align-items:center;gap:11px;font-weight:800;letter-spacing:-.04em}
.brand-mark{width:30px;height:30px;border:2px solid var(--lime);border-radius:8px;display:grid;place-items:center;color:var(--lime);font-size:12px;font-weight:900;box-shadow:0 0 24px rgba(200,255,56,.16)}
.brand span{font-size:16px}
.navlinks{display:flex;gap:31px;color:#858a80;font-size:13px}
.navlinks a{transition:.2s}.navlinks a:hover{color:var(--text)}
.nav-actions{display:flex;gap:8px;align-items:center;flex-wrap:wrap}
.btn{border:1px solid rgba(255,255,255,.12);background:rgba(255,255,255,.03);color:var(--text);padding:12px 18px;border-radius:999px;font-size:13px;font-weight:700;cursor:pointer;transition:.25s}
.btn:hover{transform:translateY(-2px);border-color:rgba(200,255,56,.45)}
.btn.primary{background:var(--lime);border-color:var(--lime);color:#0b0d07;box-shadow:0 0 35px rgba(200,255,56,.18)}
.btn.primary:hover{box-shadow:0 0 45px rgba(200,255,56,.34)}
.hero{min-height:690px;display:grid;grid-template-columns:1fr;align-items:center;text-align:center;position:relative;padding:80px 0 120px}
.eyebrow{font-family:"DM Mono",monospace;font-size:11px;color:var(--lime);letter-spacing:.18em;text-transform:uppercase;margin-bottom:25px}
.hero h1{font-family:"Playfair Display",serif;font-size:clamp(58px,9vw,128px);line-height:.86;letter-spacing:-.075em;font-weight:600;max-width:1000px;margin:0 auto}
.hero h1 em{color:var(--lime);font-weight:600}
.hero p{max-width:590px;margin:30px auto 0;color:#a5aaa0;font-size:14px;line-height:1.8}
.cta{margin-top:30px;display:flex;justify-content:center;gap:12px;flex-wrap:wrap}
.hero-grid{position:absolute;inset:auto 0 35px;display:grid;grid-template-columns:1fr 1.4fr 1fr;gap:20px;pointer-events:none}
.metric{color:#8e938a;text-align:left;font-family:"DM Mono",monospace;font-size:10px;letter-spacing:.1em}
.metric strong{display:block;font-family:Inter;font-size:34px;letter-spacing:-.05em;color:var(--text);margin-bottom:3px}
.metric:nth-child(2){text-align:center}.metric:nth-child(3){text-align:right}
.lime-line{height:1px;background:linear-gradient(90deg,transparent,var(--lime),transparent);opacity:.5;margin:0 auto;max-width:580px}
section{padding:100px 0;position:relative}
.section-head{display:flex;justify-content:space-between;align-items:end;gap:30px;margin-bottom:38px}
.kicker{color:var(--lime);font-family:"DM Mono",monospace;font-size:10px;letter-spacing:.16em;text-transform:uppercase;margin-bottom:13px}
h2{font-family:"Playfair Display",serif;font-size:clamp(42px,6vw,76px);line-height:.95;letter-spacing:-.06em;font-weight:600}
.section-copy{max-width:440px;color:var(--muted);line-height:1.75;font-size:13px}
.glass{background:linear-gradient(135deg,rgba(23,27,19,.76),rgba(9,11,9,.55));border:1px solid var(--line);border-radius:25px;backdrop-filter:blur(22px);box-shadow:0 30px 100px rgba(0,0,0,.25)}
.services{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:18px;align-items:stretch}
.service{padding:30px;min-height:280px;display:flex;flex-direction:column;position:relative;overflow:hidden;transition:.35s}
.service:hover{transform:translateY(-6px);border-color:rgba(200,255,56,.4)}
.service:after{content:"";position:absolute;width:180px;height:180px;border-radius:50%;right:-70px;bottom:-90px;background:rgba(200,255,56,.12);filter:blur(25px)}
.num{font-family:"DM Mono";font-size:10px;color:var(--lime)}
.service h3{font-size:22px;margin:42px 0 10px;letter-spacing:-.04em}
.service p{color:var(--muted);font-size:13px;line-height:1.7;max-width:430px}
.tags{display:flex;flex-wrap:wrap;gap:7px;margin-top:18px}
.tag{font-size:10px;color:#aeb5a5;border:1px solid rgba(255,255,255,.1);border-radius:999px;padding:7px 10px}
.process{display:grid;grid-template-columns:repeat(6,1fr);gap:10px}
.step{padding:22px 18px;min-height:160px}
.step b{font-family:"DM Mono";font-size:10px;color:var(--lime)}
.step h4{margin:28px 0 8px;font-size:14px}
.step p{font-size:11px;color:var(--muted);line-height:1.6}
.quality{display:grid;grid-template-columns:1.15fr .85fr;gap:18px}
.big-card{padding:44px;min-height:390px;position:relative;overflow:hidden}
.big-card h3{font-family:"Playfair Display";font-size:58px;line-height:.95;letter-spacing:-.06em;max-width:550px}
.big-card h3 em{color:var(--lime)}
.big-card p{color:var(--muted);line-height:1.8;font-size:13px;max-width:540px;margin-top:25px}
.specs{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:30px}
.spec{padding:18px;border:1px solid rgba(255,255,255,.08);border-radius:15px;background:rgba(255,255,255,.02)}
.spec span{display:block;color:var(--muted);font-size:10px}.spec strong{display:block;margin-top:7px;font-size:13px}
.side{display:grid;gap:10px}
.side .glass{padding:28px;min-height:120px}
.side h4{font-size:13px}.side p{font-size:11px;color:var(--muted);margin-top:7px;line-height:1.6}
.about{display:grid;grid-template-columns:.8fr 1.2fr;gap:60px;align-items:start}
.about p{color:var(--muted);font-size:14px;line-height:1.9}
.checks{margin-top:26px;display:grid;gap:12px}
.check{display:flex;gap:10px;color:#c7cbc2;font-size:12px}.check i{width:17px;height:17px;border-radius:50%;background:rgba(200,255,56,.14);border:1px solid rgba(200,255,56,.5);color:var(--lime);display:grid;place-items:center;font-style:normal;font-size:9px}
.contact{display:grid;grid-template-columns:1fr .8fr;gap:15px}
.contact-main{padding:45px}.contact-main h2{max-width:700px}.contact-main p{color:var(--muted);line-height:1.8;font-size:13px;margin:25px 0}
.contact-info{display:grid;gap:10px}
.info{padding:24px}.info small{font-family:"DM Mono";color:var(--lime);font-size:9px}.info div{margin-top:8px;font-size:14px}.info a{color:var(--text)}
footer{border-top:1px solid rgba(255,255,255,.07);padding:30px 0;color:#777c73;font-size:11px;display:flex;justify-content:space-between;gap:20px}
.reveal{opacity:0;transform:translateY(25px);transition:opacity .8s ease,transform .8s ease}.reveal.visible{opacity:1;transform:none}
.float{position:fixed;right:22px;bottom:22px;z-index:15;background:var(--lime);color:#0a0d06;border-radius:999px;padding:14px 19px;font-size:12px;font-weight:800;box-shadow:0 10px 40px rgba(200,255,56,.25);animation:pulse 2.8s infinite}
@keyframes pulse{0%,100%{box-shadow:0 10px 40px rgba(200,255,56,.18)}50%{box-shadow:0 10px 55px rgba(200,255,56,.42)}}
.cursor{position:fixed;width:320px;height:320px;border-radius:50%;background:rgba(200,255,56,.06);filter:blur(45px);pointer-events:none;z-index:-1;transform:translate(-50%,-50%)}
@media(max-width:900px){
 .navlinks{display:none}.hero-grid{grid-template-columns:1fr 1fr}.metric:nth-child(2){display:none}
 .services,.quality,.about,.contact{grid-template-columns:1fr}.process{grid-template-columns:repeat(2,1fr)}
 .big-card{min-height:auto}.section-head{display:block}.section-copy{margin-top:20px}
}
@media(max-width:560px){
 .container{width:min(100% - 28px,var(--max))}.hero{padding:55px 0 120px;min-height:620px}.hero h1{font-size:56px}
 section{padding:72px 0}.services{grid-template-columns:1fr}.process{grid-template-columns:1fr 1fr}
 .metric strong{font-size:26px}.metric{font-size:8px}.contact-main{padding:28px}.big-card{padding:28px}.big-card h3{font-size:45px}
 footer{display:block}.float{right:14px;bottom:14px}
}
.social-strip{margin:0 0 34px;padding:22px 25px;border:1px solid rgba(200,255,56,.14);border-radius:20px;background:rgba(15,18,13,.58);display:flex;justify-content:space-between;align-items:center;gap:20px}.social-strip span{display:block;font-family:"DM Mono";font-size:9px;letter-spacing:.16em;color:var(--lime);margin-bottom:7px}.social-strip strong{font-size:13px;letter-spacing:-.02em}.social-links{display:flex;gap:9px;flex-wrap:wrap;justify-content:flex-end}.social-links a{border:1px solid rgba(255,255,255,.09);padding:10px 13px;border-radius:999px;font-size:10px;color:#aeb4a9;transition:.2s}.social-links a:hover{border-color:rgba(200,255,56,.4);color:var(--text);transform:translateY(-2px)}.social-links b{color:var(--text);font-weight:600;margin-left:4px}@media(max-width:560px){.nav-actions .btn{padding:9px 12px;font-size:11px}.nav-actions .btn.primary{display:none}.social-strip{display:block}.social-links{justify-content:flex-start;margin-top:16px}}</style>
</head>
<body>
<div class="noise"></div><div class="cursor" id="cursor"></div>

<div class="container">
<nav>
  <a href="#" class="brand"><span class="brand-mark">D</span><span>DMZ <span style="color:var(--lime)">CUSTOM</span></span></a>
  <div class="navlinks">
    <a href="#services">Layanan</a><a href="#process">SOP</a><a href="#quality">Standar</a><a href="#about">Tentang</a>
  </div>
  <div class="nav-actions"><a class="btn" href="https://instagram.com/dmzcustom" target="_blank">Instagram</a><a class="btn" href="https://www.tiktok.com/@dmzcustomgarage" target="_blank">TikTok</a><a class="btn primary" href="https://wa.me/6288896527794" target="_blank">Konsultasi</a></div>
</nav>

<header class="hero">
  <div>
    <div class="eyebrow">Motorcycle paint · restoration · custom</div>
    <h1>Build a bike that<br><em>looks unforgettable.</em></h1>
    <p>DMZ Custom adalah bengkel spesialis pengecatan, restorasi dan custom motor di Yogyakarta. Kami menggabungkan proses yang rapi, material yang tepat, dan finishing yang dibuat untuk bertahan.</p>
    <div class="cta"><a class="btn primary" href="https://wa.me/6288896527794" target="_blank">Mulai Konsultasi ↗</a><a class="btn" href="#services">Lihat Layanan</a></div>
  </div>
  <div class="hero-grid">
    <div class="metric"><strong>24H</strong>WORKSHOP</div>
    <div class="metric"><strong>PRO</strong>PAINT PROCESS</div>
    <div class="metric"><strong>YOGYAKARTA</strong>IMOGIRI TIMUR KM7</div>
  </div>
</header>
<div class="lime-line"></div>

<section id="services" class="reveal">
  <div class="section-head"><div><div class="kicker">01 / Services</div><h2>Make it <em style="color:var(--lime)">yours.</em></h2></div>
  <p class="section-copy">Mulai dari repaint standar pabrikan sampai custom airbrush dan restorasi total. Setiap pekerjaan disesuaikan dengan kondisi motor, kebutuhan, dan budget.</p></div>
  <div class="services">
    <article class="glass service"><div class="num">01 — BODY REPAINT</div><h3>Premium Body Repaint</h3><p>Stripping, epoxy, base coat dan top coat dengan pilihan finishing Super Glossy atau Doff/Matte.</p><div class="tags"><span class="tag">OEM Look</span><span class="tag">Glossy</span><span class="tag">Matte</span></div></article>
    <article class="glass service"><div class="num">02 — WHEELS</div><h3>Spesialis Cat Velg</h3><p>Material khusus untuk menghadapi panas mesin dan debu rem. Pilihan solid, candy, magnesium look hingga chrome effect.</p><div class="tags"><span class="tag">Solid</span><span class="tag">Candy</span><span class="tag">Chrome Effect</span></div></article>
    <article class="glass service"><div class="num">03 — RESTORATION</div><h3>Restorasi Total & Detailing</h3><p>Mengembalikan motor lama menuju tampilan New Old Stock melalui frame, exterior refresh, detailing dan penataan look.</p><div class="tags"><span class="tag">Frame</span><span class="tag">Detailing</span><span class="tag">NOS Look</span></div></article>
    <article class="glass service"><div class="num">04 — ARTWORK</div><h3>Custom Paint & Airbrush</h3><p>Pinstriping manual, motif grafis minimalis dan racing look untuk motor yang ingin punya identitas visual sendiri.</p><div class="tags"><span class="tag">Pinstriping</span><span class="tag">Racing</span><span class="tag">Custom</span></div></article>
  </div>
</section>

<section id="quality" class="reveal">
  <div class="section-head"><div><div class="kicker">02 / Quality System</div><h2>Detail is the<br><em style="color:var(--lime)">difference.</em></h2></div>
  <p class="section-copy">Kami tidak hanya mengejar warna yang bagus. Persiapan permukaan, material, teknik semprot dan quality control menentukan umur hasil akhir.</p></div>
  <div class="quality">
    <div class="glass big-card"><div class="kicker">DMZ STANDARD</div><h3>Clean process.<br><em>Better finish.</em></h3><p>Material cat PU dan NC disesuaikan dengan kebutuhan dan budget. High Gloss Clear Coat dengan pelindung UV digunakan untuk membantu menjaga warna dan kilap.</p>
      <div class="specs"><div class="spec"><span>CLEAR COAT</span><strong>High Gloss + UV</strong></div><div class="spec"><span>BASE</span><strong>Epoxy Preparation</strong></div><div class="spec"><span>FINISH</span><strong>Gloss / Matte</strong></div></div>
    </div>
    <div class="side"><div class="glass"><h4>Material Selection</h4><p>PU / NC menyesuaikan karakter pekerjaan, request dan budget customer.</p></div><div class="glass"><h4>Dust Control</h4><p>Painting dilakukan di ruang tertutup dengan kondisi yang dibuat minim debu dan kontaminasi.</p></div><div class="glass"><h4>Final Inspection</h4><p>QC mengecek bintik, leleh, coverage dan kualitas finishing sebelum motor diserahkan.</p></div></div>
  </div>
</section>

<section id="process" class="reveal">
  <div class="section-head"><div><div class="kicker">03 / Workflow</div><h2>From rough<br>to <em style="color:var(--lime)">refined.</em></h2></div>
  <p class="section-copy">Alur pengerjaan dibuat jelas agar customer mengetahui apa yang terjadi pada motornya dari awal sampai finishing.</p></div>
  <div class="process">
    <div class="glass step"><b>01</b><h4>Konsultasi</h4><p>Konsep, warna, kondisi motor dan estimasi biaya.</p></div>
    <div class="glass step"><b>02</b><h4>Bongkar & Cleaning</h4><p>Part dibongkar dan dibersihkan sebelum proses.</p></div>
    <div class="glass step"><b>03</b><h4>Surface Prep</h4><p>Amplas dan dempul halus untuk permukaan rata.</p></div>
    <div class="glass step"><b>04</b><h4>Painting</h4><p>Proses pengecatan di ruang tertutup minim debu.</p></div>
    <div class="glass step"><b>05</b><h4>Quality Control</h4><p>Inspeksi cacat, coverage dan kualitas permukaan.</p></div>
    <div class="glass step"><b>06</b><h4>Finishing</h4><p>Poles akhir untuk kilap maksimal sesuai request.</p></div>
  </div>
</section>

<section id="about" class="reveal">
 <div class="about"><div><div class="kicker">04 / About DMZ</div><h2>Born from<br><em style="color:var(--lime)">obsession.</em></h2></div>
 <div><p>DMZ Custom berawal dari hobi terhadap dunia otomotif dan berkembang menjadi bengkel yang membantu owner motor mendapatkan tampilan yang maksimal, rapi, dan punya karakter. Kami mengombinasikan skill, material yang sesuai dan proses pengecatan yang terstruktur.</p>
 <div class="checks"><div class="check"><i>✓</i><span>Edukasi material pengecatan yang tepat</span></div><div class="check"><i>✓</i><span>SOP dari pengamplasan hingga finishing</span></div><div class="check"><i>✓</i><span>Menjaga ketepatan waktu sesuai kesepakatan</span></div></div></div></div>
</section>

<section class="reveal">
 <div class="contact">
  <div class="glass contact-main"><div class="kicker">05 / Start a project</div><h2>Ready to make your bike <em style="color:var(--lime)">different?</em></h2><p>Ceritakan motor, konsep, warna, part yang ingin dikerjakan, dan target hasilnya. Tim DMZ Custom akan membantu menentukan treatment yang paling sesuai.</p><a class="btn primary" href="https://wa.me/6288896527794?text=Halo%20DMZ%20Custom,%20saya%20ingin%20konsultasi%20repaint%20motor." target="_blank">Chat WhatsApp ↗</a></div>
  <div class="contact-info"><div class="glass info"><small>WORKSHOP</small><div>Jl. Imogiri Timur KM7<br>Bantul, Yogyakarta</div></div><div class="glass info"><small>INSTAGRAM</small><div><a href="https://instagram.com/dmzcustom" target="_blank">@dmzcustom ↗</a></div></div><div class="glass info"><small>TIKTOK</small><div><a href="https://www.tiktok.com/@dmzcustomgarage" target="_blank">@dmzcustomgarage ↗</a></div></div><div class="glass info"><small>OPEN</small><div>Senin — Sabtu · 24 Jam</div></div></div>
 </div>
</section>

<div class="social-strip"><div><span>FOLLOW DMZ CUSTOM</span><strong>Build. Paint. Restore.</strong></div><div class="social-links"><a href="https://instagram.com/dmzcustom" target="_blank">Instagram <b>@dmzcustom</b> ↗</a><a href="https://www.tiktok.com/@dmzcustomgarage" target="_blank">TikTok <b>@dmzcustomgarage</b> ↗</a></div></div><footer><span>© 2026 DMZ Custom — Motorcycle Paint & Restoration</span><span>Yogyakarta · Indonesia</span></footer>
</div>
<a class="float" href="https://wa.me/6288896527794" target="_blank">WhatsApp DMZ ↗</a>
<script>
const cursor=document.getElementById('cursor');
window.addEventListener('pointermove',e=>{cursor.style.left=e.clientX+'px';cursor.style.top=e.clientY+'px'});
const obs=new IntersectionObserver(entries=>entries.forEach(e=>{if(e.isIntersecting)e.target.classList.add('visible')}),{threshold:.12});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));
</script>
</body>
</html>
