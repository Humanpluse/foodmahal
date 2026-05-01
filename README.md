<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Food Mahal — Pir Mahal</title>
<link href="https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Nunito:wght@300;400;600;700;800&family=Dancing+Script:wght@700&display=swap" rel="stylesheet"/>
<style>
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
:root{
  --red:#C0192A;
  --red-dark:#8B0F1D;
  --orange:#E8820C;
  --orange-light:#F5A623;
  --cream:#FFF8F0;
  --cream2:#FFF0DC;
  --dark:#1A0A00;
  --dark2:#2D1500;
  --mid:#6B3B1A;
  --text:#3D1C00;
  --muted:#8B6040;
  --white:#FFFFFF;
  --green:#25D366;
}
html{scroll-behavior:smooth}
body{font-family:'Nunito',sans-serif;background:var(--cream);color:var(--text);overflow-x:hidden}

/* NAVBAR */
nav{
  position:fixed;top:0;left:0;right:0;z-index:1000;
  display:flex;align-items:center;justify-content:space-between;
  padding:0.8rem 5vw;
  background:rgba(26,10,0,0.95);
  backdrop-filter:blur(10px);
  border-bottom:2px solid var(--orange);
}
.nav-brand{
  display:flex;align-items:center;gap:0.7rem;
  text-decoration:none;
}
.nav-logo-icon{
  width:42px;height:42px;border-radius:50%;
  background:var(--orange);
  display:flex;align-items:center;justify-content:center;
  font-size:1.3rem;flex-shrink:0;
}
.nav-brand-text{
  font-family:'Abril Fatface',cursive;
  font-size:1.4rem;color:var(--white);letter-spacing:0.02em;
  line-height:1;
}
.nav-brand-text span{color:var(--orange-light)}
.nav-links{display:flex;gap:1.5rem;list-style:none;align-items:center}
.nav-links a{
  font-size:0.82rem;font-weight:700;letter-spacing:0.08em;
  text-transform:uppercase;text-decoration:none;
  color:rgba(255,255,255,0.7);transition:color 0.2s;
}
.nav-links a:hover{color:var(--orange-light)}
.nav-order-btn{
  background:var(--green)!important;
  color:var(--white)!important;
  padding:0.45rem 1.1rem;
  border-radius:20px;
  font-size:0.78rem!important;
}
.hamburger{
  display:none;flex-direction:column;gap:5px;cursor:pointer;
  background:none;border:none;padding:4px;
}
.hamburger span{display:block;width:24px;height:2px;background:var(--white);border-radius:2px;transition:all 0.3s}
.mobile-menu{
  display:none;
  position:fixed;top:62px;left:0;right:0;
  background:rgba(26,10,0,0.98);
  z-index:999;padding:1.5rem 5vw 2rem;
  border-bottom:2px solid var(--orange);
}
.mobile-menu.open{display:block}
.mobile-menu a{
  display:block;padding:0.7rem 0;
  font-size:1rem;font-weight:700;letter-spacing:0.06em;
  text-transform:uppercase;text-decoration:none;
  color:rgba(255,255,255,0.8);
  border-bottom:1px solid rgba(255,255,255,0.08);
}
.mobile-menu a:hover{color:var(--orange-light)}

