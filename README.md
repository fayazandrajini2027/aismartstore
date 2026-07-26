# aismartstore
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:css='false' b:defaultwidgetversion='2' b:layoutsVersion='3' b:responsive='true' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
<head>
  <meta content='width=device-width, initial-scale=1' name='viewport'/>
  <b:include data='blog' name='all-head-content'/>
  <title><b:if cond='data:view.isHomepage'><data:blog.title/> | Premium AI Tools &amp; Digital Solutions</b:if><b:if cond='!data:view.isHomepage'><data:view.title/> | <data:blog.title/></b:if></title>
  <meta content='#06070a' name='theme-color'/>
  <b:if cond='data:view.isHomepage'>
    <meta content='Premium AI tools, productivity memberships and entertainment plans from AISMARTSTOR.IN.' name='description'/>
  </b:if>

  <!-- Premium Google Fonts -->
  <link href='https://fonts.googleapis.com' rel='preconnect'/>
  <link crossorigin='anonymous' href='https://fonts.gstatic.com' rel='preconnect'/>
  <link href='https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,600;0,800;1,600&amp;family=Plus+Jakarta+Sans:wght@400;500;700;800&amp;display=swap' rel='stylesheet'/>

  <b:skin><![CDATA[
/* ==========================================================
   AISMARTSTOR.IN — Luxury Blogger Theme
   1. TOKENS + RESET
   ========================================================== */
:root {
  --bg: #06070a;
  --bg-soft: #0b0d12;
  --card-bg: rgba(17, 19, 25, 0.82);
  --text-main: #f7f4ec;
  --text-muted: #a9abb4;
  --gold: #cba65b;
  --gold-light: #f8e7b3;
  --ivory: #f7f3e9;
  --electric: #8d7cff;
  --wa-green: #25D366;
  --border-color: rgba(255,255,255,.09);
  --shadow: 0 24px 80px rgba(0,0,0,.42);
  /* ONE rail for the whole page — this is what fixes the alignment */
  --wrap: 1240px;
  --gutter: clamp(16px, 4vw, 28px);
  --nav-h: 76px;
}
*, *::before, *::after { box-sizing: border-box; }
html { scroll-behavior: smooth; scroll-padding-top: calc(var(--nav-h) + 22px); -webkit-text-size-adjust: 100%; }
body {
  font-family: 'Plus Jakarta Sans', system-ui, -apple-system, 'Segoe UI', sans-serif;
  margin: 0; padding: 0; line-height: 1.6; color: var(--text-main);
  background:
    radial-gradient(circle at 10% 0%, rgba(216,177,95,.11), transparent 28rem),
    radial-gradient(circle at 90% 26%, rgba(94,77,180,.08), transparent 30rem),
    var(--bg);
  overflow-x: hidden;
}
body::before {
  content: ''; position: fixed; inset: 0; pointer-events: none; opacity: .16; z-index: -1;
  background-image: linear-gradient(rgba(255,255,255,.025) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,.025) 1px, transparent 1px);
  background-size: 56px 56px;
  -webkit-mask-image: linear-gradient(to bottom, black, transparent 80%);
  mask-image: linear-gradient(to bottom, black, transparent 80%);
}
::selection { background: var(--gold); color: #080808; }
img { max-width: 100%; height: auto; }
h1, h2, h3, .logo { font-family: 'Playfair Display', Georgia, serif; }

/* Shared alignment rail. Every band on the page uses this, so the
   navbar, hero, product grid, service strip and footer all line up. */
.wrap {
  width: 100%;
  max-width: calc(var(--wrap) + (var(--gutter) * 2));
  margin-left: auto; margin-right: auto;
  padding-left: var(--gutter); padding-right: var(--gutter);
}

/* ==========================================================
   2. NAVBAR, QUICK NAV + SEARCH
   ========================================================== */
nav.site-nav {
  position: sticky; top: 0; z-index: 50;
  background: rgba(6,7,10,.82);
  -webkit-backdrop-filter: blur(24px); backdrop-filter: blur(24px);
  border-bottom: 1px solid rgba(255,255,255,.075);
}
.nav-inner {
  display: flex; align-items: center; justify-content: space-between;
  gap: 18px; min-height: var(--nav-h);
  padding-top: 12px; padding-bottom: 12px;
}
.brand-lockup { display: flex; align-items: center; gap: 12px; text-decoration: none; flex: 0 0 auto; }
.brand-seal {
  width: 44px; height: 44px; flex: 0 0 auto; display: grid; place-items: center;
  border-radius: 14px; color: #111; background: linear-gradient(145deg,#fff3c7,#c89b45);
  box-shadow: 0 9px 28px rgba(203,166,91,.24), inset 0 1px 0 rgba(255,255,255,.8);
  font-family: 'Playfair Display', serif; font-weight: 800; font-size: 1.03em;
}
.brand-name { display: block; color: #fff; font-family: 'Plus Jakarta Sans', sans-serif; font-weight: 800; font-size: .95em; letter-spacing: 1.6px; line-height: 1.2; }
.brand-note { display: block; color: #8f9099; font-size: .58em; line-height: 1.5; letter-spacing: 1.4px; text-transform: uppercase; margin-top: 3px; }
.nav-action {
  flex: 0 0 auto; color: #0a0a0a; background: linear-gradient(135deg, #fff1c7, var(--gold));
  padding: 11px 18px; border-radius: 999px; text-decoration: none;
  font-size: .78em; font-weight: 800; white-space: nowrap;
  box-shadow: 0 8px 30px rgba(216,177,95,.18);
  transition: transform .25s ease, box-shadow .25s ease;
}
.nav-action:hover { transform: translateY(-2px); box-shadow: 0 12px 35px rgba(216,177,95,.28); }

.search-container { flex: 1 1 240px; min-width: 0; max-width: 460px; position: relative; }
.search-container > svg { position: absolute; left: 17px; top: 50%; width: 18px; height: 18px; transform: translateY(-50%); stroke: var(--gold-light); z-index: 1; pointer-events: none; }
.search-bar {
  width: 100%; padding: 12px 20px 12px 46px; border-radius: 50px;
  border: 1px solid var(--border-color); background: rgba(255,255,255,.045);
  color: #fff; outline: none; font-size: .92em; transition: border-color .3s ease, box-shadow .3s ease, background .3s ease;
  font-family: 'Plus Jakarta Sans', sans-serif;
}
.search-bar::placeholder { color: #7f818a; }
.search-bar:focus { border-color: var(--gold); box-shadow: 0 0 0 3px rgba(212,175,55,.14); background: rgba(255,255,255,.075); }
.search-status {
  position: absolute; left: 12px; top: calc(100% + 12px); display: none;
  padding: 9px 13px; color: #e9e9ed; background: rgba(15,16,20,.97);
  border: 1px solid rgba(255,255,255,.1); border-radius: 12px;
  box-shadow: 0 14px 35px rgba(0,0,0,.35); font-size: .72em; font-weight: 700;
  white-space: nowrap; z-index: 80;
}
.search-status.active { display: block; }

.quick-nav { background: rgba(8,9,12,.94); border-bottom: 1px solid rgba(255,255,255,.065); }
.quick-nav-inner {
  display: flex; align-items: center; gap: 8px;
  padding-top: 9px; padding-bottom: 9px;
  overflow-x: auto; scrollbar-width: none; -webkit-overflow-scrolling: touch;
}
.quick-nav-inner::-webkit-scrollbar { display: none; }
.quick-nav a {
  flex: 0 0 auto; color: #aeb0b8; text-decoration: none; font-size: .70em; font-weight: 700;
  letter-spacing: .65px; padding: 8px 12px; border-radius: 999px;
  transition: color .2s ease, background .2s ease; white-space: nowrap;
}
.quick-nav a:hover { color: #fff; background: rgba(255,255,255,.06); }
.quick-nav a.featured { color: #f4d68e; border: 1px solid rgba(203,166,91,.2); background: rgba(203,166,91,.07); }

/* ==========================================================
   3. HERO (opening screen)
   ========================================================== */
header.hero {
  position: relative; isolation: isolate; overflow: hidden;
  text-align: left;
  border-bottom: 1px solid var(--border-color);
  padding-top: clamp(52px, 6.5vw, 92px);
  padding-bottom: clamp(48px, 6vw, 82px);
  background:
    radial-gradient(circle at 50% 0%, rgba(216,177,95,.20), transparent 31rem),
    radial-gradient(circle at 14% 70%, rgba(91,74,170,.10), transparent 25rem),
    linear-gradient(180deg, #090a0e, #06070a);
}
header.hero::after {
  content: ''; position: absolute; z-index: 0;
  width: 460px; height: 460px; border: 1px solid rgba(216,177,95,.15); border-radius: 50%;
  left: 50%; top: -320px; transform: translateX(-50%);
  box-shadow: 0 0 0 80px rgba(216,177,95,.025), 0 0 0 160px rgba(216,177,95,.015);
  pointer-events: none;
}
.hero-inner {
  position: relative; z-index: 2;
  display: grid; grid-template-columns: minmax(0, 1.06fr) minmax(0, .94fr);
  align-items: center; gap: clamp(34px, 4.5vw, 64px);
}
.hero-copy { min-width: 0; }
.eyebrow {
  display: inline-flex; align-items: center; gap: 9px; padding: 8px 14px;
  border: 1px solid rgba(216,177,95,.27); border-radius: 999px; color: var(--gold-light);
  font-size: .70em; font-weight: 800; letter-spacing: 1.6px; text-transform: uppercase;
  margin-bottom: 22px; background: rgba(216,177,95,.06);
  box-shadow: inset 0 1px 0 rgba(255,255,255,.06); line-height: 1.4;
}
.eyebrow::before { content: ''; flex: 0 0 auto; width: 6px; height: 6px; border-radius: 50%; background: #84f0b4; box-shadow: 0 0 12px #84f0b4; }
.hero h1 {
  margin: 0 0 20px; font-weight: 800;
  font-size: clamp(2.15rem, 5vw, 3.9rem);
  line-height: 1.08; letter-spacing: -1.4px;
  overflow-wrap: break-word;
}
.gradient-text { background: linear-gradient(135deg, #d8b15f 0%, #fff0bd 48%, #b98a37 100%); -webkit-background-clip: text; background-clip: text; color: transparent; }
.hero p { margin: 0 0 28px; max-width: 56ch; font-size: clamp(1rem, 1.1vw, 1.09rem); color: #b4b4bc; line-height: 1.75; }
.hero-intro { animation: hero-gentle-reveal .72s cubic-bezier(.22,.75,.25,1) both; }
.hero-intro-1 { animation-delay: .08s; }
.hero-intro-2 { animation-delay: .16s; }
.hero-intro-3 { animation-delay: .24s; }
@keyframes hero-gentle-reveal {
  from { opacity: 0; transform: translateY(12px); }
  to { opacity: 1; transform: translateY(0); }
}
.hero-actions { display: flex; justify-content: flex-start; flex-wrap: wrap; gap: 12px; margin-bottom: 30px; }
.hero-btn {
  display: inline-flex; align-items: center; justify-content: center; gap: 9px;
  min-width: 178px; padding: 15px 22px; border-radius: 999px; text-decoration: none;
  font-size: .84em; font-weight: 800; transition: transform .25s ease, box-shadow .25s ease;
}
.hero-btn.primary { color: #090909; background: linear-gradient(135deg, #fff1c7, #c79d4d); box-shadow: 0 16px 45px rgba(199,157,77,.2); }
.hero-btn.secondary { color: #f2f2f4; border: 1px solid rgba(255,255,255,.13); background: rgba(255,255,255,.045); }
.hero-btn:hover { transform: translateY(-3px); }
.trust-badges { display: flex; justify-content: flex-start; flex-wrap: wrap; gap: 10px; }
.trust-badges span { padding: 10px 14px; border-radius: 999px; background: rgba(255,255,255,.04); border: 1px solid var(--border-color); font-weight: 700; font-size: .74em; color: #d8d8dd; text-transform: uppercase; letter-spacing: 1px; }

.hero-showcase {
  position: relative; min-width: 0;
  border: 1px solid rgba(255,255,255,.10); border-radius: 30px; padding: clamp(22px, 2.4vw, 30px);
  background: linear-gradient(145deg, rgba(255,255,255,.075), rgba(255,255,255,.018));
  box-shadow: 0 35px 100px rgba(0,0,0,.48), inset 0 1px 0 rgba(255,255,255,.08);
  overflow: hidden;
}
.hero-showcase::before { content: ''; position: absolute; width: 230px; height: 230px; right: -90px; top: -100px; border-radius: 50%; background: rgba(203,166,91,.25); filter: blur(65px); }
.showcase-kicker { position: relative; color: #b8b9c1; font-size: .67em; font-weight: 800; text-transform: uppercase; letter-spacing: 1.6px; }
.showcase-title { position: relative; color: #fff; font-family: 'Playfair Display', serif; font-size: clamp(1.5rem, 2vw, 1.95rem); line-height: 1.16; margin: 11px 0 24px; max-width: 21ch; }
.logo-stack { position: relative; display: grid; grid-template-columns: repeat(4, minmax(0, 1fr)); gap: 10px; }
.mini-logo { height: clamp(52px, 5vw, 66px); display: grid; place-items: center; border-radius: 18px; background: rgba(255,255,255,.95); box-shadow: 0 12px 30px rgba(0,0,0,.22); color: #111; }
.mini-logo svg { width: 60%; max-width: 34px; height: auto; display: block; }
.showcase-meta { position: relative; display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 22px; padding-top: 21px; border-top: 1px solid rgba(255,255,255,.09); }
.showcase-meta strong { display: block; color: #fff; font-size: 1.14em; margin-bottom: 4px; }
.showcase-meta span { color: #92949d; font-size: .70em; line-height: 1.45; }

/* Compact header used on post / page / label views */
.page-head {
  border-bottom: 1px solid var(--border-color);
  padding-top: clamp(38px, 5vw, 66px); padding-bottom: clamp(30px, 4vw, 52px);
  background: radial-gradient(circle at 50% 0%, rgba(216,177,95,.14), transparent 26rem), linear-gradient(180deg, #090a0e, #06070a);
}
.page-head h1 { margin: 0; color: #fff; font-size: clamp(1.85rem, 4vw, 3rem); line-height: 1.1; letter-spacing: -1px; overflow-wrap: break-word; }

/* ==========================================================
   4. LAYOUT + SECTION HEADINGS
   ========================================================== */
.container { padding-top: clamp(38px, 4.5vw, 62px); padding-bottom: clamp(38px, 4.5vw, 62px); }
.category-title {
  font-size: clamp(1.95rem, 4.4vw, 3.2rem); margin: clamp(46px, 5vw, 74px) 0 30px;
  color: #fff; text-align: left; letter-spacing: -1.6px; line-height: 1.06;
  scroll-margin-top: calc(var(--nav-h) + 22px);
}
.category-title:first-child { margin-top: 0; }
.category-title small { display: block; color: var(--gold); font-family: 'Plus Jakarta Sans', sans-serif; font-size: .26em; letter-spacing: 2px; text-transform: uppercase; margin-bottom: 10px; line-height: 1.5; }
.launch-banner {
  display: flex; align-items: center; justify-content: space-between; gap: 22px;
  padding: 22px 24px; margin: 14px 0 22px; border: 1px solid rgba(132,240,180,.2);
  border-radius: 22px; background: linear-gradient(135deg, rgba(132,240,180,.08), rgba(141,124,255,.07));
  box-shadow: inset 0 1px 0 rgba(255,255,255,.05);
}
.launch-banner strong { display: block; color: #fff; font-size: 1.02em; margin-bottom: 5px; }
.launch-banner span { color: var(--text-muted); font-size: .86em; }
.email-chip { display: inline-flex; align-items: center; gap: 8px; flex-shrink: 0; padding: 10px 14px; border-radius: 999px; color: #b9f8cf; background: rgba(132,240,180,.08); border: 1px solid rgba(132,240,180,.2); font-size: .73em; font-weight: 800; text-transform: uppercase; letter-spacing: .8px; overflow-wrap: anywhere; }
.product-grid {
  display: grid; grid-template-columns: repeat(auto-fill, minmax(272px, 1fr));
  gap: 18px; margin-bottom: 8px;
  scroll-margin-top: calc(var(--nav-h) + 22px);
}

/* ==========================================================
   5. SCROLL ANIMATION
   ========================================================== */
.animate-scroll { opacity: 0; transform: translateY(46px); transition: opacity .9s cubic-bezier(.25,1,.5,1), transform .9s cubic-bezier(.25,1,.5,1); }
.animate-scroll.visible { opacity: 1; transform: translateY(0); }

/* ==========================================================
   6. PRODUCT CARDS
   ========================================================== */
.product-card {
  display: flex; flex-direction: column; min-width: 0;
  border-radius: 26px; padding: 26px; border: 1px solid rgba(255,255,255,.085);
  -webkit-backdrop-filter: blur(14px); backdrop-filter: blur(14px);
  box-shadow: 0 18px 55px rgba(0,0,0,.25);
  position: relative; overflow: hidden; min-height: 430px;
  transform-origin: 50% 80%; will-change: transform, opacity;
  transition: transform .35s ease, border-color .35s ease, box-shadow .35s ease;
  background:
    radial-gradient(260px circle at var(--mx,86%) var(--my,2%), var(--accent-soft, rgba(216,177,95,.14)), transparent 58%),
    linear-gradient(145deg, rgba(255,255,255,.057), rgba(255,255,255,.014));
}
.product-card::before { content: ''; position: absolute; top: 0; left: 0; width: 100%; height: 2px; background: linear-gradient(90deg, transparent, var(--accent, var(--gold-light)), transparent); opacity: 0; transition: opacity .4s ease; }
.product-card::after { content: ''; position: absolute; width: 190px; height: 190px; border-radius: 50%; background: var(--accent-soft, rgba(216,177,95,.16)); filter: blur(62px); top: -115px; right: -90px; opacity: .9; pointer-events: none; }
.product-card:hover { transform: translateY(-9px); border-color: rgba(216,177,95,.42); box-shadow: 0 34px 85px rgba(0,0,0,.55); }
.product-card:hover::before { opacity: 1; }

.product-grid .product-card:nth-child(8n+1) { --accent:#79e6a5; --accent-soft:rgba(121,230,165,.13); }
.product-grid .product-card:nth-child(8n+2) { --accent:#9b8cff; --accent-soft:rgba(155,140,255,.14); }
.product-grid .product-card:nth-child(8n+3) { --accent:#64c9ff; --accent-soft:rgba(100,201,255,.13); }
.product-grid .product-card:nth-child(8n+4) { --accent:#ff8e9d; --accent-soft:rgba(255,142,157,.13); }
.product-grid .product-card:nth-child(8n+5) { --accent:#f4cd70; --accent-soft:rgba(244,205,112,.14); }
.product-grid .product-card:nth-child(8n+6) { --accent:#6ee7dc; --accent-soft:rgba(110,231,220,.13); }
.product-grid .product-card:nth-child(8n+7) { --accent:#d493ff; --accent-soft:rgba(212,147,255,.13); }
.product-grid .product-card:nth-child(8n+8) { --accent:#ffab67; --accent-soft:rgba(255,171,103,.13); }

.brand-icon {
  width: 64px; height: 64px; flex: 0 0 auto; display: grid; place-items: center;
  border-radius: 20px; background: linear-gradient(145deg, #fff, #ececec);
  margin-bottom: 22px; box-shadow: 0 14px 35px rgba(0,0,0,.34), inset 0 1px 0 #fff;
  position: relative; z-index: 1; color: #111; align-self: flex-start;
  border: 1px solid rgba(255,255,255,.34);
  transition: transform .42s cubic-bezier(.2,.8,.2,1), box-shadow .42s ease;
}
.brand-icon svg { width: 38px; height: 38px; display: block; }
.brand-icon.wordmark { width: auto; min-width: 64px; padding: 0 15px; display: inline-flex; align-items: center; font-size: .70em; font-weight: 900; letter-spacing: -.2px; color: #0b0b0d; text-align: center; }
.brand-icon.multi { width: auto; display: inline-flex; align-items: center; padding: 0 13px; gap: 8px; }
.brand-icon.multi svg { width: 27px; height: 27px; }
.product-card:hover .brand-icon { transform: translateY(-5px) rotate(-2deg) scale(1.06); box-shadow: 0 20px 42px rgba(0,0,0,.44), 0 0 0 5px var(--accent-soft, rgba(216,177,95,.16)); }

.card-title { font-size: 1.4em; font-weight: 800; margin: 0 0 8px; color: #fbfaf6; font-family: 'Plus Jakarta Sans', sans-serif; letter-spacing: -.4px; line-height: 1.25; overflow-wrap: break-word; transition: color .28s ease, transform .28s ease; }
.product-card:hover .card-title { color: var(--accent, var(--gold-light)); transform: translateX(2px); }
.product-tagline { font-size: .88em; font-weight: 600; color: var(--gold-light); margin-bottom: 16px; font-family: 'Playfair Display', serif; font-style: italic; letter-spacing: .4px; opacity: .95; line-height: 1.45; }
.badge { display: inline-block; padding: 6px 11px; border-radius: 50px; font-size: .70em; font-weight: 800; margin-bottom: 16px; width: -webkit-max-content; width: max-content; max-width: 100%; text-transform: uppercase; letter-spacing: 1px; color: var(--gold-light); background: var(--accent-soft, rgba(216,177,95,.09)); border: 1px solid rgba(216,177,95,.23); }
.product-desc { font-size: .90em; color: var(--text-muted); margin: 0 0 20px; line-height: 1.68; }
.features { list-style: none; padding: 0; margin: 0 0 24px; flex-grow: 1; }
.features li { font-size: .86em; color: #d4d4da; margin-bottom: 11px; display: flex; align-items: flex-start; gap: 10px; line-height: 1.55; font-weight: 600; transition: color .22s ease, transform .22s ease; }
.product-card:hover .features li { color: #ececf0; transform: translateX(2px); }
.feat-icon { flex: 0 0 auto; color: var(--accent, #91e6af); font-size: 1em; line-height: 1.55; }

.dm-btn {
  background: linear-gradient(135deg, #f9e7ac, #c99a44); color: #080808;
  padding: 15px; text-decoration: none; border-radius: 14px; font-weight: 800;
  text-align: center; transition: box-shadow .3s ease, transform .3s ease, filter .3s ease;
  margin-top: auto; display: block; text-transform: uppercase; letter-spacing: .8px;
  font-size: .82em; position: relative; overflow: hidden;
}
.dm-btn:hover { box-shadow: 0 12px 30px rgba(216,177,95,.25); transform: translateY(-2px); filter: brightness(1.06); }
.dm-btn::after { content: ''; position: absolute; inset: 0; transform: translateX(-120%) skewX(-18deg); background: linear-gradient(90deg, transparent, rgba(255,255,255,.42), transparent); transition: transform .65s ease; }
.product-card:hover .dm-btn::after { transform: translateX(120%) skewX(-18deg); }

.product-card.animate-scroll { opacity: 0; transform: translateY(34px) scale(.965); filter: blur(5px); }
.product-card.animate-scroll.visible { animation: card-arrive .72s cubic-bezier(.2,.8,.2,1) var(--delay,0ms) both; }
.product-card.visible .brand-icon { animation: icon-arrive .72s cubic-bezier(.2,.9,.2,1) calc(var(--delay,0ms) + 100ms) both; }
@keyframes card-arrive {
  0% { opacity:0; transform:translateY(34px) scale(.965); filter:blur(5px); }
  62% { opacity:1; transform:translateY(-4px) scale(1.006); filter:blur(0); }
  100% { opacity:1; transform:translateY(0) scale(1); filter:blur(0); }
}
@keyframes icon-arrive {
  0% { opacity:0; transform:translateY(15px) scale(.8) rotate(5deg); }
  70% { opacity:1; transform:translateY(-3px) scale(1.04) rotate(-2deg); }
  100% { opacity:1; transform:none; }
}

/* ==========================================================
   7. BLOG POSTS + PAGES
   ========================================================== */
.post-stream { display: grid; gap: 26px; }
.post-entry {
  border: 1px solid var(--border-color); border-radius: 26px;
  padding: clamp(22px, 3vw, 38px);
  background: linear-gradient(145deg, rgba(255,255,255,.05), rgba(255,255,255,.014));
  box-shadow: 0 18px 55px rgba(0,0,0,.25); min-width: 0;
}
.post-title { margin: 0 0 10px; color: #fff; font-size: clamp(1.4rem, 2.6vw, 2.1rem); line-height: 1.2; letter-spacing: -.6px; overflow-wrap: break-word; }
.post-title a { color: inherit; text-decoration: none; transition: color .25s ease; }
.post-title a:hover { color: var(--gold-light); }
.post-meta { color: var(--gold); font-size: .72em; font-weight: 800; text-transform: uppercase; letter-spacing: 1.4px; margin-bottom: 18px; }
.post-body { color: #d4d4da; font-size: .97em; line-height: 1.8; overflow-wrap: break-word; }
.post-body a { color: var(--gold-light); }
.post-body img { border-radius: 16px; }
.post-body h2, .post-body h3 { color: #fff; line-height: 1.25; }
.post-more { max-width: 260px; margin-top: 26px; }
.blog-pager { display: flex; flex-wrap: wrap; justify-content: space-between; gap: 12px; margin-top: 30px; }
.pager-btn { color: #f2f2f4; text-decoration: none; border: 1px solid rgba(255,255,255,.13); background: rgba(255,255,255,.045); padding: 12px 20px; border-radius: 999px; font-size: .8em; font-weight: 800; }
.pager-btn:hover { border-color: rgba(216,177,95,.42); }
.blog-section .widget { min-width: 0; }

/* ==========================================================
   8. FLOATING WHATSAPP
   ========================================================== */
.floating-wa {
  position: fixed; bottom: 24px; right: 24px; background: var(--wa-green); color: #fff;
  width: 60px; height: 60px; border-radius: 50%; display: flex; justify-content: center;
  align-items: center; box-shadow: 0 10px 25px rgba(37,211,102,.35); text-decoration: none;
  z-index: 1000; transition: transform .3s; border: 2px solid rgba(255,255,255,.35);
}
.floating-wa svg { width: 30px; height: 30px; fill: #fff; }
.floating-wa:hover { transform: scale(1.1) rotate(5deg); }

/* ==========================================================
   9. SERVICE STRIP + FOOTER
   ========================================================== */
.service-band { padding-top: 6px; padding-bottom: 6px; }
.service-strip {
  display: grid; grid-template-columns: repeat(3, minmax(0, 1fr));
  border: 1px solid var(--border-color); border-radius: 24px;
  background: rgba(255,255,255,.025); overflow: hidden;
}
.service-item { padding: 24px 22px; text-align: center; border-right: 1px solid var(--border-color); min-width: 0; }
.service-item:last-child { border-right: 0; }
.service-item strong { display: block; color: var(--ivory); margin-bottom: 5px; }
.service-item span { color: var(--text-muted); font-size: .82em; }

.premium-footer {
  text-align: left; margin-top: clamp(46px, 5.5vw, 72px);
  background: radial-gradient(circle at 16% 0%, rgba(203,166,91,.10), transparent 26rem), #030304;
  border-top: 1px solid var(--border-color);
}
.footer-cta {
  display: flex; align-items: center; justify-content: space-between; gap: 32px;
  padding-top: clamp(40px, 5vw, 60px); padding-bottom: clamp(34px, 4vw, 46px);
  border-bottom: 1px solid rgba(255,255,255,.08);
}
.footer-cta small { display: block; color: var(--gold); font-size: .68em; font-weight: 800; text-transform: uppercase; letter-spacing: 1.6px; margin-bottom: 9px; }
.footer-cta h2 { color: #fff; font-family: 'Playfair Display', serif; font-size: clamp(1.7rem, 3.4vw, 2.9rem); line-height: 1.12; margin: 0; max-width: 22ch; }
.footer-cta a {
  flex: 0 0 auto; display: inline-flex; align-items: center; gap: 10px;
  padding: 15px 22px; border-radius: 999px; color: #0a0a0a;
  background: linear-gradient(135deg, #fff1c5, #c99d4c); text-decoration: none;
  font-size: .78em; font-weight: 800; box-shadow: 0 16px 40px rgba(203,166,91,.18);
  transition: transform .25s ease;
}
.footer-cta a:hover { transform: translateY(-2px); }
.footer-grid {
  display: grid; grid-template-columns: 1.5fr 1fr 1fr 1.2fr;
  gap: clamp(28px, 3.4vw, 46px);
  padding-top: clamp(34px, 4vw, 46px); padding-bottom: clamp(34px, 4vw, 46px);
  align-items: start;
}
.footer-grid > div { min-width: 0; }
.footer-brand .brand-lockup { margin-bottom: 18px; }
.footer-brand p { max-width: 38ch; color: #8f9099; line-height: 1.75; font-size: .85em; margin: 0 0 20px; }
.footer-heading { color: #f4f4f5; font-size: .74em; font-weight: 800; letter-spacing: 1.25px; text-transform: uppercase; margin: 4px 0 18px; }
.footer-links { list-style: none; margin: 0; padding: 0; }
.footer-links li { margin-bottom: 12px; }
.footer-links a, .footer-links span { color: #92949d; text-decoration: none; font-size: .84em; line-height: 1.5; transition: color .2s ease; overflow-wrap: anywhere; }
.footer-links a:hover { color: var(--gold-light); }
.contact-row { display: flex; align-items: flex-start; gap: 10px; min-width: 0; }
.contact-row svg { flex: 0 0 auto; width: 17px; height: 17px; margin-top: 3px; stroke: var(--gold); fill: none; stroke-width: 1.6; }
.payment-pills { display: flex; flex-wrap: wrap; gap: 7px; margin-top: 15px; }
.payment-pills span { color: #d5d5d8; border: 1px solid rgba(255,255,255,.1); background: rgba(255,255,255,.04); border-radius: 999px; padding: 7px 11px; font-size: .68em; font-weight: 800; }
.footer-bottom { border-top: 1px solid rgba(255,255,255,.07); }
.footer-bottom-inner {
  display: flex; justify-content: space-between; align-items: center; gap: 18px;
  padding-top: 20px; padding-bottom: 24px; color: #6f7179; font-size: .72em;
}
.footer-status { display: inline-flex; align-items: center; gap: 7px; white-space: nowrap; }
.footer-status::before { content: ''; width: 6px; height: 6px; border-radius: 50%; background: #72e5a0; box-shadow: 0 0 10px rgba(114,229,160,.8); }

/* ==========================================================
   10. RESPONSIVE
   ========================================================== */
@media (max-width: 1000px) {
  .hero-inner { grid-template-columns: 1fr; gap: 40px; }
  .hero-showcase { max-width: 560px; }
  .footer-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }
  .footer-brand { grid-column: 1 / -1; }
}
@media (max-width: 860px) {
  .footer-cta { flex-direction: column; align-items: flex-start; }
  .footer-cta h2 { max-width: none; }
  .service-strip { grid-template-columns: 1fr; }
  .service-item { border-right: 0; border-bottom: 1px solid var(--border-color); }
  .service-item:last-child { border-bottom: 0; }
}
@media (max-width: 760px) {
  :root { --nav-h: 64px; }
  .nav-inner { flex-wrap: wrap; gap: 12px; padding-top: 10px; padding-bottom: 12px; }
  .brand-note { display: none; }
  .brand-seal { width: 38px; height: 38px; border-radius: 12px; }
  .nav-action { font-size: .72em; padding: 10px 14px; }
  .search-container { order: 3; flex: 1 1 100%; max-width: none; }
  .product-grid { grid-template-columns: 1fr; }
  .product-card { min-height: 0; }
  .launch-banner { flex-direction: column; align-items: flex-start; padding: 20px; }
  .showcase-meta { grid-template-columns: 1fr; }
  .footer-bottom-inner { flex-direction: column; align-items: flex-start; }
  .post-more { max-width: none; }
}
@media (max-width: 480px) {
  .brand-name { font-size: .84em; }
  .nav-action { display: none; }
  .hero h1 { letter-spacing: -1px; }
  .hero-btn { min-width: 100%; }
  .floating-wa { width: 54px; height: 54px; right: 16px; bottom: 16px; }
  .mini-logo { border-radius: 14px; }
  .footer-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 30px 20px; }
  .footer-grid > div:last-child { grid-column: 1 / -1; }
}
@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  *, *::before, *::after { transition: none !important; animation: none !important; }
  .animate-scroll, .hero-intro { opacity: 1; transform: none; }
  .product-card.animate-scroll, .product-card.animate-scroll.visible, .product-card.visible .brand-icon { opacity: 1; transform: none; filter: none; }
}

/* Keep the Blogger Layout editor usable */
body#layout .hero, body#layout .quick-nav, body#layout .service-band, body#layout .floating-wa { display: none; }
body#layout .container, body#layout .premium-footer { padding: 10px; }

  ]]></b:skin>
</head>
<body>

  <!-- ============ NAVBAR ============ -->
  <nav class='site-nav'>
    <div class='nav-inner wrap'>
      <a class='brand-lockup' expr:href='data:blog.homepageUrl'>
        <span class='brand-seal'>AI</span>
        <span><span class='brand-name'>AISMARTSTOR.IN</span><span class='brand-note'>Premium digital membership store</span></span>
      </a>
      <div class='search-container'>
        <svg aria-hidden='true' fill='none' stroke-width='1.8' viewBox='0 0 24 24'><circle cx='11' cy='11' r='7'/><path d='m20 20-3.6-3.6'/></svg>
        <input aria-label='Search premium tools' autocomplete='off' class='search-bar' id='searchInput' placeholder='Search premium tools...' type='search'/>
        <span aria-live='polite' class='search-status' id='searchStatus'></span>
      </div>
      <a class='nav-action' href='https://wa.me/919071145694?text=Hi,%20I%20want%20to%20explore%20your%20premium%20plans' rel='noopener' target='_blank'>Explore plans</a>
    </div>
  </nav>

  <!-- ============ CATEGORY QUICK NAV ============ -->
  <div class='quick-nav'>
    <div class='quick-nav-inner wrap' aria-label='Product categories'>
      <a expr:href='data:blog.homepageUrl + &quot;#grid-ai&quot;'>AI tools</a>
      <a expr:href='data:blog.homepageUrl + &quot;#grid-prod&quot;'>Productivity</a>
      <a expr:href='data:blog.homepageUrl + &quot;#grid-biz&quot;'>Business</a>
      <a expr:href='data:blog.homepageUrl + &quot;#grid-ent&quot;'>Entertainment</a>
      <a class='featured' expr:href='data:blog.homepageUrl + &quot;#grid-new&quot;'>Newly added</a>
    </div>
  </div>

  <b:if cond='data:view.isHomepage'>

  <!-- ============ HERO (homepage only) ============ -->
  <header class='hero'>
    <div class='hero-inner wrap'>
      <div class='hero-copy'>
        <div class='eyebrow hero-intro hero-intro-1'>Curated access for ambitious creators</div>
        <h1 class='hero-intro hero-intro-2'>Premium tools.<br/><span class='gradient-text'>Serious momentum</span></h1>
        <p class='hero-intro hero-intro-3'>A carefully selected collection of AI, creative, business and entertainment memberships&#8212;with clear guidance and responsive human support.</p>
        <div class='hero-actions animate-scroll'>
          <a class='hero-btn primary' href='#grid-ai'>Explore the collection <span aria-hidden='true'>&#8595;</span></a>
          <a class='hero-btn secondary' href='https://wa.me/919071145694?text=Hi,%20I%20need%20help%20choosing%20a%20premium%20plan' rel='noopener' target='_blank'>Get personal guidance <span aria-hidden='true'>&#8594;</span></a>
        </div>
        <div class='trust-badges animate-scroll'>
          <span>100+ plans delivered</span>
          <span>Fast activation</span>
          <span>Human assistance</span>
        </div>
      </div>
      <div class='hero-showcase animate-scroll'>
        <div class='showcase-kicker'>One store &#8226; exceptional possibilities</div>
        <div class='showcase-title'>Your next breakthrough starts with the right toolkit.</div>
        <div class='logo-stack'>
          <div class='mini-logo' data-logo='openai'><svg aria-label='OpenAI logo' role='img' viewBox='0 0 256 260'><path d='M239.184 106.203a64.72 64.72 0 0 0-5.576-53.103C219.452 28.459 191 15.784 163.213 21.74A65.586 65.586 0 0 0 52.096 45.22a64.72 64.72 0 0 0-43.23 31.36c-14.31 24.602-11.061 55.634 8.033 76.74a64.67 64.67 0 0 0 5.525 53.102c14.174 24.65 42.644 37.324 70.446 31.36a64.72 64.72 0 0 0 48.754 21.744c28.481.025 53.714-18.361 62.414-45.481a64.77 64.77 0 0 0 43.229-31.36c14.137-24.558 10.875-55.423-8.083-76.483m-97.56 136.338a48.4 48.4 0 0 1-31.105-11.255l1.535-.87l51.67-29.825a8.6 8.6 0 0 0 4.247-7.367v-72.85l21.845 12.636c.218.111.37.32.409.563v60.367c-.056 26.818-21.783 48.545-48.601 48.601M37.158 197.93a48.35 48.35 0 0 1-5.781-32.589l1.534.921l51.722 29.826a8.34 8.34 0 0 0 8.441 0l63.181-36.425v25.221a.87.87 0 0 1-.358.665l-52.335 30.184c-23.257 13.398-52.97 5.431-66.404-17.803M23.549 85.38a48.5 48.5 0 0 1 25.58-21.333v61.39a8.29 8.29 0 0 0 4.195 7.316l62.874 36.272l-21.845 12.636a.82.82 0 0 1-.767 0L41.353 151.53c-23.211-13.454-31.171-43.144-17.804-66.405zm179.466 41.695l-63.08-36.63L161.73 77.86a.82.82 0 0 1 .768 0l52.233 30.184a48.6 48.6 0 0 1-7.316 87.635v-61.391a8.54 8.54 0 0 0-4.4-7.213m21.742-32.69l-1.535-.922l-51.619-30.081a8.39 8.39 0 0 0-8.492 0L99.98 99.808V74.587a.72.72 0 0 1 .307-.665l52.233-30.133a48.652 48.652 0 0 1 72.236 50.391zM88.061 139.097l-21.845-12.585a.87.87 0 0 1-.41-.614V65.685a48.652 48.652 0 0 1 79.757-37.346l-1.535.87l-51.67 29.825a8.6 8.6 0 0 0-4.246 7.367zm11.868-25.58L128.067 97.3l28.188 16.218v32.434l-28.086 16.218l-28.188-16.218z'/></svg></div>
          <div class='mini-logo' data-logo='gemini'><svg aria-label='Google Gemini logo' role='img' style='color:#8E75B2;fill:currentColor' viewBox='0 0 24 24'><path d='M11.04 19.32Q12 21.51 12 24q0-2.49.93-4.68.96-2.19 2.58-3.81t3.81-2.55Q21.51 12 24 12q-2.49 0-4.68-.93a12.3 12.3 0 0 1-3.81-2.58 12.3 12.3 0 0 1-2.58-3.81Q12 2.49 12 0q0 2.49-.96 4.68-.93 2.19-2.55 3.81a12.3 12.3 0 0 1-3.81 2.58Q2.49 12 0 12q2.49 0 4.68.96 2.19.93 3.81 2.55t2.55 3.81'/></svg></div>
          <div class='mini-logo' data-logo='canva'><svg aria-label='Canva logo' role='img' style='color:#00C4CC;fill:currentColor' viewBox='0 0 24 24'><path d='M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zM6.962 7.68c.754 0 1.337.549 1.405 1.2.069.583-.171 1.097-.822 1.406-.343.171-.48.172-.549.069-.034-.069 0-.137.069-.206.617-.514.617-.926.548-1.508-.034-.378-.308-.618-.583-.618-1.2 0-2.914 2.674-2.674 4.629.103.754.549 1.646 1.509 1.646.308 0 .65-.103.96-.24.5-.264.799-.47 1.097-.8-.073-.885.704-2.046 1.851-2.046.515 0 .926.205.96.583.068.514-.377.582-.514.582s-.378-.034-.378-.17c-.034-.138.309-.07.275-.378-.035-.206-.24-.274-.446-.274-.72 0-1.131.994-1.029 1.611.035.275.172.549.447.549.205 0 .514-.31.617-.755.068-.308.343-.514.583-.514.102 0 .17.034.205.171v.138c-.034.137-.137.548-.102.651 0 .069.034.171.17.171.092 0 .436-.18.777-.459.117-.59.253-1.298.253-1.357.034-.24.137-.48.617-.48.103 0 .171.034.205.171v.138l-.136.617c.445-.583 1.097-.994 1.508-.994.172 0 .309.102.309.274 0 .103 0 .274-.069.446-.137.377-.309.96-.412 1.474 0 .137.035.274.207.274.171 0 .685-.206 1.096-.754l.007-.004c-.002-.068-.007-.134-.007-.202 0-.411.035-.754.104-.994.068-.274.411-.514.617-.514.103 0 .205.069.205.171 0 .035 0 .103-.034.137-.137.446-.24.857-.24 1.269 0 .24.034.582.102.788 0 .034.035.069.07.069.068 0 .548-.445.89-1.028-.308-.206-.48-.549-.48-.96 0-.72.446-1.097.858-1.097.343 0 .617.24.617.72 0 .308-.103.65-.274.96h.102a.77.77 0 0 0 .584-.24.293.293 0 0 1 .134-.117c.335-.425.83-.74 1.41-.74.48 0 .924.205.959.582.068.515-.378.618-.515.618l-.002-.002c-.138 0-.377-.035-.377-.172 0-.137.309-.068.274-.376-.034-.206-.24-.275-.446-.275-.686 0-1.13.891-1.028 1.611.034.275.171.583.445.583.206 0 .515-.308.652-.754.068-.274.343-.514.583-.514.103 0 .17.034.205.171 0 .069 0 .206-.137.652-.17.308-.171.48-.137.617.034.274.171.48.309.583.034.034.068.102.068.102 0 .069-.034.138-.137.138-.034 0-.068 0-.103-.035-.514-.205-.72-.548-.789-.891-.205.24-.445.377-.72.377-.445 0-.89-.411-.96-.926a1.609 1.609 0 0 1 .075-.649c-.203.13-.422.203-.623.203h-.17c-.447.652-.927 1.098-1.27 1.303a.896.896 0 0 1-.377.104c-.068 0-.171-.035-.205-.104-.095-.152-.156-.392-.193-.667-.481.527-1.145.805-1.453.805-.343 0-.548-.206-.582-.55v-.376c.102-.754.377-1.2.377-1.337a.074.074 0 0 0-.069-.07c-.24 0-1.028.824-1.166 1.373l-.103.445c-.068.309-.377.515-.582.515-.103 0-.172-.035-.206-.172v-.137l.046-.233c-.435.31-.87.508-1.075.508-.308 0-.48-.172-.514-.412-.206.274-.445.412-.754.412-.352 0-.696-.24-.862-.593-.244.275-.523.553-.852.764-.48.309-1.028.549-1.68.549-.582 0-1.097-.309-1.371-.583-.412-.377-.651-.96-.686-1.509-.205-1.68.823-3.84 2.4-4.8.378-.205.755-.343 1.132-.343zm9.77 3.291c-.104 0-.172.172-.172.343 0 .274.137.583.309.755a1.74 1.74 0 0 0 .102-.583c0-.343-.137-.515-.24-.515z'/></svg></div>
          <div class='mini-logo' data-logo='adobe'><svg aria-label='Adobe logo' role='img' viewBox='0 0 256 227'><path d='m128.024 83.527l60.288 143.042h-39.513l-18.038-45.554H86.642zM256 0v226.54L161.353 0zM94.684 0L0 226.54V0z' fill='#fa0f00'/></svg></div>
        </div>
        <div class='showcase-meta'>
          <div><strong>57</strong><span>Curated premium offers</span></div>
          <div><strong>Email</strong><span>Guided activation available</span></div>
        </div>
      </div>
    </div>
  </header>

  <!-- ============ STORE (homepage only) ============ -->
  <div class='container wrap'>
    <b:section id='main-products' showaddelement='yes'>
      <b:widget id='HTML1' locked='false' title='Store Layout' type='HTML' version='2' visible='true'>
        <b:widget-settings>
          <b:widget-setting name='content'><![CDATA[

            


            
            <!-- ==============================================
                 CATEGORY: AI TOOLS
                 ============================================== -->
            <h2 class="category-title animate-scroll"><small>Original collection • Intelligence, elevated</small>AI Tools</h2>
            <div class="product-grid" id="grid-ai">
              
              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#ffffff,#dff7ee)"><svg role="img" aria-label="OpenAI logo" viewBox="0 0 256 260"><path d="M239.184 106.203a64.72 64.72 0 0 0-5.576-53.103C219.452 28.459 191 15.784 163.213 21.74A65.586 65.586 0 0 0 52.096 45.22a64.72 64.72 0 0 0-43.23 31.36c-14.31 24.602-11.061 55.634 8.033 76.74a64.67 64.67 0 0 0 5.525 53.102c14.174 24.65 42.644 37.324 70.446 31.36a64.72 64.72 0 0 0 48.754 21.744c28.481.025 53.714-18.361 62.414-45.481a64.77 64.77 0 0 0 43.229-31.36c14.137-24.558 10.875-55.423-8.083-76.483m-97.56 136.338a48.4 48.4 0 0 1-31.105-11.255l1.535-.87l51.67-29.825a8.6 8.6 0 0 0 4.247-7.367v-72.85l21.845 12.636c.218.111.37.32.409.563v60.367c-.056 26.818-21.783 48.545-48.601 48.601M37.158 197.93a48.35 48.35 0 0 1-5.781-32.589l1.534.921l51.722 29.826a8.34 8.34 0 0 0 8.441 0l63.181-36.425v25.221a.87.87 0 0 1-.358.665l-52.335 30.184c-23.257 13.398-52.97 5.431-66.404-17.803M23.549 85.38a48.5 48.5 0 0 1 25.58-21.333v61.39a8.29 8.29 0 0 0 4.195 7.316l62.874 36.272l-21.845 12.636a.82.82 0 0 1-.767 0L41.353 151.53c-23.211-13.454-31.171-43.144-17.804-66.405zm179.466 41.695l-63.08-36.63L161.73 77.86a.82.82 0 0 1 .768 0l52.233 30.184a48.6 48.6 0 0 1-7.316 87.635v-61.391a8.54 8.54 0 0 0-4.4-7.213m21.742-32.69l-1.535-.922l-51.619-30.081a8.39 8.39 0 0 0-8.492 0L99.98 99.808V74.587a.72.72 0 0 1 .307-.665l52.233-30.133a48.652 48.652 0 0 1 72.236 50.391zM88.061 139.097l-21.845-12.585a.87.87 0 0 1-.41-.614V65.685a48.652 48.652 0 0 1 79.757-37.346l-1.535.87l-51.67 29.825a8.6 8.6 0 0 0-4.246 7.367zm11.868-25.58L128.067 97.3l28.188 16.218v32.434l-28.086 16.218l-28.188-16.218z"/></svg></div>
                <h3 class="card-title">ChatGPT Plus</h3>
                <div class="product-tagline">"Unleash Your Ultimate Genius."</div>
                <div class="badge">1 Month Access</div>
                <p class="product-desc">Experience the ultimate AI sidekick for lightning-fast coding, writing, and deep research.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> AI Chat, Coding &amp; Writing</li><li><span class="feat-icon">✦</span> Advanced Research Capabilities</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20ChatGPT%20Plus" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#eefeff,#ffffff)"><svg role="img" aria-label="Canva logo" viewBox="0 0 24 24" style="color:#00C4CC;fill:currentColor"><path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zM6.962 7.68c.754 0 1.337.549 1.405 1.2.069.583-.171 1.097-.822 1.406-.343.171-.48.172-.549.069-.034-.069 0-.137.069-.206.617-.514.617-.926.548-1.508-.034-.378-.308-.618-.583-.618-1.2 0-2.914 2.674-2.674 4.629.103.754.549 1.646 1.509 1.646.308 0 .65-.103.96-.24.5-.264.799-.47 1.097-.8-.073-.885.704-2.046 1.851-2.046.515 0 .926.205.96.583.068.514-.377.582-.514.582s-.378-.034-.378-.17c-.034-.138.309-.07.275-.378-.035-.206-.24-.274-.446-.274-.72 0-1.131.994-1.029 1.611.035.275.172.549.447.549.205 0 .514-.31.617-.755.068-.308.343-.514.583-.514.102 0 .17.034.205.171v.138c-.034.137-.137.548-.102.651 0 .069.034.171.17.171.092 0 .436-.18.777-.459.117-.59.253-1.298.253-1.357.034-.24.137-.48.617-.48.103 0 .171.034.205.171v.138l-.136.617c.445-.583 1.097-.994 1.508-.994.172 0 .309.102.309.274 0 .103 0 .274-.069.446-.137.377-.309.96-.412 1.474 0 .137.035.274.207.274.171 0 .685-.206 1.096-.754l.007-.004c-.002-.068-.007-.134-.007-.202 0-.411.035-.754.104-.994.068-.274.411-.514.617-.514.103 0 .205.069.205.171 0 .035 0 .103-.034.137-.137.446-.24.857-.24 1.269 0 .24.034.582.102.788 0 .034.035.069.07.069.068 0 .548-.445.89-1.028-.308-.206-.48-.549-.48-.96 0-.72.446-1.097.858-1.097.343 0 .617.24.617.72 0 .308-.103.65-.274.96h.102a.77.77 0 0 0 .584-.24.293.293 0 0 1 .134-.117c.335-.425.83-.74 1.41-.74.48 0 .924.205.959.582.068.515-.378.618-.515.618l-.002-.002c-.138 0-.377-.035-.377-.172 0-.137.309-.068.274-.376-.034-.206-.24-.275-.446-.275-.686 0-1.13.891-1.028 1.611.034.275.171.583.445.583.206 0 .515-.308.652-.754.068-.274.343-.514.583-.514.103 0 .17.034.205.171 0 .069 0 .206-.137.652-.17.308-.171.48-.137.617.034.274.171.48.309.583.034.034.068.102.068.102 0 .069-.034.138-.137.138-.034 0-.068 0-.103-.035-.514-.205-.72-.548-.789-.891-.205.24-.445.377-.72.377-.445 0-.89-.411-.96-.926a1.609 1.609 0 0 1 .075-.649c-.203.13-.422.203-.623.203h-.17c-.447.652-.927 1.098-1.27 1.303a.896.896 0 0 1-.377.104c-.068 0-.171-.035-.205-.104-.095-.152-.156-.392-.193-.667-.481.527-1.145.805-1.453.805-.343 0-.548-.206-.582-.55v-.376c.102-.754.377-1.2.377-1.337a.074.074 0 0 0-.069-.07c-.24 0-1.028.824-1.166 1.373l-.103.445c-.068.309-.377.515-.582.515-.103 0-.172-.035-.206-.172v-.137l.046-.233c-.435.31-.87.508-1.075.508-.308 0-.48-.172-.514-.412-.206.274-.445.412-.754.412-.352 0-.696-.24-.862-.593-.244.275-.523.553-.852.764-.48.309-1.028.549-1.68.549-.582 0-1.097-.309-1.371-.583-.412-.377-.651-.96-.686-1.509-.205-1.68.823-3.84 2.4-4.8.378-.205.755-.343 1.132-.343zm9.77 3.291c-.104 0-.172.172-.172.343 0 .274.137.583.309.755a1.74 1.74 0 0 0 .102-.583c0-.343-.137-.515-.24-.515z"/></svg></div>
                <h3 class="card-title">Canva Pro</h3>
                <div class="product-tagline">"Design Like a Master."</div>
                <div class="badge">12 Months Access</div>
                <p class="product-desc">Unlock millions of premium assets, templates, and the magical Brand Kit to elevate your visuals.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Premium Templates &amp; Assets</li><li><span class="feat-icon">✦</span> Brand Kit &amp; Magic Studio</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Canva%20Pro" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff,#ececec)"><svg role="img" aria-label="CapCut logo" viewBox="0 0 48 48" style="color:#111111"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M43.5 35.9L4.505 16.242v-1.383a3.717 3.717 0 0 1 3.722-3.728h21.998a3.717 3.717 0 0 1 3.722 3.728v1.695"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="m43.5 11.836l-39 19.66l.005 1.645a3.717 3.717 0 0 0 3.723 3.728h21.996a3.717 3.717 0 0 0 3.723-3.728v-1.948"/></svg></div>
                <h3 class="card-title">CapCut Pro</h3>
                <div class="product-tagline">"Hollywood in Your Hands."</div>
                <div class="badge">1 Month Access</div>
                <p class="product-desc">Create viral masterpieces effortlessly with advanced filters, pro transitions, and premium editing tools.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Premium Video Editing Features</li><li><span class="feat-icon">✦</span> Advanced Effects &amp; Filters</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20CapCut%20Pro" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#171923,#444b63)"><span style="color:#fff">KLING AI</span></div>
                <h3 class="card-title">Kling Pro</h3>
                <div class="product-tagline">"Your Vision, Animated."</div>
                <div class="badge">1,300 Credits</div>
                <p class="product-desc">Turn simple text and images into breathtaking, cinematic AI videos instantly.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Text-to-Video &amp; Image-to-Video</li><li><span class="feat-icon">✦</span> Cinematic AI Video Generation</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Kling%20Pro" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#7b61ff,#ff6bb5)"><span style="color:#fff">HEYGEN</span></div>
                <h3 class="card-title">HeyGen Creator</h3>
                <div class="product-tagline">"The Future of Video Production."</div>
                <div class="badge">Creator Plan</div>
                <p class="product-desc">Produce studio-quality talking avatars and ultra-realistic voiceovers without ever using a camera.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> AI Avatar Videos</li><li><span class="feat-icon">✦</span> Realistic Voiceovers</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20HeyGen%20Creator" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#111827,#6d28d9)"><span style="color:#fff">OPENART</span></div>
                <h3 class="card-title">OpenArt AI</h3>
                <div class="product-tagline">"Paint with Algorithms."</div>
                <div class="badge">Essential / Advance Plan</div>
                <p class="product-desc">Generate stunning professional artwork and photorealistic images with unparalleled AI precision.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Advanced AI Image Generation</li><li><span class="feat-icon">✦</span> Professional Artwork Creation</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20OpenArt%20AI" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff,#ececec)"><svg role="img" aria-label="ElevenLabs logo" viewBox="0 0 24 24" style="color:#111111;fill:currentColor"><path d="M4.6035 0v24h4.9317V0zm9.8613 0v24h4.9317V0z"/></svg></div>
                <h3 class="card-title">ElevenLabs Creator</h3>
                <div class="product-tagline">"Give Your Words Life."</div>
                <div class="badge">Creator Plan</div>
                <p class="product-desc">Clone voices or generate hyper-realistic text-to-speech audio that sounds 100% authentically human.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> AI Voice Generation</li><li><span class="feat-icon">✦</span> Voice Cloning &amp; Text-to-Speech</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20ElevenLabs%20Creator" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#17112e,#8459ff)"><span style="color:#fff">LEONARDO.AI</span></div>
                <h3 class="card-title">Leonardo AI</h3>
                <div class="product-tagline">"Dream It, Build It."</div>
                <div class="badge">1 Month Access</div>
                <p class="product-desc">Craft mesmerizing concept art, product designs, and high-quality game assets with ultimate creative control.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> AI Concept Art Generation</li><li><span class="feat-icon">✦</span> Product Design &amp; Rendering</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Leonardo%20AI" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#eef4ff,#ffffff)"><svg role="img" aria-label="Google Gemini logo" viewBox="0 0 24 24" style="color:#8E75B2;fill:currentColor"><path d="M11.04 19.32Q12 21.51 12 24q0-2.49.93-4.68.96-2.19 2.58-3.81t3.81-2.55Q21.51 12 24 12q-2.49 0-4.68-.93a12.3 12.3 0 0 1-3.81-2.58 12.3 12.3 0 0 1-2.58-3.81Q12 2.49 12 0q0 2.49-.96 4.68-.93 2.19-2.55 3.81a12.3 12.3 0 0 1-3.81 2.58Q2.49 12 0 12q2.49 0 4.68.96 2.19.93 3.81 2.55t2.55 3.81"/></svg></div>
                <h3 class="card-title">Gemini Pro</h3>
                <div class="product-tagline">"Google's Best, Unlocked."</div>
                <div class="badge">12/18 Months</div>
                <p class="product-desc">Supercharge your productivity with advanced reasoning, coding, and ultra-smart AI assistance.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Google's Premium AI</li><li><span class="feat-icon">✦</span> Advanced Reasoning Assistant</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Gemini%20Pro" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff,#e9e9e9)"><svg role="img" aria-label="Grok logo" viewBox="0 0 256 246"><path d="M63.83 56.843c27.469-27.48 67.635-34.865 101.712-21.87l2.314.917c7.645 2.844 14.309 6.89 19.507 10.651l-28.857 13.342c-26.869-11.286-57.649-3.609-76.435 15.2c-25.405 25.414-30.539 69.484-.764 97.96L0 245.764c4.296-5.923 9.457-11.573 14.75-17.178l5.815-6.13l2.608-2.774c15.53-16.655 28.81-33.77 20.496-56.709l-.766-1.98c-14.592-35.497-6.094-77.096 20.928-104.15m156.956-21.587L256 0l-10.128 14.069c-21.094 29.716-30.456 48.424-21.11 88.659l-.065-.065c7.23 30.728-.503 64.803-25.472 89.802c-31.478 31.538-81.852 38.558-123.336 10.17l28.923-13.407c26.476 10.41 55.442 5.839 76.26-15.003c20.818-20.844 25.493-51.2 15.03-76.462c-1.989-4.79-7.952-5.992-12.125-2.909L98.87 157.755L220.786 35.147z"/></svg></div>
                <h3 class="card-title">Super Grok</h3>
                <div class="product-tagline">"Unfiltered Rebel Intelligence."</div>
                <div class="badge">Premium Plans</div>
                <p class="product-desc">Access xAI's cutting-edge assistant for real-time insights, coding, and witty, advanced research.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> xAI Premium Access</li><li><span class="feat-icon">✦</span> Advanced Real-Time AI Assistant</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Super%20Grok" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>
            </div>

            <!-- ==============================================
                 CATEGORY: PRODUCTIVITY
                 ============================================== -->
            <h2 class="category-title animate-scroll"><small>Work without limits</small>Productivity</h2>
            <div class="product-grid" id="grid-prod">
              
              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#eefeff,#ffffff)"><svg role="img" aria-label="Canva logo" viewBox="0 0 24 24" style="color:#00C4CC;fill:currentColor"><path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zM6.962 7.68c.754 0 1.337.549 1.405 1.2.069.583-.171 1.097-.822 1.406-.343.171-.48.172-.549.069-.034-.069 0-.137.069-.206.617-.514.617-.926.548-1.508-.034-.378-.308-.618-.583-.618-1.2 0-2.914 2.674-2.674 4.629.103.754.549 1.646 1.509 1.646.308 0 .65-.103.96-.24.5-.264.799-.47 1.097-.8-.073-.885.704-2.046 1.851-2.046.515 0 .926.205.96.583.068.514-.377.582-.514.582s-.378-.034-.378-.17c-.034-.138.309-.07.275-.378-.035-.206-.24-.274-.446-.274-.72 0-1.131.994-1.029 1.611.035.275.172.549.447.549.205 0 .514-.31.617-.755.068-.308.343-.514.583-.514.102 0 .17.034.205.171v.138c-.034.137-.137.548-.102.651 0 .069.034.171.17.171.092 0 .436-.18.777-.459.117-.59.253-1.298.253-1.357.034-.24.137-.48.617-.48.103 0 .171.034.205.171v.138l-.136.617c.445-.583 1.097-.994 1.508-.994.172 0 .309.102.309.274 0 .103 0 .274-.069.446-.137.377-.309.96-.412 1.474 0 .137.035.274.207.274.171 0 .685-.206 1.096-.754l.007-.004c-.002-.068-.007-.134-.007-.202 0-.411.035-.754.104-.994.068-.274.411-.514.617-.514.103 0 .205.069.205.171 0 .035 0 .103-.034.137-.137.446-.24.857-.24 1.269 0 .24.034.582.102.788 0 .034.035.069.07.069.068 0 .548-.445.89-1.028-.308-.206-.48-.549-.48-.96 0-.72.446-1.097.858-1.097.343 0 .617.24.617.72 0 .308-.103.65-.274.96h.102a.77.77 0 0 0 .584-.24.293.293 0 0 1 .134-.117c.335-.425.83-.74 1.41-.74.48 0 .924.205.959.582.068.515-.378.618-.515.618l-.002-.002c-.138 0-.377-.035-.377-.172 0-.137.309-.068.274-.376-.034-.206-.24-.275-.446-.275-.686 0-1.13.891-1.028 1.611.034.275.171.583.445.583.206 0 .515-.308.652-.754.068-.274.343-.514.583-.514.103 0 .17.034.205.171 0 .069 0 .206-.137.652-.17.308-.171.48-.137.617.034.274.171.48.309.583.034.034.068.102.068.102 0 .069-.034.138-.137.138-.034 0-.068 0-.103-.035-.514-.205-.72-.548-.789-.891-.205.24-.445.377-.72.377-.445 0-.89-.411-.96-.926a1.609 1.609 0 0 1 .075-.649c-.203.13-.422.203-.623.203h-.17c-.447.652-.927 1.098-1.27 1.303a.896.896 0 0 1-.377.104c-.068 0-.171-.035-.205-.104-.095-.152-.156-.392-.193-.667-.481.527-1.145.805-1.453.805-.343 0-.548-.206-.582-.55v-.376c.102-.754.377-1.2.377-1.337a.074.074 0 0 0-.069-.07c-.24 0-1.028.824-1.166 1.373l-.103.445c-.068.309-.377.515-.582.515-.103 0-.172-.035-.206-.172v-.137l.046-.233c-.435.31-.87.508-1.075.508-.308 0-.48-.172-.514-.412-.206.274-.445.412-.754.412-.352 0-.696-.24-.862-.593-.244.275-.523.553-.852.764-.48.309-1.028.549-1.68.549-.582 0-1.097-.309-1.371-.583-.412-.377-.651-.96-.686-1.509-.205-1.68.823-3.84 2.4-4.8.378-.205.755-.343 1.132-.343zm9.77 3.291c-.104 0-.172.172-.172.343 0 .274.137.583.309.755a1.74 1.74 0 0 0 .102-.583c0-.343-.137-.515-.24-.515z"/></svg></div>
                <h3 class="card-title">Canva Admin Panel</h3>
                <div class="product-tagline">"Empower Your Entire Team."</div>
                <div class="badge">3 Months Access</div>
                <p class="product-desc">Manage multiple accounts seamlessly with ultimate team collaboration and premium feature sharing.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Team Collaboration Control</li><li><span class="feat-icon">✦</span> Distribute Premium Features</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Canva%20Admin%20Panel" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#f7f7ff,#dfe2ff)"><svg role="img" aria-label="Framer logo" viewBox="0 0 256 384"><path d="M0 0h256v128H128zm0 128h128l128 128H128v128L0 256z"/></svg></div>
                <h3 class="card-title">Framer Pro</h3>
                <div class="product-tagline">"Ship Sites Faster Than Ever."</div>
                <div class="badge">1 Month Access</div>
                <p class="product-desc">Build interactive, high-performance websites visually with AI-powered prototyping and design.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> AI Website Builder</li><li><span class="feat-icon">✦</span> Advanced Design Prototyping</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Framer%20Pro" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#1a1740,#6255d9)"><span style="color:#fff">FLOURISH</span></div>
                <h3 class="card-title">Flourish</h3>
                <div class="product-tagline">"Data Made Beautiful."</div>
                <div class="badge">1 Month Access</div>
                <p class="product-desc">Transform boring spreadsheets into interactive, stunning charts and animated visual stories.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Interactive Data Visualization</li><li><span class="feat-icon">✦</span> Animated Charts &amp; Maps</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Flourish" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff,#f0edff)"><svg aria-label="AI video ideas" role="img" viewBox="0 0 24 24"><path fill="#6d4aff" d="m12 1 1.9 5.1L19 8l-5.1 1.9L12 15l-1.9-5.1L5 8l5.1-1.9L12 1Z"/><path fill="#ff4f98" d="m18.5 13 1 2.5L22 16.5l-2.5 1-1 2.5-1-2.5-2.5-1 2.5-1 1-2.5Z"/><path fill="#18b6a4" d="m6 14 1.2 3.2L10.5 18l-3.3 1.2L6 22.5l-1.2-3.3L1.5 18l3.3-.8L6 14Z"/></svg></div>
                <h3 class="card-title">Video Ideas AI</h3>
                <div class="product-tagline">"Go Viral on Demand."</div>
                <div class="badge">Premium Access</div>
                <p class="product-desc">Never run out of content. Generate highly engaging viral video scripts and creative concepts instantly.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Viral Content Ideas</li><li><span class="feat-icon">✦</span> Automated Script Generation</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Video%20Ideas%20AI" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff,#ececec)"><svg role="img" aria-label="RoboForm logo" viewBox="0 0 48 48" style="color:#149747"><rect width="34.231" height="26.437" x="7.009" y="5.5" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" rx="6.921" ry="6.921"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M12.029 31.963H35.97a5.27 5.27 0 0 1 5.27 5.268h0a5.27 5.27 0 0 1-5.27 5.27H12.03a5.27 5.27 0 0 1-5.27-5.27h0a5.27 5.27 0 0 1 5.27-5.268m8.895-13.31a3.703 3.703 0 1 1 0-.026m6.525.026a3.703 3.703 0 1 0 0-.026"/></svg></div>
                <h3 class="card-title">RoboForm Premium</h3>
                <div class="product-tagline">"Unbreakable Digital Security."</div>
                <div class="badge">12 Months Access</div>
                <p class="product-desc">Keep your digital life safe with military-grade password management and a highly secure vault.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Premium Password Manager</li><li><span class="feat-icon">✦</span> Encrypted Secure Vault</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20RoboForm%20Premium" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>
            </div>

            <!-- ==============================================
                 CATEGORY: BUSINESS TOOLS
                 ============================================== -->
            <h2 class="category-title animate-scroll"><small>Build your advantage</small>Business Tools</h2>
            <div class="product-grid" id="grid-biz">
              
              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#f1f8ff,#ffffff)"><svg role="img" aria-label="LinkedIn logo" viewBox="0 0 256 256"><path fill="#0a66c2" d="M218.123 218.127h-37.931v-59.403c0-14.165-.253-32.4-19.728-32.4c-19.756 0-22.779 15.434-22.779 31.369v60.43h-37.93V95.967h36.413v16.694h.51a39.91 39.91 0 0 1 35.928-19.733c38.445 0 45.533 25.288 45.533 58.186zM56.955 79.27c-12.157.002-22.014-9.852-22.016-22.009s9.851-22.014 22.008-22.016c12.157-.003 22.014 9.851 22.016 22.008A22.013 22.013 0 0 1 56.955 79.27m18.966 138.858H37.95V95.967h37.97zM237.033.018H18.89C8.58-.098.125 8.161-.001 18.471v219.053c.122 10.315 8.576 18.582 18.89 18.474h218.144c10.336.128 18.823-8.139 18.966-18.474V18.454c-.147-10.33-8.635-18.588-18.966-18.453"/></svg></div>
                <h3 class="card-title">LinkedIn Premium</h3>
                <div class="product-tagline">"Accelerate Your Career."</div>
                <div class="badge">Premium Profile</div>
                <p class="product-desc">Unlock top-tier networking, exclusive job insights, and unlimited InMail to land your dream role.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Advanced Job Search &amp; InMail</li><li><span class="feat-icon">✦</span> LinkedIn Learning Included</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20LinkedIn%20Premium" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#eef5ff,#ffffff)"><svg role="img" aria-label="Coursera logo" viewBox="0 0 24 24" style="color:#0056D2;fill:currentColor"><path d="M11.374 23.977c-4.183-.21-8.006-2.626-9.959-6.347-2.097-3.858-1.871-8.864.732-12.454C4.748 1.338 9.497-.698 14.281.23c4.583.857 8.351 4.494 9.358 8.911 1.122 4.344-.423 9.173-3.925 12.04-2.289 1.953-5.295 2.956-8.34 2.797zm7.705-8.05a588.737 588.737 0 0 0-3.171-1.887c-.903 1.483-2.885 2.248-4.57 1.665-2.024-.639-3.394-2.987-2.488-5.134.801-2.009 2.79-2.707 4.357-2.464a4.19 4.19 0 0 1 2.623 1.669c1.077-.631 2.128-1.218 3.173-1.855-2.03-3.118-6.151-4.294-9.656-2.754-3.13 1.423-4.89 4.68-4.388 7.919.54 3.598 3.73 6.486 7.716 6.404a7.664 7.664 0 0 0 6.404-3.563z"/></svg></div>
                <h3 class="card-title">Coursera Premium</h3>
                <div class="product-tagline">"Master Any Skill."</div>
                <div class="badge">Premium Courses</div>
                <p class="product-desc">Learn from top global universities and earn professional certificates to skyrocket your career.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Professional Certifications</li><li><span class="feat-icon">✦</span> Unlimited Premium Course Access</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Coursera%20Premium" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>
            </div>

            <!-- ==============================================
                 CATEGORY: ENTERTAINMENT
                 ============================================== -->
            <h2 class="category-title animate-scroll"><small>Premium downtime</small>Entertainment</h2>
            <div class="product-grid" id="grid-ent">
              
              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#181818,#050505)"><svg role="img" aria-label="Spotify logo" viewBox="0 0 256 256"><path fill="#1ed760" d="M128 0C57.308 0 0 57.309 0 128c0 70.696 57.309 128 128 128c70.697 0 128-57.304 128-128C256 57.314 198.697.007 127.998.007zm58.699 184.614c-2.293 3.76-7.215 4.952-10.975 2.644c-30.053-18.357-67.885-22.515-112.44-12.335a7.98 7.98 0 0 1-9.552-6.007a7.97 7.97 0 0 1 6-9.553c48.76-11.14 90.583-6.344 124.323 14.276c3.76 2.308 4.952 7.215 2.644 10.975m15.667-34.853c-2.89 4.695-9.034 6.178-13.726 3.289c-34.406-21.148-86.853-27.273-127.548-14.92c-5.278 1.594-10.852-1.38-12.454-6.649c-1.59-5.278 1.386-10.842 6.655-12.446c46.485-14.106 104.275-7.273 143.787 17.007c4.692 2.89 6.175 9.034 3.286 13.72zm1.345-36.293C162.457 88.964 94.394 86.71 55.007 98.666c-6.325 1.918-13.014-1.653-14.93-7.978c-1.917-6.328 1.65-13.012 7.98-14.935C93.27 62.027 168.434 64.68 215.929 92.876c5.702 3.376 7.566 10.724 4.188 16.405c-3.362 5.69-10.73 7.565-16.4 4.187z"/></svg></div>
                <h3 class="card-title">Spotify Premium</h3>
                <div class="product-tagline">"Your Soundtrack, Uninterrupted."</div>
                <div class="badge">Individual Plan</div>
                <p class="product-desc">Immerse yourself in ad-free music, offline listening, and crystal-clear audio quality everywhere.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Ad-Free Music Streaming</li><li><span class="feat-icon">✦</span> Offline Downloads Supported</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Spotify%20Premium" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#181818,#000000)"><svg role="img" aria-label="Netflix logo" viewBox="0 0 256 256"><defs><path id="SVG8fYEGcDn" fill="#b1060f" stroke="#000" d="m141.676 41.275l-.067 38.361l-.068 38.361l-3.156-8.905l-.006-.017l-4.078 85.402c4.01 11.324 6.158 17.369 6.182 17.393c.031.032 2.317.17 5.078.307c8.366.415 18.734 1.304 26.599 2.282c1.821.226 3.388.342 3.483.257c.094-.084.145-39.143.114-86.797l-.058-86.644zm-61.538-.115v86.732c0 47.703.047 86.779.104 86.836s3.011-.222 6.565-.62c3.553-.398 8.465-.893 10.914-1.1c3.756-.317 14.97-1.038 16.268-1.046c.378-.002.402-1.95.457-36.735l.058-36.734l2.713 7.677l.96 2.713l4.077-85.381l-1.401-3.96a32066 32066 0 0 0-6.283-17.754l-.225-.628z"/><path id="SVGk3mpMeLQ" fill="url(#SVG4ILQC65E)" d="M80.138 41.16v48.685l34.296 90.976c.004-2.085.008-3.211.012-5.594l.058-36.734l2.713 7.677c15.104 42.738 23.218 65.652 23.266 65.7c.031.032 2.317.17 5.078.307c8.366.415 18.734 1.304 26.599 2.282c1.821.226 3.388.342 3.483.257c.064-.058.107-19.21.118-46.227l-34.136-98.14l-.016 9.287l-.068 38.361l-3.156-8.905c-3.084-8.701-5.143-14.52-17.532-49.55a32066 32066 0 0 0-6.283-17.754l-.225-.628z"/><path id="SVGVthXec6c" fill="#e50914" d="m80.139 41.16l34.365 97.377v-.044l2.713 7.677c15.104 42.738 23.218 65.652 23.266 65.7c.031.032 2.317.17 5.078.307c8.366.415 18.734 1.304 26.599 2.282c1.812.225 3.37.34 3.48.258l-34.1-96.737v.017l-3.156-8.905c-3.084-8.701-5.143-14.52-17.532-49.55c-3.332-9.42-6.159-17.408-6.283-17.754l-.225-.628z"/><radialGradient id="SVG4ILQC65E" cx="48.34%" cy="49.419%" r="70.438%" fx="48.34%" fy="49.419%" gradientTransform="matrix(1 0 0 .55088 0 .222)"><stop offset="0%"/><stop offset="100%" stop-opacity="0"/></radialGradient></defs><path d="M0 0h255.904v255.904H0z"/><use href="#SVG8fYEGcDn" stroke-width="2.956"/><use href="#SVGk3mpMeLQ"/><use href="#SVGVthXec6c"/><use href="#SVG8fYEGcDn" stroke-width="2.956"/><use href="#SVGk3mpMeLQ"/><use href="#SVGVthXec6c"/></svg></div>
                <h3 class="card-title">Netflix Premium</h3>
                <div class="product-tagline">"The Ultimate Cinema Experience."</div>
                <div class="badge">4K UHD Access</div>
                <p class="product-desc">Stream award-winning shows and movies in breathtaking 4K UHD and HDR on multiple devices.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> 4K UHD &amp; HDR Streaming</li><li><span class="feat-icon">✦</span> Multi-Device Support</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Netflix%20Premium" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#ffffff,#f3f3f3)"><svg role="img" aria-label="YouTube logo" viewBox="0 0 256 180"><path fill="red" d="M250.346 28.075A32.18 32.18 0 0 0 227.69 5.418C207.824 0 127.87 0 127.87 0S47.912.164 28.046 5.582A32.18 32.18 0 0 0 5.39 28.24c-6.009 35.298-8.34 89.084.165 122.97a32.18 32.18 0 0 0 22.656 22.657c19.866 5.418 99.822 5.418 99.822 5.418s79.955 0 99.82-5.418a32.18 32.18 0 0 0 22.657-22.657c6.338-35.348 8.291-89.1-.164-123.134"/><path fill="#fff" d="m102.421 128.06l66.328-38.418l-66.328-38.418z"/></svg></div>
                <h3 class="card-title">YouTube Premium</h3>
                <div class="product-tagline">"Pure Video Bliss."</div>
                <div class="badge">Premium Access</div>
                <p class="product-desc">Enjoy zero ads, uninterrupted background play, and offline video downloads for a flawless journey.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Ad-Free Videos</li><li><span class="feat-icon">✦</span> Background Play &amp; Downloads</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20YouTube%20Premium" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#effbff,#ffffff)"><svg role="img" aria-label="Amazon Prime Video logo" viewBox="0 0 48 48" style="color:#00A8E1"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="m15.993 20.125l-2 5.3l-2-5.3"/><rect width="4" height="5.3" x="32.007" y="20.215" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" rx="2"/><circle cx="18.007" cy="17.675" r=".7" fill="currentColor"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M18.007 20.125v5.3m11.738-1.009a2 2 0 0 1-1.738 1.009h0a2 2 0 0 1-2-2v-1.3a2 2 0 0 1 2-2h0a2 2 0 0 1 2 2v.65h-4m-2-.65a2 2 0 0 0-2-2h0a2 2 0 0 0-2 2v1.3a2 2 0 0 0 2 2h0a2 2 0 0 0 2-2m0 2v-8"/><circle cx="24" cy="24" r="21.5" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M32.28 29.406c1.113-.45 3.092-1.05 3.688-.327c.644.781-.17 2.477-.92 3.794"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M11.798 29.929c1.759 1.396 6.954 3.534 12.488 3.534a17 17 0 0 0 10.167-3.08"/></svg></div>
                <h3 class="card-title">Amazon Prime Video</h3>
                <div class="product-tagline">"Binge Without Limits."</div>
                <div class="badge">Premium Access</div>
                <p class="product-desc">Dive into exclusive blockbuster movies, hit TV shows, and award-winning Amazon Originals ad-free.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Ad-Free Video Streaming</li><li><span class="feat-icon">✦</span> Exclusive Amazon Originals</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Amazon%20Prime%20Video" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon multi" style="background:linear-gradient(145deg,#fff,#f4f4f4)"><svg role="img" aria-label="ZEE5 logo" viewBox="0 0 48 48" style="color:#7b2cff"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M25.291 27.547h3.667m-3.667-7.334h3.667m-3.667 3.667h2.383m-2.383-3.667v7.334m8.112-.143h3.667m-3.667-7.335h3.667m-3.667 3.667h2.383m-2.383-3.667v7.335m-16.575-7.388h4.859l-4.859 7.334h4.859m19.146-.485a2.88 2.88 0 0 0 2.2.642h.275a2.427 2.427 0 0 0 2.384-2.384h0a2.427 2.427 0 0 0-2.384-2.384h-2.475v-2.567h4.86"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M19.951 36.955A13.189 13.189 0 0 1 25.642 11.2"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M30.637 40.992a17.935 17.935 0 1 1 1.55-32.417"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="M23.405 45.5a21.502 21.502 0 0 1 .277-43"/></svg><svg role="img" aria-label="JioHotstar logo" viewBox="0 0 48 48" style="color:#2056e8"><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" d="m21.834 17.238l3.22-10.01l.936 11.064L42.5 7.462L29.035 22.506L38.109 30l-12.06-2.986l-5.445 13.759l.176-13.232l-10.42 2.635l7.259-6.03L5.5 18.116l12.997 1.288l-3.044-6.147z"/></svg><span style="font:900 .65em Plus Jakarta Sans,sans-serif;color:#e51f55">aha</span></div>
                <h3 class="card-title">ZEE5, Hotstar &amp; Aha</h3>
                <div class="product-tagline">"Endless Desi Entertainment."</div>
                <div class="badge">Premium Bundles</div>
                <p class="product-desc">Get unlimited access to the biggest Indian blockbusters, live sports, and premium regional web series.</p>
                <ul class="features"><li><span class="feat-icon">✦</span> Live Sports &amp; Blockbusters</li><li><span class="feat-icon">✦</span> Premium Regional Content</li></ul>
                <a href="https://wa.me/919071145694?text=Hi,%20I%20want%20to%20know%20the%20price%20for%20Zee5,%20Hotstar%20and%20Aha" target="_blank" rel="noopener" class="dm-btn">DM for Price</a>
              </div>
            </div>



            <!-- ==============================================
                 NEWLY ADDED: AI & BUSINESS TOOLS
                 ============================================== -->
            <h2 class="category-title animate-scroll"><small>Fresh arrivals • unbeatable value</small>Newly Added AI &amp; Business Tools</h2>
            <div class="launch-banner animate-scroll">
              <div><strong>Powerful new tools. Exceptional plans.</strong><span>Choose your tool and message us for the latest available price.</span></div>
              <div class="email-chip">✓ Activation on your email</div>
            </div>
            <div class="product-grid" id="grid-new">
              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#5b4bff,#8f83ff)"><span style="color:#fff">INDY</span></div>
                <h3 class="card-title">Indy Pro</h3>
                <div class="product-tagline">“Run your independent business with confidence!”</div>
                <div class="badge">12 Months</div>
                <p class="product-desc">Bring proposals, contracts, invoices, tasks and client communication into one polished freelance workspace.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Professional client documents</li><li><span class="feat-icon">✓</span> Projects, billing and workflow tools</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Indy%20Pro%20%E2%80%94%2012%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#111,#343434)"><span style="color:#fff">MOBBIN</span></div>
                <h3 class="card-title">Mobbin Team</h3>
                <div class="product-tagline">“Turn the world’s best interfaces into your advantage!”</div>
                <div class="badge">1 Year • 10 Seats</div>
                <p class="product-desc">Explore real mobile and web product flows to research patterns, sharpen UX decisions and design faster as a team.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Curated UI and UX reference library</li><li><span class="feat-icon">✓</span> Team research for up to 10 seats</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Mobbin%20Team%20%E2%80%94%201%20Year%20%E2%80%A2%2010%20Seats" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#6626ff,#ae72ff)"><span style="color:#fff">ChatPRD</span></div>
                <h3 class="card-title">ChatPRD Pro</h3>
                <div class="product-tagline">“Go from rough idea to product-ready clarity!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Use an AI product partner to draft PRDs, refine requirements and turn customer problems into actionable plans.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> AI-assisted product documentation</li><li><span class="feat-icon">✓</span> Faster requirements and strategy work</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20ChatPRD%20Pro%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#eeff57,#a2ea23)"><span style="color:#111">GUMLOOP</span></div>
                <h3 class="card-title">Gumloop AI Pro</h3>
                <div class="product-tagline">“Automate the busywork and reclaim your day!”</div>
                <div class="badge">12 Months</div>
                <p class="product-desc">Build powerful no-code AI workflows that connect apps, process information and automate repetitive business tasks.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Visual AI workflow automation</li><li><span class="feat-icon">✓</span> Connect data, models and business tools</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Gumloop%20AI%20Pro%20%E2%80%94%2012%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#effff2,#fff)"><svg role="img" aria-label="MongoDB logo" viewBox="0 0 24 24" style="color:#47A248;fill:currentColor"><path d="M17.193 9.555c-1.264-5.58-4.252-7.414-4.573-8.115-.28-.394-.53-.954-.735-1.44-.036.495-.055.685-.523 1.184-.723.566-4.438 3.682-4.74 10.02-.282 5.912 4.27 9.435 4.888 9.884l.07.05A73.49 73.49 0 0111.91 24h.481c.114-1.032.284-2.056.51-3.07.417-.296.604-.463.85-.693a11.342 11.342 0 003.639-8.464c.01-.814-.103-1.662-.197-2.218zm-5.336 8.195s0-8.291.275-8.29c.213 0 .49 10.695.49 10.695-.381-.045-.765-1.76-.765-2.405z"/></svg></div>
                <h3 class="card-title">MongoDB Atlas</h3>
                <div class="product-tagline">“Give your next application room to scale!”</div>
                <div class="badge">$110 Cloud Credits</div>
                <p class="product-desc">Build modern applications with a flexible cloud database suited to operational data, search and AI-powered experiences.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Managed cloud database credits</li><li><span class="feat-icon">✓</span> Flexible data and vector-search workflows</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20MongoDB%20Atlas%20%E2%80%94%20%24110%20Cloud%20Credits" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#0369a1,#38bdf8)"><span style="color:#fff">XINTERVIEW</span></div>
                <h3 class="card-title">XInterview AI</h3>
                <div class="product-tagline">“Screen talent faster without losing the human touch!”</div>
                <div class="badge">Launch Plan • 2 Months</div>
                <p class="product-desc">Streamline early-stage hiring with structured video interviews and AI-supported candidate evaluation.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Asynchronous candidate interviews</li><li><span class="feat-icon">✓</span> Faster screening and hiring workflows</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20XInterview%20AI%20%E2%80%94%20Launch%20Plan%20%E2%80%A2%202%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#4a3aff,#8c7cff)"><span style="color:#fff">SLITE</span></div>
                <h3 class="card-title">Slite</h3>
                <div class="product-tagline">“Make company knowledge effortless to find!”</div>
                <div class="badge">Premium Team Wiki • 1 Year</div>
                <p class="product-desc">Create a calm, searchable team knowledge base for documentation, decisions, onboarding and AI-assisted answers.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Collaborative team documentation</li><li><span class="feat-icon">✓</span> Fast knowledge search and discovery</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Slite%20%E2%80%94%20Premium%20Team%20Wiki%20%E2%80%A2%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff1f1,#fff)"><svg role="img" aria-label="Raycast logo" viewBox="0 0 24 24" style="color:#FF6363;fill:currentColor"><path d="M6.004 15.492v2.504L0 11.992l1.258-1.249Zm2.504 2.504H6.004L12.008 24l1.253-1.253zm14.24-4.747L24 11.997 12.003 0 10.75 1.251 15.491 6h-2.865L9.317 2.692 8.065 3.944l2.06 2.06H8.691v9.31H18v-1.432l2.06 2.06 1.252-1.252-3.312-3.32V8.506ZM6.63 5.372 5.38 6.625l1.342 1.343 1.251-1.253Zm10.655 10.655-1.247 1.251 1.342 1.343 1.253-1.251zM3.944 8.059 2.692 9.31l3.312 3.314v-2.506zm9.936 9.937h-2.504l3.314 3.312 1.25-1.252z"/></svg></div>
                <h3 class="card-title">Raycast Pro</h3>
                <div class="product-tagline">“Command your Mac at the speed of thought!”</div>
                <div class="badge">12 Months</div>
                <p class="product-desc">Launch apps, automate actions, search information and use AI from one beautifully fast keyboard-first command bar.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Powerful launcher and extensions</li><li><span class="feat-icon">✓</span> AI commands and productivity workflows</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Raycast%20Pro%20%E2%80%94%2012%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#0f766e,#2dd4bf)"><span style="color:#fff">LEADS.CM</span></div>
                <h3 class="card-title">Leads.CM</h3>
                <div class="product-tagline">“Keep every opportunity moving forward!”</div>
                <div class="badge">6 Months</div>
                <p class="product-desc">Organize prospects and outreach in a focused lead-management workspace built to support consistent sales activity.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Lead organization and follow-up</li><li><span class="feat-icon">✓</span> Clearer sales workflow visibility</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Leads.CM%20%E2%80%94%206%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#eaffff,#fff)"><svg role="img" aria-label="Perplexity logo" viewBox="0 0 256 298"><path fill="#3f7e8b" d="m34.831 0l84.689 78.028V.18h16.486v78.197L221.074 0v88.964H256v128.322h-34.819v79.218l-85.175-74.833v75.692H119.52v-74.459l-84.593 74.508v-80.126H0V88.964h34.831zm72.26 105.248H16.487v95.753h18.42v-30.204zm-55.68 72.775v83.052l68.109-59.988v-84.926zm85.069 22.27v-84.212l68.128 61.865v39.34h.088v42.94zm84.701.708h18.333v-95.753h-89.93l71.597 64.87zM204.588 88.964V37.457l-55.904 51.507zm-97.368 0H51.317V37.457z"/></svg></div>
                <h3 class="card-title">Perplexity AI</h3>
                <div class="product-tagline">“Research with answers you can verify!”</div>
                <div class="badge">Enterprise Pro • 1 Month</div>
                <p class="product-desc">Search the web through an AI answer engine designed for fast research, clear summaries and source-backed discovery.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> AI-powered research and answers</li><li><span class="feat-icon">✓</span> Source-aware web discovery</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Perplexity%20AI%20%E2%80%94%20Enterprise%20Pro%20%E2%80%A2%201%20Month" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#ea580c,#fb923c)"><span style="color:#fff">SNAP LEADS</span></div>
                <h3 class="card-title">Snap Leads Pro</h3>
                <div class="product-tagline">“Turn prospecting into a repeatable growth engine!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Discover, organize and manage potential customers with tools created to speed up lead-generation workflows.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Faster prospect discovery</li><li><span class="feat-icon">✓</span> Organized lead-generation workflow</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Snap%20Leads%20Pro%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff0f5,#fff)"><svg role="img" aria-label="Appwrite logo" viewBox="0 0 256 171"><path fill="#f02e65" d="M128.019 11.498C140.579 4.209 155.174.036 170.743.036C217.83.036 256 38.206 256 85.293s-38.17 85.258-85.257 85.258c-15.563 0-30.152-4.17-42.71-11.453c-28.765 16.635-65.89 15.525-94.082-5.75a85.257 85.257 0 0 1 94.068-141.85M29.815 43.419c-23.126 30.647-17.03 74.238 13.616 97.365s74.239 17.03 97.366-13.616c15.491-20.53 17.87-46.867 8.54-68.972c-6.853-16.133-19.627-29.144-35.596-36.305l.036-.034C84.841 8.838 49.736 17.021 29.815 43.42m61.54 12.028c2.61 0 3.464.15 3.313.6c-.073.171-.288.966-.576 2.118l-.111.448c-.286 1.16-.628 2.602-.97 4.108a1986 1986 0 0 1-2.985 12.71l-.225.947l-1.106 4.663c-1.605 6.775-3.613 15.408-4.518 19.171l-1.555 6.928h-3.464c-1.906 0-3.463-.203-3.463-.452c0-.904 1.506-7.73 4.018-18.118c1.302-5.672 3.611-15.257 5.068-21.33a504 504 0 0 1 2.064-8.592l.107-.423c.36-1.432.597-2.328.639-2.43c.098-.199 1.806-.348 3.764-.348M69.473 72.509c2.308 0 4.216.15 4.216.351c0 .25-1.808 2.361-4.015 4.82c-2.21 2.409-4.017 4.666-4.017 5.018c0 .3 1.957 2.71 4.318 5.217l4.316 4.669h-9.135l-3.212-3.412c-1.756-1.857-3.817-4.117-4.567-5.02l-1.356-1.605l4.617-5.02l4.67-5.018Zm35.083 0l4.514 4.87c2.51 2.659 4.518 5.018 4.518 5.268c0 .3-1.906 2.612-4.267 5.22l-4.264 4.667l-4.668.05h-4.666l4.164-4.568c2.308-2.459 4.216-4.816 4.316-5.169c.15-.65-2.61-3.965-6.527-7.879c-1.052-1.054-1.906-2.007-1.906-2.159c0-.15 1.957-.3 4.417-.3z"/></svg></div>
                <h3 class="card-title">Appwrite Pro</h3>
                <div class="product-tagline">“Ship your backend without the boilerplate!”</div>
                <div class="badge">4 Months</div>
                <p class="product-desc">Build applications faster with managed authentication, databases, storage and server-side functions in one platform.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Backend services for modern apps</li><li><span class="feat-icon">✓</span> Auth, data, storage and functions</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Appwrite%20Pro%20%E2%80%94%204%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff,#ececec)"><svg role="img" aria-label="Cal.com logo" viewBox="0 0 24 24" style="color:#111111;fill:currentColor"><path d="M2.408 14.488C1.035 14.488 0 13.4 0 12.058c0-1.346.982-2.443 2.408-2.443.758 0 1.282.233 1.691.765l-.66.55a1.343 1.343 0 0 0-1.03-.442c-.93 0-1.44.711-1.44 1.57 0 .86.559 1.557 1.44 1.557.413 0 .765-.147 1.043-.443l.651.573c-.391.51-.929.743-1.695.743zM6.948 10.913h.89v3.49h-.89v-.51c-.185.362-.493.604-1.083.604-.943 0-1.695-.82-1.695-1.826 0-1.007.752-1.825 1.695-1.825.585 0 .898.241 1.083.604zm.026 1.758c0-.546-.374-.998-.964-.998-.568 0-.938.457-.938.998 0 .528.37.998.938.998.586 0 .964-.456.964-.998zM8.467 9.503h.89v4.895h-.89zM9.752 13.937a.53.53 0 0 1 .542-.528c.313 0 .533.242.533.528a.527.527 0 0 1-.533.537.534.534 0 0 1-.542-.537zM14.23 13.839c-.33.403-.832.658-1.426.658a1.806 1.806 0 0 1-1.84-1.826c0-1.007.778-1.825 1.84-1.825.572 0 1.07.241 1.4.622l-.687.577c-.172-.215-.396-.376-.713-.376-.568 0-.938.456-.938.998 0 .541.37.997.938.997.343 0 .58-.179.757-.42zM14.305 12.671c0-1.007.78-1.825 1.84-1.825 1.061 0 1.84.818 1.84 1.825 0 1.007-.779 1.826-1.84 1.826-1.06-.005-1.84-.82-1.84-1.826zm2.778 0c0-.546-.37-.998-.938-.998-.568-.004-.937.452-.937.998 0 .542.37.998.937.998.568 0 .938-.456.938-.998zM24 12.269v2.13h-.89v-1.911c0-.604-.281-.864-.704-.864-.396 0-.678.197-.678.864v1.91h-.89v-1.91c0-.604-.285-.864-.704-.864-.396 0-.744.197-.744.864v1.91h-.89v-3.49h.89v.484c.185-.376.52-.564 1.035-.564.489 0 .898.241 1.123.649.224-.417.554-.65 1.153-.65.731.005 1.299.56 1.299 1.442z"/></svg></div>
                <h3 class="card-title">Cal.com Teams</h3>
                <div class="product-tagline">“Make every meeting easier to book!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Coordinate team availability, routing and scheduling workflows with a flexible calendar infrastructure platform.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Team scheduling and routing</li><li><span class="feat-icon">✓</span> Custom booking workflows</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Cal.com%20Teams%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff2f2,#fff)"><svg role="img" aria-label="Adobe logo" viewBox="0 0 256 227"><path fill="#fa0f00" d="m128.024 83.527l60.288 143.042h-39.513l-18.038-45.554H86.642zM256 0v226.54L161.353 0zM94.684 0L0 226.54V0z"/></svg></div>
                <h3 class="card-title">Adobe Creative Cloud</h3>
                <div class="product-tagline">“Bring every creative idea to life!”</div>
                <div class="badge">4 Months</div>
                <p class="product-desc">Create professional graphics, videos, layouts and digital experiences with Adobe’s industry-leading creative applications.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Photoshop, Illustrator, Premiere and more</li><li><span class="feat-icon">✓</span> Professional design and video workflows</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Adobe%20Creative%20Cloud%20%E2%80%94%204%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#334155,#64748b)"><span style="color:#fff">CIMANOTE</span></div>
                <h3 class="card-title">CimaNote Pro</h3>
                <div class="product-tagline">“Capture ideas before they disappear!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Keep notes, knowledge and important information organized in one focused space for faster recall and planning.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Organized note-taking workflow</li><li><span class="feat-icon">✓</span> Quick access to saved knowledge</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20CimaNote%20Pro%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#4f46e5,#ec4899)"><span style="color:#fff">SOFTR</span></div>
                <h3 class="card-title">Softr Pro</h3>
                <div class="product-tagline">“Launch a polished business app without code!”</div>
                <div class="badge">1 Month</div>
                <p class="product-desc">Turn business data into client portals, internal tools, directories and custom web apps with visual building blocks.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> No-code portals and internal apps</li><li><span class="feat-icon">✓</span> Connect data to responsive interfaces</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Softr%20Pro%20%E2%80%94%201%20Month" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#eff3ff,#fff)"><svg role="img" aria-label="Webflow logo" viewBox="0 0 24 24" style="color:#146EF5;fill:currentColor"><path d="m24 4.515-7.658 14.97H9.149l3.205-6.204h-.144C9.566 16.713 5.621 18.973 0 19.485v-6.118s3.596-.213 5.71-2.435H0V4.515h6.417v5.278l.144-.001 2.622-5.277h4.854v5.244h.144l2.72-5.244H24Z"/></svg></div>
                <h3 class="card-title">Webflow Premium</h3>
                <div class="product-tagline">“Design, build and publish without compromise!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Create responsive professional websites visually while retaining precise control over layout, CMS content and interactions.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Visual professional website builder</li><li><span class="feat-icon">✓</span> CMS, responsive design and interactions</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Webflow%20Premium%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#f7f0ff,#fff)"><svg role="img" aria-label="Sentry logo" viewBox="0 0 256 227"><path fill="#362d59" d="M148.368 12.403a23.935 23.935 0 0 0-41.003 0L73.64 70.165c52.426 26.174 87.05 78.177 90.975 136.642h-23.679c-3.918-50.113-34.061-94.41-79.238-116.448l-31.213 53.97a81.6 81.6 0 0 1 47.307 62.375h-54.38a3.895 3.895 0 0 1-3.178-5.69l15.069-25.626a55 55 0 0 0-17.221-9.738L3.167 191.277a23.27 23.27 0 0 0 8.662 31.982a23.9 23.9 0 0 0 11.583 3.075h74.471a99.43 99.43 0 0 0-41.003-88.72l11.84-20.5c35.679 24.504 55.754 66.038 52.79 109.22h63.094c2.99-65.43-29.047-127.512-84.107-162.986l23.935-41.002a3.947 3.947 0 0 1 5.382-1.384c2.716 1.486 103.993 178.208 105.89 180.258a3.895 3.895 0 0 1-3.486 5.792h-24.396q.46 9.789 0 19.528h24.499A23.53 23.53 0 0 0 256 202.91a23 23 0 0 0-3.178-11.685z"/></svg></div>
                <h3 class="card-title">Sentry</h3>
                <div class="product-tagline">“Find problems before your customers do!”</div>
                <div class="badge">Team / Business • 1 Year</div>
                <p class="product-desc">Monitor application errors and performance so development teams can diagnose issues quickly and ship with confidence.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Error and performance monitoring</li><li><span class="feat-icon">✓</span> Team and Business plans available</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Sentry%20%E2%80%94%20Team%20%2F%20Business%20%E2%80%A2%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#111827,#374151)"><span style="color:#fff">JOINSECRET</span></div>
                <h3 class="card-title">JoinSecret Premium</h3>
                <div class="product-tagline">“Unlock powerful software deals for your business!”</div>
                <div class="badge">6 or 12 Months</div>
                <p class="product-desc">Discover curated SaaS offers and startup-focused benefits that can reduce the cost of building and growing a company.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Premium SaaS deal discovery</li><li><span class="feat-icon">✓</span> Six and twelve-month options</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20JoinSecret%20Premium%20%E2%80%94%206%20or%2012%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#5b21b6,#a855f7)"><span style="color:#fff">FIREFLIES.AI</span></div>
                <h3 class="card-title">Fireflies AI Pro</h3>
                <div class="product-tagline">“Let every meeting become searchable knowledge!”</div>
                <div class="badge">4 Months</div>
                <p class="product-desc">Automatically capture meeting notes, transcripts and conversation insights so teams can focus on the discussion.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> AI meeting transcription and notes</li><li><span class="feat-icon">✓</span> Searchable conversation intelligence</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Fireflies%20AI%20Pro%20%E2%80%94%204%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff,#f4f4f4)"><svg role="img" aria-label="JetBrains logo" viewBox="0 0 256 256"><path d="M0 0h256v256H0z"/><path fill="#fff" d="M27.861 208h96v16h-96zm-4.01-141.995l7.125-6.741a8.02 8.02 0 0 0 6.272 3.712c2.73 0 4.523-1.92 4.523-5.632V32.085h11.008V57.43a14.68 14.68 0 0 1-3.926 11.222a15.02 15.02 0 0 1-10.025 4.266h-.94a16.38 16.38 0 0 1-13.45-6.132zm33.877-33.92h32.128v9.344H68.523v6.102H87.68v8.533H68.693v6.357h21.334v9.387H57.6zm47.787 9.686H93.568v-9.686h35.03v9.686h-11.99v30.25h-11.093zM28.288 87.808h18.859c3.954-.325 7.874.95 10.88 3.541a8.92 8.92 0 0 1 2.602 6.486a9.3 9.3 0 0 1-6.186 8.917a9.685 9.685 0 0 1 7.936 9.77c0 7.211-5.59 11.478-15.147 11.478H28.288zm21.333 12.33c0-2.218-1.792-3.413-5.034-3.413h-5.504v6.998h5.333c3.328 0 5.29-1.152 5.29-3.456zm-3.84 11.35h-6.698v7.381h6.912c3.413 0 5.29-1.322 5.29-3.669c-.08-2.11-1.497-3.515-4.704-3.693zM88.704 128l-8.064-12.117h-3.712V128H65.835l.085-40.192h17.707a17.66 17.66 0 0 1 13.013 4.267a12.46 12.46 0 0 1 3.552 8.439l-.01.862a12.8 12.8 0 0 1-8.235 12.33l7.795 11.661l15.842-37.858h10.667l17.066 40.278h-11.904l-2.858-7.211h-15.488L110.208 128zm32.128-27.35l-4.523 11.307h9.003zm-37.888-3.242h-5.93v9.685l5.973-.085c3.712 0 5.973-1.835 5.973-4.779c0-3.2-2.347-4.821-6.016-4.821m62.123-9.728h11.093v39.979h-11.093zm15.189 0h10.41l14.38 21.333V87.68h10.965v39.979h-9.686l-15.061-21.931v21.93h-11.008zm37.59 34.048l6.143-7.381a20.74 20.74 0 0 0 12.8 4.821c3.03 0 4.608-1.067 4.608-2.773c0-1.29-.695-2.092-3.262-2.937l-1.219-.366a42 42 0 0 0-.702-.188l-1.6-.392l-.876-.204l-1.704-.422l-1.632-.448c-6.379-1.86-10.85-4.612-10.85-11.427c0-7.424 5.888-12.8 15.488-12.8a25.1 25.1 0 0 1 16.427 5.333l-5.334 7.595a19.46 19.46 0 0 0-11.178-3.926c-2.688 0-4.011 1.067-4.011 2.56c0 1.352.741 2.148 3.368 2.968l1.244.355q.341.09.715.182l1.628.378c9.173 2.005 14.848 4.992 14.848 12.459c0 7.877-6.02 12.486-15.17 12.784l-.958.016a28 28 0 0 1-17.765-5.41z"/></svg></div>
                <h3 class="card-title">JetBrains All Products Pack</h3>
                <div class="product-tagline">“Code with the full power of a professional toolbox!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Access JetBrains IDEs for multiple languages and workflows, from IntelliJ IDEA and PyCharm to WebStorm and beyond.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Professional IDE suite</li><li><span class="feat-icon">✓</span> Tools for web, mobile and backend coding</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20JetBrains%20All%20Products%20Pack%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#0f172a,#475569)"><span style="color:#fff">ALIAS</span></div>
                <h3 class="card-title">AliasBrowser Pro</h3>
                <div class="product-tagline">“Keep multiple browser identities cleanly separated!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Manage distinct browser profiles and workflows for multi-account operations, testing and organized digital work.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Isolated browser identities</li><li><span class="feat-icon">✓</span> Cleaner multi-account workflows</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20AliasBrowser%20Pro%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff9e8,#fff)"><svg role="img" aria-label="Airtable logo" viewBox="0 0 256 215"><path fill="#ffbf00" d="M114.259 2.701L18.86 42.176c-5.305 2.195-5.25 9.73.089 11.847l95.797 37.989a35.54 35.54 0 0 0 26.208 0l95.799-37.99c5.337-2.115 5.393-9.65.086-11.846L141.442 2.7a35.55 35.55 0 0 0-27.183 0"/><path fill="#26b5f8" d="M136.35 112.757v94.902c0 4.514 4.55 7.605 8.746 5.942l106.748-41.435a6.39 6.39 0 0 0 4.035-5.941V71.322c0-4.514-4.551-7.604-8.747-5.941l-106.748 41.434a6.39 6.39 0 0 0-4.035 5.942"/><path fill="#ed3049" d="m111.423 117.654l-31.68 15.296l-3.217 1.555L9.65 166.548C5.411 168.593 0 165.504 0 160.795V71.72c0-1.704.874-3.175 2.046-4.283a7.3 7.3 0 0 1 1.618-1.213c1.598-.959 3.878-1.215 5.816-.448l101.41 40.18c5.155 2.045 5.56 9.268.533 11.697"/><path fill-opacity=".25" d="m111.423 117.654l-31.68 15.296L2.045 67.438a7.3 7.3 0 0 1 1.618-1.213c1.598-.959 3.878-1.215 5.816-.448l101.41 40.18c5.155 2.045 5.56 9.268.533 11.697"/></svg></div>
                <h3 class="card-title">Airtable Team</h3>
                <div class="product-tagline">“Turn scattered work into connected systems!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Combine flexible databases, collaborative views and automations to manage projects, content and business operations.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Flexible collaborative databases</li><li><span class="feat-icon">✓</span> Views, interfaces and automations</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Airtable%20Team%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#f97316,#fb7185)"><span style="color:#fff">CODERABBIT</span></div>
                <h3 class="card-title">CodeRabbit Pro+</h3>
                <div class="product-tagline">“Give every pull request an AI reviewer!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Accelerate code reviews with AI-generated feedback that helps teams spot issues and improve pull requests earlier.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> AI-assisted pull request reviews</li><li><span class="feat-icon">✓</span> Faster feedback for development teams</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20CodeRabbit%20Pro%2B%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff0f5,#fff)"><svg role="img" aria-label="Asana logo" viewBox="0 0 256 237"><path fill="#f06a6a" d="M200.325 125.27c-30.749 0-55.675 24.927-55.675 55.677s24.926 55.677 55.675 55.677S256 211.696 256 180.947c0-30.75-24.926-55.677-55.675-55.677m-144.65.005C24.927 125.275 0 150.197 0 180.947s24.927 55.677 55.675 55.677c30.75 0 55.678-24.928 55.678-55.677c0-30.75-24.928-55.672-55.678-55.672m128-69.6c0 30.75-24.927 55.68-55.674 55.68c-30.75 0-55.676-24.93-55.676-55.68C72.325 24.928 97.25 0 128 0c30.747 0 55.673 24.93 55.673 55.674"/></svg></div>
                <h3 class="card-title">Asana Advanced + AI</h3>
                <div class="product-tagline">“Move ambitious teamwork forward!”</div>
                <div class="badge">1 Year • 100 Seats</div>
                <p class="product-desc">Plan projects, coordinate dependencies and use AI-assisted workflows to keep large teams aligned on outcomes.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Advanced project and portfolio management</li><li><span class="feat-icon">✓</span> AI workflows for up to 100 seats</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Asana%20Advanced%20%2B%20AI%20%E2%80%94%201%20Year%20%E2%80%A2%20100%20Seats" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#111,#463d91)"><span style="color:#fff">SUPERHUMAN</span></div>
                <h3 class="card-title">Superhuman Business</h3>
                <div class="product-tagline">“Fly through your inbox and win back hours!”</div>
                <div class="badge">12 Months</div>
                <p class="product-desc">Use a speed-focused email experience with shortcuts, intelligent organization and collaboration features for busy teams.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Keyboard-first premium email</li><li><span class="feat-icon">✓</span> Faster triage and team productivity</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Superhuman%20Business%20%E2%80%94%2012%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff8bf,#fff)"><svg role="img" aria-label="Miro logo" viewBox="0 0 256 256"><path fill="#fd3" d="M0 64C0 28.654 28.654 0 64 0h128c35.346 0 64 28.654 64 64v128c0 35.346-28.654 64-64 64H64c-35.346 0-64-28.654-64-64z"/><path d="M170.195 48.8h-23.239l19.366 34.026L123.717 48.8h-23.239l21.303 41.588L77.239 48.8H54l23.239 52.937L54 207.6h23.239l44.542-113.426L100.478 207.6h23.239l42.605-120.988L146.956 207.6h23.239L212.8 75.263z"/></svg></div>
                <h3 class="card-title">Miro Starter</h3>
                <div class="product-tagline">“Turn team thinking into visible momentum!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Brainstorm, map processes, plan projects and collaborate visually on an expansive online workspace.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Collaborative whiteboards</li><li><span class="feat-icon">✓</span> Templates for planning and workshops</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Miro%20Starter%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#eff4ff,#fff)"><svg role="img" aria-label="Intercom logo" viewBox="0 0 256 263"><path d="M221.66 144.561c0 2.342-.897 4.588-2.493 6.244c-1.597 1.656-3.763 2.586-6.021 2.586s-4.424-.93-6.021-2.586s-2.494-3.902-2.494-6.244V65.677c0-2.342.897-4.588 2.494-6.243s3.763-2.587 6.02-2.587c2.259 0 4.425.93 6.022 2.587c1.596 1.655 2.493 3.901 2.493 6.243zm-2.955 54.657c-1.126 1.168-32.792 28.533-90.846 28.533s-89.508-27.22-90.845-28.387a8.6 8.6 0 0 1-2.043-2.654a9 9 0 0 1-.533-6.637a8.8 8.8 0 0 1 1.59-2.969c1.47-1.763 3.552-2.852 5.793-3.03a8.32 8.32 0 0 1 6.17 2.082c.493.365 28.78 24.154 79.798 24.154s79.516-23.935 79.798-24.154a8.45 8.45 0 0 1 6.202-2.059c2.247.177 4.339 1.256 5.83 3.007a8.9 8.9 0 0 1 1.995 6.274c-.158 2.282-1.178 4.407-2.839 5.913zM33.988 65.678c.127-2.35 1.146-4.551 2.834-6.124s3.907-2.388 6.173-2.269a8.38 8.38 0 0 1 5.564 2.6a9 9 0 0 1 2.458 5.792v78.738c0 2.342-.897 4.588-2.494 6.244c-1.596 1.656-3.762 2.586-6.02 2.586c-2.259 0-4.424-.93-6.021-2.586s-2.494-3.902-2.494-6.244zM76.7 48.163c.128-2.35 1.146-4.551 2.834-6.124s3.908-2.388 6.174-2.268a8.38 8.38 0 0 1 5.564 2.599a9 9 0 0 1 2.458 5.793V164.92c0 2.341-.898 4.587-2.494 6.243s-3.763 2.586-6.02 2.586c-2.26 0-4.425-.93-6.022-2.586s-2.494-3.902-2.494-6.243zm42.925-4.379c0-2.342.897-4.587 2.494-6.243s3.763-2.587 6.02-2.587c2.259 0 4.425.93 6.021 2.587c1.597 1.656 2.494 3.901 2.494 6.243v126.973c0 2.342-.897 4.588-2.494 6.244c-1.596 1.656-3.762 2.586-6.02 2.586s-4.424-.93-6.021-2.586s-2.494-3.902-2.494-6.244zm42.221 4.379c0-2.342.897-4.588 2.494-6.244s3.763-2.586 6.02-2.586c2.259 0 4.425.93 6.021 2.586s2.494 3.902 2.494 6.244V164.92c0 2.341-.897 4.587-2.494 6.243c-1.596 1.656-3.762 2.586-6.02 2.586s-4.424-.93-6.021-2.586s-2.494-3.902-2.494-6.243zM223.982 0H32.018a30.8 30.8 0 0 0-12.205 2.434A31.7 31.7 0 0 0 9.44 9.533A33.1 33.1 0 0 0 2.482 20.21A34 34 0 0 0 0 32.839v197.028a34 34 0 0 0 2.482 12.628a33.1 33.1 0 0 0 6.958 10.678a31.7 31.7 0 0 0 10.373 7.098a30.8 30.8 0 0 0 12.205 2.434h191.964a30.8 30.8 0 0 0 12.188-2.427a31.7 31.7 0 0 0 10.365-7.08a33.1 33.1 0 0 0 6.963-10.652A34 34 0 0 0 256 229.94V32.84a34 34 0 0 0-2.475-12.612a33.1 33.1 0 0 0-6.94-10.67a31.75 31.75 0 0 0-10.35-7.102A30.8 30.8 0 0 0 224.053.001"/></svg></div>
                <h3 class="card-title">Intercom Advanced</h3>
                <div class="product-tagline">“Create customer conversations that convert!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Support and engage customers through messaging, help-center experiences and intelligent service workflows.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Customer messaging and support</li><li><span class="feat-icon">✓</span> Help-center and automation workflows</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Intercom%20Advanced%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#6d28d9,#c026d3)"><span style="color:#fff">WHIMSICAL</span></div>
                <h3 class="card-title">Whimsical Pro</h3>
                <div class="product-tagline">“Make complex ideas instantly understandable!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Create flowcharts, wireframes, mind maps and collaborative documents in a fast, beautifully simple visual workspace.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Flowcharts, wireframes and mind maps</li><li><span class="feat-icon">✓</span> Fast visual team collaboration</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Whimsical%20Pro%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#fff2e9,#fff)"><svg role="img" aria-label="GitLab logo" viewBox="0 0 256 247"><path fill="#e24329" d="m251.845 97.642l-.328-.986l-34.85-90.903c-.657-1.808-1.972-3.287-3.616-4.274Q210.586 0 207.627 0c-1.973 0-3.78.822-5.26 1.973a8.73 8.73 0 0 0-3.124 4.767l-23.506 71.999H80.56l-23.506-72c-.493-1.808-1.644-3.451-3.123-4.766C52.45.822 50.643 0 48.67 0s-3.781.329-5.425 1.48c-1.644.986-2.96 2.465-3.617 4.273L4.781 96.656l-.33.986c-10.355 26.959-1.479 57.37 21.535 74.794h.328c0 .164 53.096 39.944 53.096 39.944l26.3 19.89l15.946 12c3.78 2.96 9.205 2.96 12.986 0l15.945-12l26.3-19.89l53.424-39.944c23.014-17.425 31.726-47.835 21.37-74.794z"/><path fill="#fc6d26" d="m251.845 97.642l-.328-.986c-17.26 3.616-33.205 10.85-46.849 21.04c-.164 0-41.424 31.398-76.602 57.863a18377 18377 0 0 0 48.657 36.821l53.424-39.944c23.013-17.425 31.726-47.835 21.37-74.794z"/><path fill="#fca326" d="m79.245 212.38l26.301 19.89l15.945 12c3.78 2.96 9.206 2.96 12.986 0l15.945-12l26.301-19.89s-22.684-17.095-48.657-36.82c-26.136 19.725-48.82 36.82-48.82 36.82"/><path fill="#fc6d26" d="M51.465 117.697c-13.644-10.192-29.589-17.589-46.849-21.04l-.329.985c-10.356 26.959-1.479 57.37 21.534 74.794h.33c0 .164 53.094 39.944 53.094 39.944s22.685-17.095 48.821-36.82c-35.013-26.466-76.272-57.699-76.601-57.863"/></svg></div>
                <h3 class="card-title">GitLab Ultimate</h3>
                <div class="product-tagline">“Take software from idea to production in one place!”</div>
                <div class="badge">12 Months</div>
                <p class="product-desc">Plan, build, secure and deploy software with an integrated DevSecOps platform for serious development teams.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Complete DevSecOps lifecycle</li><li><span class="feat-icon">✓</span> Advanced security and governance tools</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20GitLab%20Ultimate%20%E2%80%94%2012%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon" style="background:linear-gradient(145deg,#f4f1ff,#fff)"><svg role="img" aria-label="Framer logo" viewBox="0 0 256 384"><path d="M0 0h256v128H128zm0 128h128l128 128H128v128L0 256z"/></svg></div>
                <h3 class="card-title">Framer Pro</h3>
                <div class="product-tagline">“Publish world-class websites at design speed!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Design responsive websites visually with smooth interactions, CMS content and professional publishing tools.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Visual design and responsive layouts</li><li><span class="feat-icon">✓</span> CMS, effects and professional publishing</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Framer%20Pro%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#0f766e,#34d399)"><span style="color:#fff">TEXTSHIFT</span></div>
                <h3 class="card-title">TextShift Pro</h3>
                <div class="product-tagline">“Transform text-heavy work into rapid results!”</div>
                <div class="badge">1 Year</div>
                <p class="product-desc">Streamline content transformation and text-processing workflows for faster, more consistent everyday output.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Efficient text transformation</li><li><span class="feat-icon">✓</span> Consistent content-processing workflow</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20TextShift%20Pro%20%E2%80%94%201%20Year" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#111827,#6d28d9)"><span style="color:#fff">ANAM.AI</span></div>
                <h3 class="card-title">Anam AI Video</h3>
                <div class="product-tagline">“Bring lifelike AI characters into real-time conversations!”</div>
                <div class="badge">6 Months</div>
                <p class="product-desc">Create interactive AI personas for video experiences, customer engagement and natural face-to-face digital conversations.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Interactive AI video personas</li><li><span class="feat-icon">✓</span> Real-time conversational experiences</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Anam%20AI%20Video%20%E2%80%94%206%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#047857,#34d399)"><span style="color:#fff">SCALINGO</span></div>
                <h3 class="card-title">Scalingo Cloud Credits</h3>
                <div class="product-tagline">“Deploy your application and keep building!”</div>
                <div class="badge">6 or 12 Months</div>
                <p class="product-desc">Run web applications, workers and managed data services on a developer-friendly cloud platform.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Cloud credits for app deployment</li><li><span class="feat-icon">✓</span> Six and twelve-month options</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Scalingo%20Cloud%20Credits%20%E2%80%94%206%20or%2012%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>

              <div class="product-card animate-scroll">
                <div class="brand-icon wordmark" style="background:linear-gradient(145deg,#9d174d,#f472b6)"><span style="color:#fff">SENTAIMENT</span></div>
                <h3 class="card-title">Sentaiment Starter</h3>
                <div class="product-tagline">“Turn customer feelings into decisions!”</div>
                <div class="badge">12 Months</div>
                <p class="product-desc">Track and interpret audience sentiment to reveal useful patterns across feedback, conversations and customer signals.</p>
                <ul class="features"><li><span class="feat-icon">✓</span> Sentiment and feedback analysis</li><li><span class="feat-icon">✓</span> Actionable customer insight discovery</li></ul>
                <a href="https://wa.me/919071145694?text=Hi%2C%20I%20want%20to%20know%20the%20price%20for%20Sentaiment%20Starter%20%E2%80%94%2012%20Months" target="_blank" rel="noopener" class="dm-btn">Get best price <span aria-hidden="true">→</span></a>
              </div>
            </div>

          ]]></b:widget-setting>
        </b:widget-settings>
        <b:includable id='main'>
          <data:content/>
        </b:includable>
      </b:widget>
    </b:section>
  </div>

  <b:else/>

  <!-- ============ POST / PAGE / LABEL VIEW ============ -->
  <header class='page-head'>
    <div class='wrap'>
      <div class='eyebrow'>AISMARTSTOR.IN</div>
      <h1><data:view.title/></h1>
    </div>
  </header>

  <div class='container wrap blog-section'>
    <b:section id='blog-main' maxwidgets='1' showaddelement='no'>
      <b:widget id='Blog1' locked='true' title='Blog Posts' type='Blog' version='2' visible='true'>
        <b:includable id='main'>
          <div class='post-stream'>
            <b:loop values='data:posts' var='post'>
              <article class='post-entry'>
                <b:if cond='data:view.isSingleItem'>
                  <h1 class='post-title'><data:post.title/></h1>
                <b:else/>
                  <h2 class='post-title'><a expr:href='data:post.url'><data:post.title/></a></h2>
                </b:if>
                <div class='post-meta'><data:post.date/></div>
                <div class='post-body'><data:post.body/></div>
                <b:if cond='data:view.isSingleItem'>
                  <b:include data='post' name='comments'/>
                <b:else/>
                  <a class='dm-btn post-more' expr:href='data:post.url'>Read the full post</a>
                </b:if>
              </article>
            </b:loop>
          </div>
          <div class='blog-pager'>
            <b:if cond='data:newerPageUrl'>
              <a class='pager-btn' expr:href='data:newerPageUrl'>&#8592; Newer posts</a>
            </b:if>
            <b:if cond='data:olderPageUrl'>
              <a class='pager-btn' expr:href='data:olderPageUrl'>Older posts &#8594;</a>
            </b:if>
          </div>
        </b:includable>
      </b:widget>
    </b:section>
  </div>

  </b:if>

  <!-- ============ SERVICE STRIP ============ -->
  <div class='service-band wrap'>
    <div class='service-strip animate-scroll'>
      <div class='service-item'><strong>Fast activation</strong><span>Quick, guided setup after confirmation</span></div>
      <div class='service-item'><strong>Human assistance</strong><span>Real support before and after your order</span></div>
      <div class='service-item'><strong>Curated plans</strong><span>Only useful tools for work, learning and play</span></div>
    </div>
  </div>

  <!-- ============ FOOTER ============ -->
  <footer class='premium-footer'>
    <div class='footer-cta wrap'>
      <div>
        <small>Need help choosing?</small>
        <h2>Let&#8217;s find the right premium plan for your goals.</h2>
      </div>
      <a href='https://wa.me/919071145694?text=Hi,%20please%20help%20me%20choose%20the%20right%20premium%20tool' rel='noopener' target='_blank'>Start a conversation <span aria-hidden='true'>&#8594;</span></a>
    </div>

    <div class='footer-grid wrap'>
      <div class='footer-brand'>
        <a class='brand-lockup' expr:href='data:blog.homepageUrl'>
          <span class='brand-seal'>AI</span>
          <span><span class='brand-name'>AISMARTSTOR.IN</span><span class='brand-note'>Premium digital membership store</span></span>
        </a>
        <p>Curated digital tools for people who want to create faster, work smarter and enjoy more&#8212;supported by a real person when guidance matters.</p>
        <div class='payment-pills'><span>UPI</span><span>Binance</span><span>Guided activation</span></div>
      </div>
      <div>
        <div class='footer-heading'>Collection</div>
        <ul class='footer-links'>
          <li><a expr:href='data:blog.homepageUrl + &quot;#grid-ai&quot;'>AI tools</a></li>
          <li><a expr:href='data:blog.homepageUrl + &quot;#grid-prod&quot;'>Productivity</a></li>
          <li><a expr:href='data:blog.homepageUrl + &quot;#grid-biz&quot;'>Business</a></li>
          <li><a expr:href='data:blog.homepageUrl + &quot;#grid-ent&quot;'>Entertainment</a></li>
          <li><a expr:href='data:blog.homepageUrl + &quot;#grid-new&quot;'>New arrivals</a></li>
        </ul>
      </div>
      <div>
        <div class='footer-heading'>Our standard</div>
        <ul class='footer-links'>
          <li><span>Clear plan information</span></li>
          <li><span>Responsive assistance</span></li>
          <li><span>Fast activation guidance</span></li>
          <li><span>Curated useful products</span></li>
        </ul>
      </div>
      <div>
        <div class='footer-heading'>Contact</div>
        <ul class='footer-links'>
          <li class='contact-row'><svg viewBox='0 0 24 24'><path d='M3 5h18v14H3z'/><path d='m3 6 9 7 9-7'/></svg><a href='mailto:aismartstore.in@gmail.com'>aismartstore.in@gmail.com</a></li>
          <li class='contact-row'><svg viewBox='0 0 24 24'><path d='M20 11.5a8.5 8.5 0 0 1-12.6 7.4L3 20l1.1-4.3A8.5 8.5 0 1 1 20 11.5z'/></svg><a href='https://wa.me/919071145694' rel='noopener' target='_blank'>Chat on WhatsApp</a></li>
        </ul>
      </div>
    </div>

    <div class='footer-bottom'>
      <div class='footer-bottom-inner wrap'>
        <span>&#169; <data:blog.title/>. All rights reserved.</span>
        <span class='footer-status'>Support available</span>
      </div>
    </div>
  </footer>

  <!-- ============ FLOATING WHATSAPP ============ -->
  <a class='floating-wa' href='https://wa.me/919071145694?text=Hi,%20I%20need%20help%20with%20AISMARTSTOR.IN' rel='noopener' target='_blank'>
    <svg aria-label='WhatsApp' role='img' viewBox='0 0 32 32'><path d='M19.11 17.21c-.28-.14-1.65-.81-1.9-.91-.26-.09-.44-.14-.63.14-.19.28-.72.91-.88 1.09-.16.19-.33.21-.6.07-.28-.14-1.17-.43-2.23-1.38-.83-.74-1.38-1.65-1.55-1.93-.16-.28-.02-.43.12-.57.13-.12.28-.33.42-.49.14-.16.19-.28.28-.46.09-.19.05-.35-.02-.49-.07-.14-.63-1.51-.86-2.07-.23-.55-.46-.48-.63-.49h-.53c-.19 0-.49.07-.74.35-.26.28-.98.95-.98 2.32s1 2.69 1.14 2.88c.14.19 1.96 2.99 4.75 4.2.66.29 1.18.47 1.59.6.67.21 1.27.18 1.75.11.53-.08 1.65-.67 1.88-1.32.23-.65.23-1.21.16-1.32-.07-.12-.25-.19-.53-.33zM16.05 4.8a11 11 0 0 0-9.44 16.66L5.05 27.2l5.87-1.54A11 11 0 1 0 16.05 4.8zm0 19.98c-1.81 0-3.58-.49-5.12-1.42l-.37-.22-3.48.91.93-3.4-.24-.38a8.96 8.96 0 1 1 8.28 4.51z'/></svg>
  </a>

  <!-- ============ SCRIPTS ============ -->
  <script type='text/javascript'>
  //<![CDATA[
  (function () {
    'use strict';

    function normalizeSearch(value) {
      return String(value || '')
        .normalize('NFKD')
        .replace(/[\u0300-\u036f]/g, '')
        .toLowerCase()
        .replace(/[^a-z0-9]+/g, ' ')
        .trim();
    }

    function ready(fn) {
      if (document.readyState === 'loading') {
        document.addEventListener('DOMContentLoaded', fn);
      } else {
        fn();
      }
    }

    ready(function () {
      var searchInput = document.getElementById('searchInput');
      var status = document.getElementById('searchStatus');
      var cards = Array.prototype.slice.call(document.querySelectorAll('.product-card'));
      var grids = Array.prototype.slice.call(document.querySelectorAll('.product-grid'));

      /* ---------- card prep: search index, stagger, cursor glow ---------- */
      cards.forEach(function (card, index) {
        card.dataset.search = normalizeSearch(card.textContent);
        card.style.setProperty('--delay', ((index % 12) * 45) + 'ms');

        card.addEventListener('pointermove', function (event) {
          var bounds = card.getBoundingClientRect();
          card.style.setProperty('--mx', (((event.clientX - bounds.left) / bounds.width) * 100) + '%');
          card.style.setProperty('--my', (((event.clientY - bounds.top) / bounds.height) * 100) + '%');
        });
        card.addEventListener('pointerleave', function () {
          card.style.setProperty('--mx', '50%');
          card.style.setProperty('--my', '0%');
        });
      });

      /* ---------- live filter ---------- */
      function filterProducts() {
        var query = normalizeSearch(searchInput.value);
        var resultCount = 0;

        cards.forEach(function (card) {
          var matches = !query || (card.dataset.search || '').indexOf(query) !== -1;
          card.hidden = !matches;
          card.style.display = matches ? '' : 'none';
          if (matches) {
            resultCount += 1;
            if (query) { card.classList.add('visible'); }
          }
        });

        grids.forEach(function (grid) {
          var hasResult = Array.prototype.slice.call(grid.querySelectorAll('.product-card')).some(function (card) {
            return !card.hidden;
          });
          var banner = grid.previousElementSibling && grid.previousElementSibling.classList.contains('launch-banner')
            ? grid.previousElementSibling
            : null;
          var heading = banner ? banner.previousElementSibling : grid.previousElementSibling;
          var show = !query || hasResult;

          grid.style.display = show ? '' : 'none';
          if (banner) { banner.style.display = show ? '' : 'none'; }
          if (heading && heading.classList.contains('category-title')) {
            heading.style.display = show ? '' : 'none';
          }
        });

        if (!status) { return; }
        if (!query) {
          status.classList.remove('active');
          status.textContent = '';
        } else {
          status.textContent = resultCount
            ? resultCount + (resultCount === 1 ? ' result' : ' results') + ' for "' + searchInput.value.trim() + '"'
            : 'No tools found for "' + searchInput.value.trim() + '"';
          status.classList.add('active');
        }
      }

      if (searchInput) {
        if (cards.length) {
          ['input', 'search', 'change'].forEach(function (name) {
            searchInput.addEventListener(name, filterProducts);
          });
        } else {
          /* Off the homepage there are no cards, so send the query to Blogger search */
          searchInput.addEventListener('keydown', function (event) {
            if (event.key === 'Enter') {
              var q = searchInput.value.trim();
              if (q) { window.location.href = '/search?q=' + encodeURIComponent(q); }
            }
          });
        }
      }

      /* ---------- reveal on scroll ---------- */
      var animated = Array.prototype.slice.call(document.querySelectorAll('.animate-scroll'));
      if (!('IntersectionObserver' in window)) {
        animated.forEach(function (el) { el.classList.add('visible'); });
        return;
      }
      var observer = new IntersectionObserver(function (entries, obs) {
        entries.forEach(function (entry) {
          if (entry.isIntersecting) {
            entry.target.classList.add('visible');
            obs.unobserve(entry.target);
          }
        });
      }, { root: null, rootMargin: '0px 0px -8% 0px', threshold: 0.12 });
      animated.forEach(function (el) { observer.observe(el); });
    });
  })();
  //]]>
  </script>

</body>
</html>
