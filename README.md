<!DOCTYPE html>

<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>🦁 のんほいパークしおり 4/29</title>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Zen+Maru+Gothic:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root {
    --sky: #5BC8F5;
    --sun: #FFD43B;
    --leaf: #5EC97A;
    --coral: #FF7F6B;
    --purple: #C47EE0;
    --sand: #FFB84C;
    --dark: #2D2A26;
    --card-bg: #FFFFFF;
    --shadow: 0 4px 20px rgba(0,0,0,0.08);
    --radius: 20px;
  }

- { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }

body {
font-family: ‘Zen Maru Gothic’, sans-serif;
background: #E8F8FF;
color: var(–dark);
min-height: 100vh;
padding-bottom: 80px;
overflow-x: hidden;
}

/* ===== STICKY NAV ===== */
.sticky-nav {
position: sticky;
top: 0;
z-index: 100;
background: rgba(255,255,255,0.92);
backdrop-filter: blur(12px);
border-bottom: 1px solid rgba(0,0,0,0.06);
padding: 8px 10px;
display: flex;
gap: 6px;
overflow-x: auto;
scrollbar-width: none;
}
.sticky-nav::-webkit-scrollbar { display: none; }
.nav-btn {
flex-shrink: 0;
background: none;
border: 1.5px solid #DDD;
border-radius: 50px;
padding: 5px 11px;
font-size: 0.72rem;
font-weight: 700;
color: #666;
cursor: pointer;
transition: all 0.15s;
font-family: ‘Zen Maru Gothic’, sans-serif;
white-space: nowrap;
}
.nav-btn:hover, .nav-btn.active {
background: var(–sky);
border-color: var(–sky);
color: #fff;
}