/* HERO */
.hero{
  min-height:100vh;
  background:var(--dark);
  display:grid;grid-template-columns:1fr 1fr;
  align-items:center;
  padding:7rem 5vw 4rem;
  gap:3rem;
  position:relative;overflow:hidden;
}
.hero::before{
  content:'';position:absolute;inset:0;
  background:radial-gradient(ellipse 80% 60% at 60% 40%, rgba(232,130,12,0.12) 0%, transparent 65%);
  pointer-events:none;
}
.hero-kicker{
  display:inline-flex;align-items:center;gap:0.6rem;
  font-size:0.72rem;font-weight:800;letter-spacing:0.2em;
  text-transform:uppercase;color:var(--orange-light);
  margin-bottom:1.2rem;
}
.hero-kicker::before{content:'';display:block;width:28px;height:2px;background:var(--orange)}
.hero-title{
  font-family:'Abril Fatface',cursive;
  font-size:clamp(2.8rem,5.5vw,5rem);
  color:var(--white);
  line-height:1.05;
  margin-bottom:1.2rem;
}
.hero-title .script{
  font-family:'Dancing Script',cursive;
  font-size:clamp(2.2rem,4vw,3.8rem);
  color:var(--orange-light);
  display:block;
}
.hero-desc{
  font-size:1rem;font-weight:400;line-height:1.7;
  color:rgba(255,255,255,0.6);
  max-width:420px;margin-bottom:2rem;
}
.hero-chips{
  display:flex;flex-wrap:wrap;gap:0.5rem;margin-bottom:2rem;
}
.chip{
  background:rgba(232,130,12,0.15);
  border:1px solid rgba(232,130,12,0.35);
  color:var(--orange-light);
  font-size:0.75rem;font-weight:700;
  letter-spacing:0.05em;text-transform:uppercase;
  padding:0.3rem 0.8rem;border-radius:20px;
}
.hero-btns{display:flex;gap:1rem;flex-wrap:wrap}
.btn-wa{
  display:inline-flex;align-items:center;gap:0.5rem;
  background:var(--green);color:var(--white);
  padding:0.75rem 1.6rem;border-radius:30px;
  font-size:0.85rem;font-weight:800;letter-spacing:0.04em;
  text-decoration:none;transition:transform 0.2s,box-shadow 0.2s;
  box-shadow:0 4px 20px rgba(37,211,102,0.3);
}
.btn-wa:hover{transform:translateY(-2px);box-shadow:0 8px 28px rgba(37,211,102,0.4)}
.btn-menu{
  display:inline-flex;align-items:center;gap:0.5rem;
  background:none;border:2px solid var(--orange);
  color:var(--orange-light);
  padding:0.75rem 1.6rem;border-radius:30px;
  font-size:0.85rem;font-weight:800;letter-spacing:0.04em;
  text-decoration:none;transition:all 0.2s;
}
.btn-menu:hover{background:var(--orange);color:var(--white)}

.hero-img-wrap{
  position:relative;
  display:flex;align-items:center;justify-content:center;
}
.hero-main-img{
  width:100%;max-width:460px;
  aspect-ratio:3/4;
  object-fit:cover;border-radius:12px;
  border:3px solid rgba(232,130,12,0.3);
}
.hero-badge-float{
  position:absolute;bottom:1.5rem;left:-1rem;
  background:var(--red);
  color:var(--white);
  padding:0.9rem 1.2rem;
  border-radius:10px;
  box-shadow:0 8px 24px rgba(192,25,42,0.4);
}
.hero-badge-float strong{
  display:block;font-family:'Abril Fatface',cursive;
  font-size:1.6rem;color:var(--white);line-height:1;
}
.hero-badge-float span{
  font-size:0.7rem;font-weight:700;
  letter-spacing:0.1em;text-transform:uppercase;
  color:rgba(255,255,255,0.75);
}

/* TICKER */
.ticker{
  background:var(--red);padding:0.65rem 0;overflow:hidden;
}
.ticker-inner{
  display:inline-flex;gap:2.5rem;
  animation:ticker 20s linear infinite;white-space:nowrap;
}
.ticker-inner span{
  font-size:0.72rem;font-weight:800;letter-spacing:0.18em;
  text-transform:uppercase;color:rgba(255,255,255,0.9);
}
.ticker-inner .dot{color:var(--orange-light);font-size:0.9rem}
@keyframes ticker{from{transform:translateX(0)}to{transform:translateX(-50%)}}

/* SECTION COMMON */
.section-label{
  font-size:0.7rem;font-weight:800;letter-spacing:0.2em;
  text-transform:uppercase;color:var(--orange);margin-bottom:0.6rem;
}
.section-title{
  font-family:'Abril Fatface',cursive;
  font-size:clamp(1.8rem,3vw,2.8rem);
  color:var(--dark);line-height:1.15;margin-bottom:0.8rem;
}
.section-title span{color:var(--red)}
section{padding:5rem 5vw}

/* ABOUT */
.about{background:var(--cream2)}
.about-inner{
  display:grid;grid-template-columns:1fr 1fr;
  gap:4rem;align-items:center;
}
.about-text p{
  font-size:1rem;line-height:1.75;
  color:var(--muted);margin-bottom:1rem;
}
.about-stats{
  display:flex;gap:2rem;margin-top:1.5rem;
  padding-top:1.5rem;border-top:2px dashed rgba(232,130,12,0.3);
}
.stat strong{
  display:block;font-family:'Abril Fatface',cursive;
  font-size:2rem;color:var(--red);
}
.stat span{font-size:0.75rem;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;color:var(--muted)}
.about-imgs{
  display:grid;grid-template-columns:1fr 1fr;
  grid-template-rows:220px 160px;gap:0.8rem;
}
.about-img{border-radius:8px;overflow:hidden}
.about-img:first-child{grid-row:span 2}
.about-img img{width:100%;height:100%;object-fit:cover;display:block}

/* MENU */
.menu{background:var(--dark)}
.menu-header{
  display:flex;align-items:flex-end;
  justify-content:space-between;
  margin-bottom:2.5rem;flex-wrap:wrap;gap:1rem;
}
.menu-header .section-title{color:var(--white);margin-bottom:0}
.menu-header .section-title span{color:var(--orange-light)}
.tab-bar{display:flex;gap:0.5rem;flex-wrap:wrap}
.tab{
  background:rgba(255,255,255,0.07);
  border:1px solid rgba(232,130,12,0.25);
  color:rgba(255,255,255,0.55);
  font-size:0.72rem;font-weight:800;
  letter-spacing:0.1em;text-transform:uppercase;
  padding:0.4rem 0.9rem;border-radius:20px;
  cursor:pointer;transition:all 0.2s;
}
.tab.active,.tab:hover{
  background:var(--orange);border-color:var(--orange);
  color:var(--white);
}
.menu-panel{display:none}
.menu-panel.active{display:block}
.menu-grid{
  display:grid;grid-template-columns:repeat(3,1fr);gap:1.2rem;
}
.dish-card{
  background:rgba(255,255,255,0.05);
  border:1px solid rgba(232,130,12,0.15);
  border-radius:10px;overflow:hidden;
  transition:transform 0.25s,border-color 0.25s;
}
.dish-card:hover{transform:translateY(-4px);border-color:rgba(232,130,12,0.5)}
.dish-img{
  aspect-ratio:4/3;overflow:hidden;position:relative;
}
.dish-img img{
  width:100%;height:100%;object-fit:cover;display:block;
  transition:transform 0.4s;
}
.dish-card:hover .dish-img img{transform:scale(1.06)}
.dish-tag{
  position:absolute;top:0.6rem;left:0.6rem;
  background:var(--red);color:var(--white);
  font-size:0.62rem;font-weight:800;letter-spacing:0.08em;text-transform:uppercase;
  padding:0.2rem 0.55rem;border-radius:10px;
}
.dish-body{padding:0.9rem 1rem}
.dish-name{
  font-size:0.95rem;font-weight:800;
  color:var(--white);margin-bottom:0.25rem;
}
.dish-desc{font-size:0.78rem;color:rgba(255,255,255,0.45);line-height:1.5;margin-bottom:0.7rem}
.dish-footer{display:flex;justify-content:space-between;align-items:center}
.dish-price{
  font-family:'Abril Fatface',cursive;
  font-size:1.1rem;color:var(--orange-light);
}
.dish-wa{
  background:var(--green);color:var(--white);
  border:none;font-size:0.7rem;font-weight:800;
  letter-spacing:0.05em;
  padding:0.3rem 0.7rem;border-radius:12px;
  cursor:pointer;text-decoration:none;
  display:inline-block;transition:opacity 0.2s;
}
.dish-wa:hover{opacity:0.85}

/* DEALS */
.deals{background:var(--cream2)}
.deals-grid{
  display:grid;grid-template-columns:repeat(3,1fr);gap:1rem;
  margin-top:2rem;
}
.deal-card{
  background:var(--white);border:2px solid transparent;
  border-radius:10px;padding:1.1rem;
  transition:border-color 0.2s,transform 0.2s;
  position:relative;overflow:hidden;
}
.deal-card::before{
  content:'';position:absolute;top:0;left:0;right:0;height:4px;
  background:linear-gradient(90deg,var(--red),var(--orange));
}
.deal-card:hover{border-color:var(--orange);transform:translateY(-3px)}
.deal-name{
  font-size:0.72rem;font-weight:800;letter-spacing:0.1em;
  text-transform:uppercase;color:var(--red);margin-bottom:0.5rem;
}
.deal-items{font-size:0.82rem;color:var(--muted);line-height:1.6;margin-bottom:0.75rem}
.deal-price{
  font-family:'Abril Fatface',cursive;
  font-size:1.4rem;color:var(--dark);
}
.deal-price small{font-family:'Nunito',sans-serif;font-size:0.72rem;color:var(--muted)}