/* ===== COVER ===== */
.cover {
background: linear-gradient(160deg, #5BC8F5 0%, #74E0A0 50%, #FFD43B 100%);
padding: 48px 20px 64px;
text-align: center;
position: relative;
overflow: hidden;
}
.cover::after {
content: ‘’;
position: absolute;
bottom: -1px; left: 0; right: 0;
height: 44px;
background: #E8F8FF;
clip-path: ellipse(55% 100% at 50% 100%);
}
.cover-emoji-row {
font-size: 2.4rem;
letter-spacing: 8px;
margin-bottom: 14px;
animation: bounce 2s ease-in-out infinite;
}
@keyframes bounce {
0%,100% { transform: translateY(0); }
50% { transform: translateY(-7px); }
}
.cover-date {
display: inline-block;
background: rgba(255,255,255,0.55);
backdrop-filter: blur(8px);
border-radius: 50px;
padding: 6px 20px;
font-size: 0.85rem;
font-weight: 700;
color: #1a6a8a;
letter-spacing: 1px;
margin-bottom: 14px;
}
.cover-title {
font-family: ‘Nunito’, sans-serif;
font-size: 1.85rem;
font-weight: 900;
color: #fff;
text-shadow: 0 2px 14px rgba(0,0,0,0.15);
line-height: 1.3;
margin-bottom: 8px;
}
.cover-subtitle {
font-size: 0.88rem;
color: rgba(255,255,255,0.92);
font-weight: 600;
margin-bottom: 20px;
}
.cover-badge-row {
display: flex;
justify-content: center;
gap: 8px;
flex-wrap: wrap;
}
.badge {
background: rgba(255,255,255,0.85);
border-radius: 50px;
padding: 6px 14px;
font-size: 0.78rem;
font-weight: 700;
color: #2D5F7A;
}

/* ===== SECTIONS ===== */
.sections {
padding: 20px 14px 0;
display: flex;
flex-direction: column;
gap: 16px;
}
.section-card {
background: var(–card-bg);
border-radius: var(–radius);
box-shadow: var(–shadow);
overflow: hidden;
}
.section-header {
padding: 14px 18px 10px;
display: flex;
align-items: center;
gap: 10px;
border-bottom: 2px dashed rgba(0,0,0,0.06);
}
.section-icon {
width: 42px; height: 42px;
border-radius: 12px;
display: flex; align-items: center; justify-content: center;
font-size: 1.3rem;
flex-shrink: 0;
}
.section-title {
font-family: ‘Nunito’, sans-serif;
font-size: 1.05rem;
font-weight: 800;
}
.section-body { padding: 14px 18px; }

.theme-sky .section-icon { background: #E3F6FD; }
.theme-leaf .section-icon { background: #E3F9EC; }
.theme-coral .section-icon { background: #FFE8E5; }
.theme-sun .section-icon { background: #FFF5D6; }
.theme-purple .section-icon { background: #F3E5FF; }
.theme-sand .section-icon { background: #FFF0D6; }
.theme-sky .section-title { color: #2A8BB5; }
.theme-leaf .section-title { color: #237A42; }
.theme-coral .section-title { color: #C94F3B; }
.theme-sun .section-title { color: #9B7A00; }
.theme-purple .section-title { color: #7B3FA8; }
.theme-sand .section-title { color: #9B6200; }

/* ===== TIMELINE ===== */
.timeline { position: relative; padding-left: 16px; }
.timeline::before {
content: ‘’;
position: absolute;
left: 20px; top: 6px; bottom: 6px;
width: 3px;
background: repeating-linear-gradient(180deg,
var(–sky) 0, var(–sky) 6px,
transparent 6px, transparent 12px);
border-radius: 10px;
}
.tl-item { display: flex; gap: 14px; margin-bottom: 18px; position: relative; }
.tl-item:last-child { margin-bottom: 0; }
.tl-dot {
width: 10px; height: 10px;
border-radius: 50%;
background: var(–sky);
border: 2.5px solid #fff;
box-shadow: 0 0 0 2px var(–sky);
flex-shrink: 0;
margin-top: 5px;
z-index: 1;
}
.tl-time {
font-family: ‘Nunito’, sans-serif;
font-size: 0.88rem;
font-weight: 800;
color: #2A8BB5;
white-space: nowrap;
min-width: 58px;
padding-top: 2px;
}
.tl-label { font-size: 0.95rem; font-weight: 700; color: var(–dark); line-height: 1.4; }
.tl-note { font-size: 0.8rem; color: #888; margin-top: 2px; line-height: 1.5; }

/* ===== COURSE BLOCKS ===== */
.course-block {
border-radius: 14px;
padding: 12px 14px;
margin-bottom: 10px;
display: flex;
gap: 12px;
align-items: flex-start;
}
.course-block:last-child { margin-bottom: 0; }
.cb-sky    { background: #EAF7FD; border-left: 4px solid var(–sky); }
.cb-sun    { background: #FFF8E0; border-left: 4px solid var(–sun); }
.cb-purple { background: #F5EEFF; border-left: 4px solid var(–purple); }
.cb-coral  { background: #FFF0ED; border-left: 4px solid var(–coral); }
.cb-sand   { background: #FFF5E0; border-left: 4px solid var(–sand); }
.cb-icon { font-size: 1.5rem; line-height: 1; flex-shrink: 0; margin-top: 1px; }
.cb-time { font-family: ‘Nunito’, sans-serif; font-size: 0.78rem; font-weight: 800; color: #666; margin-bottom: 2px; }
.cb-title { font-size: 0.95rem; font-weight: 700; color: var(–dark); }
.cb-desc { font-size: 0.8rem; color: #777; margin-top: 3px; line-height: 1.6; }

/* ===== ROUTE ===== */
.route-list { display: flex; flex-direction: column; }
.route-item { display: flex; align-items: center; gap: 10px; }
.route-node { display: flex; flex-direction: column; align-items: center; flex-shrink: 0; }
.rn-dot {
width: 12px; height: 12px;
border-radius: 50%;
background: var(–sky);
border: 2px solid #fff;
box-shadow: 0 0 0 2px var(–sky);
}
.rn-dot.green { background: var(–leaf); box-shadow: 0 0 0 2px var(–leaf); }
.rn-line {
width: 2px; height: 22px;
background: repeating-linear-gradient(180deg,
#ccc 0, #ccc 4px, transparent 4px, transparent 8px);
margin: 2px 0;
}
.route-label { font-size: 0.88rem; font-weight: 600; padding: 4px 0; color: var(–dark); }
.route-dest {
background: var(–leaf);
color: #fff;
border-radius: 50px;
padding: 6px 16px;
font-size: 0.9rem;
font-weight: 700;
display: inline-block;
margin-top: 4px;
}
.route-info-row { display: flex; gap: 8px; margin-top: 12px; flex-wrap: wrap; }
.route-chip {
background: #F0F9FF;
border: 1.5px solid #BDE9FF;
border-radius: 50px;
padding: 5px 12px;
font-size: 0.78rem;
font-weight: 700;
color: #2A8BB5;
}

/* ===== COST TABLE ===== */
.cost-table { width: 100%; border-collapse: collapse; }
.cost-table tr:not(:last-child) td { border-bottom: 1px dashed #EEE; }
.cost-table td { padding: 10px 4px; font-size: 0.88rem; }
.cost-table td:last-child { text-align: right; font-family: ‘Nunito’, sans-serif; font-weight: 800; color: var(–coral); }
.cost-label { color: #555; }
.cost-sub { font-size: 0.75rem; color: #999; margin-top: 1px; }
.cost-total-row td { background: #FFF5E5; border-radius: 10px; padding: 12px 10px !important; font-weight: 700; }
.cost-total-row td:first-child { color: var(–dark); font-size: 0.95rem; }
.cost-total-row td:last-child { color: var(–coral); font-size: 1.15rem; }

/* ===== CHECKLIST ===== */
.checklist { display: flex; flex-direction: column; }
.check-item {
display: flex;
align-items: center;
gap: 12px;
padding: 13px 0;
border-bottom: 1px dashed #EEE;
cursor: pointer;
user-select: none;
-webkit-tap-highlight-color: transparent;
}
.check-item:last-child { border-bottom: none; }
.check-box {
width: 32px; height: 32px;
border-radius: 10px;
border: 2.5px solid #D0D0D0;
display: flex; align-items: center; justify-content: center;
font-size: 1.1rem;
transition: all 0.2s;
flex-shrink: 0;
background: #fff;
}
.check-item.checked .check-box { background: var(–leaf); border-color: var(–leaf); color: #fff; }
.check-item.checked .check-text { text-decoration: line-through; color: #bbb; }
.check-text { font-size: 1rem; font-weight: 700; transition: color 0.2s; flex: 1; line-height: 1.4; }
.check-note { font-size: 0.8rem; color: #aaa; display: block; margin-top: 2px; font-weight: 500; }
.check-emoji { font-size: 1.3rem; }
.check-progress {
background: #F0F0F0;
border-radius: 50px;
height: 10px;
margin-bottom: 14px;
overflow: hidden;
}
.check-progress-bar {
height: 100%;
background: linear-gradient(90deg, var(–leaf), #4ABF68);
border-radius: 50px;
transition: width 0.4s ease;
width: 0%;
}
.check-count { font-size: 0.82rem; color: #888; font-weight: 700; margin-bottom: 8px; }

/* ===== PARKING ===== */
.parking-card {
background: linear-gradient(135deg, #EAF9F0, #D4F5E2);
border-radius: 14px;
padding: 14px 16px;
border: 1.5px solid #9EE5B5;
}
.parking-name { font-size: 1rem; font-weight: 700; color: #1C6E39; margin-bottom: 6px; }
.parking-note { font-size: 0.85rem; color: #3A8A5A; line-height: 1.8; }

.open-info { display: flex; gap: 10px; margin-top: 10px; }
.open-chip { flex: 1; border-radius: 12px; padding: 12px 10px; text-align: center; }
.open-chip.green { background: #EAF9F0; border: 1.5px solid #9EE5B5; }
.open-chip.coral { background: #FFE8E5; border: 1.5px solid #FFBBB3; }
.oc-label { font-size: 0.72rem; font-weight: 700; color: #888; margin-bottom: 4px; }
.oc-value { font-family: ‘Nunito’, sans-serif; font-size: 1.2rem; font-weight: 900; color: var(–dark); }

/* ===== WARNINGS ===== */
.warn-list { display: flex; flex-direction: column; gap: 10px; }
.warn-item {
display: flex;
gap: 10px;
align-items: flex-start;
background: #FFF8E0;
border-radius: 12px;
padding: 10px 12px;
border-left: 4px solid var(–sun);
}
.warn-icon { font-size: 1.1rem; flex-shrink: 0; margin-top: 1px; }
.warn-text { font-size: 0.88rem; font-weight: 600; color: #5A4A00; line-height: 1.6; }

.map-btn {
display: flex;
align-items: center;
justify-content: center;
gap: 8px;
background: linear-gradient(135deg, #4CAF8A, #2E9E70);
color: #fff;
border-radius: 14px;
padding: 14px;
text-decoration: none;
font-size: 0.95rem;
font-weight: 700;
margin-top: 12px;
box-shadow: 0 4px 16px rgba(46,158,112,0.3);
}

.footer {
text-align: center;
padding: 32px 20px 10px;
font-size: 0.8rem;
color: #aaa;
font-weight: 600;
}
.footer-emoji { font-size: 1.5rem; display: block; margin-bottom: 6px; }
</style>

</head>
<body>

<nav class="sticky-nav">
  <button class="nav-btn active"  onclick="goTo('cover')">🦁 ひょうし</button>
  <button class="nav-btn" onclick="goTo('schedule')">🗓 よてい</button>
  <button class="nav-btn" onclick="goTo('route')">🗺 いきかた</button>
  <button class="nav-btn" onclick="goTo('course')">🎡 こうえん</button>
  <button class="nav-btn" onclick="goTo('cost')">💰 おかね</button>
  <button class="nav-btn" onclick="goTo('checklist')">✅ もちもの</button>
  <button class="nav-btn" onclick="goTo('parking')">🅿 ちゅうしゃ</button>
  <button class="nav-btn" onclick="goTo('notes')">⚠ ちゅうい</button>
</nav>

<!-- ① ひょうし -->

<div class="cover" id="cover">
  <div class="cover-emoji-row">🦁🐘🦒🎠🦋</div>
  <div class="cover-date">4がつ29にち（かようび・おやすみ）</div>
  <div class="cover-title">のんほいパーク<br>みゆゆらのしおり🗒️</div>
  <div class="cover-subtitle">おとな2にん＋しょうがくせい2にん ｜ たかおかからしゅっぱつ</div>
  <div class="cover-badge-row">
    <span class="badge">🐾 どうぶつえん</span>
    <span class="badge">🦕 はくぶつかん</span>
    <span class="badge">🎠 ゆうえんち</span>
    <span class="badge">💰 1,600えん</span>
  </div>
</div>

<div class="sections">

  <!-- ② よてい -->

  <div class="section-card theme-sky" id="schedule">
    <div class="section-header">
      <div class="section-icon">🗓️</div>
      <div class="section-title">② とうじつのよてい</div>
    </div>
    <div class="section-body">
      <div class="timeline">
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-time">8:30</div>
          <div class="tl-content">
            <div class="tl-label">🏠 たかおかにあつまる</div>
            <div class="tl-note">もちものをかくにんしてね！</div>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-time">8:40</div>
          <div class="tl-content">
            <div class="tl-label">🚗 しゅっぱつ！</div>
            <div class="tl-note">くるまでしゅっぱつ。たのしみだね！</div>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-time">10:00ごろ</div>
          <div class="tl-content">
            <div class="tl-label">🦁 のんほいパークにとうちゃく</div>
            <div class="tl-note">ひがしもんのちゅうしゃじょうにとめるよ</div>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-time">10:00〜</div>
          <div class="tl-content">
            <div class="tl-label">🐘 どうぶつえんをたんけん！</div>
            <div class="tl-note">ごぜんちゅうにメインのどうぶつをみよう</div>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-time">11:30</div>
          <div class="tl-content">
            <div class="tl-label">🍱 はやめのおひるごはん</div>
            <div class="tl-note">こんでいるまえにたべちゃおう！</div>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-time">12:15</div>
          <div class="tl-content">
            <div class="tl-label">🦕 しぜんしはくぶつかん（おくない）</div>
            <div class="tl-note">すずしいなかでゆっくりみられるよ◎</div>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-time">13:15</div>
          <div class="tl-content">
            <div class="tl-label">🎠 ゆうえんちエリア</div>
            <div class="tl-note">みゆちゃん・ゆらちゃんのおたのしみ！</div>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-time">14:30</div>
          <div class="tl-content">
            <div class="tl-label">🍦 おやつ・おみやげ・くるまへ</div>
            <div class="tl-note">トイレもすませてね</div>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot" style="background:var(--coral);box-shadow:0 0 0 2px var(--coral)"></div>
          <div class="tl-time" style="color:var(--coral)">15:30</div>
          <div class="tl-content">
            <div class="tl-label">🚗 かえりのしゅっぱつ</div>
            <div class="tl-note">たかおかまでやく1じかん30ぷん〜2じかん</div>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot" style="background:var(--leaf);box-shadow:0 0 0 2px var(--leaf)"></div>
          <div class="tl-time" style="color:var(--leaf)">17〜18じ</div>
          <div class="tl-content">
            <div class="tl-label">🏠 たかおかにかえるよ</div>
            <div class="tl-note">こんでも19じまでにはかえれるよ👌</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ③ いきかた -->

  <div class="section-card theme-leaf" id="route">
    <div class="section-header">
      <div class="section-icon">🗺️</div>
      <div class="section-title">③ くるまでのいきかた</div>
    </div>
    <div class="section-body">
      <div class="route-list">
        <div class="route-item">
          <div class="route-node"><div class="rn-dot"></div><div class="rn-line"></div></div>
          <div class="route-label">🏠 たかおかをしゅっぱつ（8:40）</div>
        </div>
        <div class="route-item">
          <div class="route-node"><div class="rn-dot"></div><div class="rn-line"></div></div>
          <div class="route-label">こくどう1ごう（はまなバイパス）</div>
        </div>
        <div class="route-item">
          <div class="route-node"><div class="rn-dot"></div><div class="rn-line"></div></div>
          <div class="route-label">こくどう23ごう（とよはしひがしバイパス）</div>
        </div>
        <div class="route-item">
          <div class="route-node"><div class="rn-dot"></div><div class="rn-line"></div></div>
          <div class="route-label">こまつばらインター</div>
        </div>
        <div class="route-item">
          <div class="route-node"><div class="rn-dot green"></div></div>
          <div><div class="route-dest">🦁 のんほいパーク とうちゃく（10:00ごろ）</div></div>
        </div>
      </div>
      <div class="route-info-row">
        <div class="route-chip">🕐 やく1じかん20ぷん</div>
        <div class="route-chip">📍 ひがしもんちゅうしゃじょうへ</div>
      </div>
    </div>
  </div>

  <!-- ④ こうえんのまわりかた -->

  <div class="section-card theme-coral" id="course">
    <div class="section-header">
      <div class="section-icon">🎡</div>
      <div class="section-title">④ こうえんのまわりかた</div>
    </div>
    <div class="section-body">
      <div class="course-block cb-sky">
        <div class="cb-icon">🐘</div>
        <div>
          <div class="cb-time">10:00 〜 11:30</div>
          <div class="cb-title">どうぶつえんエリア</div>
          <div class="cb-desc">ライオン・ゾウ・キリンがいるよ！<br>ごぜんちゅうのすずしいうちにまわろう🌿</div>
        </div>
      </div>
      <div class="course-block cb-sun">
        <div class="cb-icon">🍱</div>
        <div>
          <div class="cb-time">11:30 〜 12:15</div>
          <div class="cb-title">おひるごはん（はやめ）</div>
          <div class="cb-desc">GWはこむから11:30にさきにたべちゃおう🍜</div>
        </div>
      </div>
      <div class="course-block cb-purple">
        <div class="cb-icon">🦕</div>
        <div>
          <div class="cb-time">12:15 〜 13:15</div>
          <div class="cb-title">しぜんしはくぶつかん</div>
          <div class="cb-desc">きょうりゅうのほねやひょうほんがみられるよ！<br>おくないですずしくてきもちいい♪</div>
        </div>
      </div>
      <div class="course-block cb-coral">
        <div class="cb-icon">🎠</div>
        <div>
          <div class="cb-time">13:15 〜 14:30</div>
          <div class="cb-title">ゆうえんちエリア</div>
          <div class="cb-desc">みゆちゃん・ゆらちゃんがたのしみにしてたとこ！<br>のりものいっぱいのろうね🎡</div>
        </div>
      </div>
      <div class="course-block cb-sand">
        <div class="cb-icon">🍦</div>
        <div>
          <div class="cb-time">14:30 〜 15:20</div>
          <div class="cb-title">おやつ・おみやげ・しゅっぱつじゅんび</div>
          <div class="cb-desc">トイレをすませて15:30にしゅっぱつしよう🚗</div>
        </div>
      </div>
    </div>
  </div>

  <!-- ⑤ おかね -->

  <div class="section-card theme-sun" id="cost">
    <div class="section-header">
      <div class="section-icon">💰</div>
      <div class="section-title">⑤ おかねのまとめ</div>
    </div>
    <div class="section-body">
      <table class="cost-table">
        <tr>
          <td><div class="cost-label">👨‍👩‍👧 にゅうじょうりょう（おとな）</div><div class="cost-sub">600えん × 2にん</div></td>
          <td>1,200えん</td>
        </tr>
        <tr>
          <td><div class="cost-label">🧒 にゅうじょうりょう（しょうがくせい）</div><div class="cost-sub">100えん × 2にん</div></td>
          <td>200えん</td>
        </tr>
        <tr>
          <td><div class="cost-label">🅿️ ちゅうしゃじょう</div><div class="cost-sub">ふつうしゃ</div></td>
          <td>200えん</td>
        </tr>
        <tr class="cost-total-row">
          <td>🎉 ごうけい</td>
          <td>1,600えん</td>
        </tr>
      </table>
    </div>
  </div>

  <!-- ⑥ もちもの -->

  <div class="section-card theme-leaf" id="checklist">
    <div class="section-header">
      <div class="section-icon">✅</div>
      <div class="section-title">⑥ もちものチェックリスト</div>
    </div>
    <div class="section-body">
      <div class="check-count" id="checkCount">0 / 7 チェックずみ</div>
      <div class="check-progress"><div class="check-progress-bar" id="progressBar"></div></div>
      <div class="checklist">
        <div class="check-item" onclick="toggleCheck(this)">
          <div class="check-box"></div>
          <div class="check-emoji">🧢</div>
          <div class="check-text">ぼうし</div>
        </div>
        <div class="check-item" onclick="toggleCheck(this)">
          <div class="check-box"></div>
          <div class="check-emoji">💧</div>
          <div class="check-text">のみもの</div>
        </div>
        <div class="check-item" onclick="toggleCheck(this)">
          <div class="check-box"></div>
          <div class="check-emoji">🍙</div>
          <div class="check-text">かるいたべもの</div>
        </div>
        <div class="check-item" onclick="toggleCheck(this)">
          <div class="check-box"></div>
          <div class="check-emoji">🍬</div>
          <div class="check-text">
            おやつ
            <span class="check-note">300えんまで</span>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this)">
          <div class="check-box"></div>
          <div class="check-emoji">👕</div>
          <div class="check-text">
            きがえ
            <span class="check-note">1セット</span>
          </div>
        </div>
        <div class="check-item" onclick="toggleCheck(this)">
          <div class="check-box"></div>
          <div class="check-emoji">🧻</div>
          <div class="check-text">ウェットティッシュ</div>
        </div>
        <div class="check-item" onclick="toggleCheck(this)">
          <div class="check-box"></div>
          <div class="check-emoji">📒</div>
          <div class="check-text">
            シールてちょう
            <span class="check-note">おきにいりのシールをはろう！</span>
          </div>
        </div>
      </div>
      <div style="margin-top:10px;text-align:center;font-size:0.8rem;color:#bbb;font-weight:600;">タップしてチェック！</div>
    </div>
  </div>

  <!-- ⑦ ちゅうしゃじょう -->

  <div class="section-card theme-leaf" id="parking">
    <div class="section-header">
      <div class="section-icon">🅿️</div>
      <div class="section-title">⑦ ちゅうしゃじょう・かいえんじょうほう</div>
    </div>
    <div class="section-body">
      <div class="parking-card">
        <div class="parking-name">⭐ おすすめ：ひがしもんちゅうしゃじょう</div>
        <div class="parking-note">
          🎠 ゆうえんちにちかくて、こどもづれにさいてき！<br>
          💴 ふつうしゃ 200えん（やすい！）<br>
          📍 とうちゃくしたら、まずひがしもんへ
        </div>
      </div>
      <div class="open-info">
        <div class="open-chip green">
          <div class="oc-label">🌅 かいえんじかん</div>
          <div class="oc-value">9:00</div>
        </div>
        <div class="open-chip coral">
          <div class="oc-label">🚪 さいしゅうにゅうえん</div>
          <div class="oc-value">16:00</div>
        </div>
      </div>
      <a href="https://www.nonhoi.jp" target="_blank" class="map-btn">
        🌐 のんほいパーク こうしきサイトをひらく
      </a>
    </div>
  </div>

  <!-- ⑧ ちゅうい -->

  <div class="section-card theme-sand" id="notes">
    <div class="section-header">
      <div class="section-icon">⚠️</div>
      <div class="section-title">⑧ ちゅういすること</div>
    </div>
    <div class="section-body">
      <div class="warn-list">
        <div class="warn-item">
          <div class="warn-icon">🎌</div>
          <div class="warn-text">GWのおやすみなので、こうえんはとってもこむよ！とくにひるすぎはこむから、ごぜんちゅうにうごこう。</div>
        </div>
        <div class="warn-item">
          <div class="warn-icon">🌅</div>
          <div class="warn-text">どうぶつえんはごぜんちゅうにまわろう。あさのほうがすずしくてきもちいい！</div>
        </div>
        <div class="warn-item">
          <div class="warn-icon">🍜</div>
          <div class="warn-text">おひるごはんは11:30にはやくたべよう。12じをすぎるとしょくどうがこむよ。</div>
        </div>
        <div class="warn-item">
          <div class="warn-icon">🚗</div>
          <div class="warn-text">15:30にしゅっぱつできれば、じゅうたいしても19じまでにはかえれるよ！</div>
        </div>
      </div>
    </div>
  </div>

</div>

<div class="footer">
  <span class="footer-emoji">🦁🐘🦒🎠🦋</span>
  みゆちゃん・ゆらちゃん、たのしんでね！<br>
  <span style="color:#ccc;">4がつ29にちのしおり ｜ のんほいパークひがえりりょこう</span>
</div>

<script>
  const TOTAL = 7;

  function toggleCheck(el) {
    el.classList.toggle('checked');
    el.querySelector('.check-box').textContent = el.classList.contains('checked') ? '✓' : '';
    updateProgress();
  }

  function updateProgress() {
    const checked = document.querySelectorAll('.check-item.checked').length;
    document.getElementById('checkCount').textContent = `${checked} / ${TOTAL} チェックずみ`;
    document.getElementById('progressBar').style.width = `${(checked / TOTAL) * 100}%`;
  }

  function goTo(id) {
    document.getElementById(id).scrollIntoView({ behavior: 'smooth', block: 'start' });
  }

  const sections = ['cover','schedule','route','course','cost','checklist','parking','notes'];
  const navBtns = document.querySelectorAll('.nav-btn');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        const idx = sections.indexOf(entry.target.id);
        navBtns.forEach(b => b.classList.remove('active'));
        if (idx >= 0) navBtns[idx].classList.add('active');
      }
    });
  }, { threshold: 0.3 });
  sections.forEach(id => {
    const el = document.getElementById(id);
    if (el) observer.observe(el);
  });
</script>

</body>
</html>