/* BROAST SECTION */
.broast-section{background:var(--dark2)}
.broast-grid{
  display:grid;grid-template-columns:1fr 1fr;gap:2rem;
  align-items:center;margin-top:2.5rem;
}
.broast-img{border-radius:12px;overflow:hidden;aspect-ratio:4/3}
.broast-img img{width:100%;height:100%;object-fit:cover;display:block}
.broast-cards{display:flex;flex-direction:column;gap:1rem}
.broast-card{
  background:rgba(255,255,255,0.06);
  border-left:4px solid var(--orange);
  border-radius:0 8px 8px 0;
  padding:1rem 1.2rem;
  display:flex;justify-content:space-between;align-items:center;
}
.broast-card h4{
  font-size:0.9rem;font-weight:800;color:var(--white);margin-bottom:0.2rem;
}
.broast-card p{font-size:0.77rem;color:rgba(255,255,255,0.5)}
.broast-price{
  font-family:'Abril Fatface',cursive;
  font-size:1.3rem;color:var(--orange-light);
  white-space:nowrap;margin-left:1rem;
}

/* GALLERY */
.gallery{background:var(--cream)}
.gallery-grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  grid-template-rows:220px 220px;
  gap:0.8rem;margin-top:2rem;
}
.gallery-item{border-radius:8px;overflow:hidden}
.gallery-item img{width:100%;height:100%;object-fit:cover;display:block;transition:transform 0.4s}
.gallery-item:hover img{transform:scale(1.05)}
.gallery-item:first-child{grid-column:span 2;grid-row:span 2}
.gallery-item:nth-child(4){grid-column:span 2}

/* CONTACT */
.contact{background:var(--dark)}
.contact-inner{display:grid;grid-template-columns:1fr 1fr;gap:3rem;align-items:start}
.contact-info h2{color:var(--white)}
.contact-detail{
  display:flex;align-items:flex-start;gap:0.8rem;
  margin-top:1.2rem;
}
.contact-icon{
  width:38px;height:38px;border-radius:50%;
  background:rgba(232,130,12,0.15);
  display:flex;align-items:center;justify-content:center;
  font-size:1rem;flex-shrink:0;color:var(--orange-light);
  border:1px solid rgba(232,130,12,0.3);
}
.contact-detail-text h4{font-size:0.75rem;font-weight:800;letter-spacing:0.1em;text-transform:uppercase;color:var(--muted);margin-bottom:0.2rem}
.contact-detail-text p{font-size:0.92rem;color:rgba(255,255,255,0.8)}
.contact-detail-text a{color:var(--orange-light);text-decoration:none}
.map-wrap{
  border-radius:10px;overflow:hidden;
  border:2px solid rgba(232,130,12,0.3);
  height:300px;
}
.map-wrap iframe{width:100%;height:100%;border:none;display:block}

/* FLOATING WA BUTTON */
.wa-float{
  position:fixed;bottom:1.5rem;right:1.5rem;z-index:500;
  background:var(--green);color:var(--white);
  width:56px;height:56px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  box-shadow:0 4px 20px rgba(37,211,102,0.5);
  text-decoration:none;font-size:1.6rem;
  animation:pulse 2.5s infinite;
  transition:transform 0.2s;
}
.wa-float:hover{transform:scale(1.1)}
@keyframes pulse{
  0%,100%{box-shadow:0 4px 20px rgba(37,211,102,0.5)}
  50%{box-shadow:0 4px 32px rgba(37,211,102,0.8),0 0 0 8px rgba(37,211,102,0.15)}
}

/* FOOTER */
footer{
  background:rgba(10,4,0,0.97);
  padding:1.2rem 5vw;
  display:flex;align-items:center;
  justify-content:space-between;flex-wrap:wrap;gap:0.8rem;
  border-top:2px solid var(--red);
}
.footer-brand{
  font-family:'Abril Fatface',cursive;
  font-size:1.1rem;color:var(--white);
}
.footer-brand span{color:var(--orange)}
footer p{font-size:0.78rem;color:rgba(255,255,255,0.4)}
.footer-links{display:flex;gap:1.2rem}
.footer-links a{
  font-size:0.75rem;font-weight:700;letter-spacing:0.06em;
  text-transform:uppercase;color:rgba(255,255,255,0.4);
  text-decoration:none;transition:color 0.2s;
}
.footer-links a:hover{color:var(--orange-light)}

/* RESPONSIVE */
@media(max-width:900px){
  .hero,.about-inner,.broast-grid,.contact-inner{
    grid-template-columns:1fr;gap:2rem;
  }
  .hero{padding-top:5.5rem;padding-bottom:3rem}
  .menu-grid,.deals-grid{grid-template-columns:1fr 1fr}
  .gallery-grid{grid-template-columns:1fr 1fr;grid-template-rows:auto}
  .gallery-item:first-child{grid-column:span 2;grid-row:span 1}
  .gallery-item:nth-child(4){grid-column:span 1}
  .nav-links{display:none}
  .hamburger{display:flex}
  .hero-img-wrap{order:-1}
  .hero-main-img{max-width:340px;margin:0 auto;display:block}
  .hero-badge-float{left:50%;transform:translateX(-50%);bottom:-1rem}
  .about-imgs{grid-template-rows:180px 140px}
}
@media(max-width:600px){
  .menu-grid,.deals-grid{grid-template-columns:1fr}
  .gallery-grid{grid-template-columns:1fr 1fr;grid-template-rows:160px 160px 160px}
  .gallery-item:first-child,.gallery-item:nth-child(4){grid-column:span 2}
  section{padding:3.5rem 4vw}
  .hero-btns{flex-direction:column}
  footer{flex-direction:column;text-align:center}
  .footer-links{justify-content:center}
}

/* SCROLL REVEAL */
.reveal{opacity:0;transform:translateY(22px);transition:opacity 0.55s ease,transform 0.55s ease}
.revealed{opacity:1;transform:translateY(0)}
</style>
</head>
<body>

<!-- FLOATING WHATSAPP -->
<a href="https://wa.me/923242336663" class="wa-float" target="_blank" rel="noopener" title="Order on WhatsApp">
  <svg width="28" height="28" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
</a>

<!-- NAV -->
<nav>
  <a href="#home" class="nav-brand">
    <div class="nav-logo-icon">🍕</div>
    <span class="nav-brand-text">Food <span>Mahal</span></span>
  </a>
  <ul class="nav-links">
    <li><a href="#home">Home</a></li>
    <li><a href="#menu">Menu</a></li>
    <li><a href="#deals">Deals</a></li>
    <li><a href="#broast">Broast</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="https://wa.me/923242336663" class="nav-order-btn" target="_blank">📲 Order Now</a></li>
  </ul>
  <button class="hamburger" onclick="document.querySelector('.mobile-menu').classList.toggle('open')" aria-label="Menu">
    <span></span><span></span><span></span>
  </button>
</nav>
<div class="mobile-menu">
  <a href="#home" onclick="this.closest('.mobile-menu').classList.remove('open')">Home</a>
  <a href="#menu" onclick="this.closest('.mobile-menu').classList.remove('open')">Menu</a>
  <a href="#deals" onclick="this.closest('.mobile-menu').classList.remove('open')">Deals</a>
  <a href="#broast" onclick="this.closest('.mobile-menu').classList.remove('open')">Broast</a>
  <a href="#contact" onclick="this.closest('.mobile-menu').classList.remove('open')">Contact</a>
  <a href="https://wa.me/923242336663" target="_blank" style="color:#25D366!important;margin-top:0.5rem">📲 Order on WhatsApp</a>
</div>

<!-- HERO -->
<section id="home" class="hero" style="padding-top:6rem">
  <div class="hero-content">
    <div class="hero-kicker">Pir Mahal's Favourite Restaurant</div>
    <h1 class="hero-title">
      Taste the<br/>
      <span class="script">Magic of</span>
      Real Food
    </h1>
    <p class="hero-desc">Pizza · Chicken Broast · Fast Food · Bar B.Q. — cooked fresh, served hot. Order in 25–30 minutes right to your door.</p>
    <div class="hero-chips">
      <span class="chip">🍕 Pizza</span>
      <span class="chip">🍗 Broast</span>
      <span class="chip">🔥 BBQ</span>
      <span class="chip">🍔 Fast Food</span>
      <span class="chip">🌯 Wraps</span>
    </div>
    <div class="hero-btns">
      <a href="https://wa.me/923242336663?text=Hi%20Food%20Mahal%2C%20I%20want%20to%20order!" class="btn-wa" target="_blank">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 
