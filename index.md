<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>朝霧 ROUTE</title>
  <style>
    /*
      朝霧 ROUTE homepage
      Paste this whole file into index.md.
      Optional image files to upload later:
      /assets/images/bg-page.png
      /assets/images/bg-panel.png
      /assets/images/header-banner.png
      /assets/images/profile-icon.png
      /assets/images/mini-art.png
      /assets/images/deco-tv.png
      /assets/images/deco-rain.png
      /assets/images/gallery-1.png
      /assets/images/gallery-2.png
      /assets/images/gallery-3.png
      /assets/images/banner-main.png
      /assets/images/banner-small.png
      /assets/images/link-official-1.png
      /assets/images/link-official-2.png
      /assets/images/video-poster.png
      Optional media files:
      /assets/audio/bgm.mp3
      /assets/video/preview.mp4
    */
    :root {
      --page-bg: #ece5dc;
      --paper: #fffaf4;
      --paper-2: #f8efe7;
      --ink: #2b292d;
      --muted: #857c78;
      --line: #d8c9bd;
      --red: #7c2f38;
      --red-soft: #b45f6a;
      --yellow: #e2c36b;
      --blue: #71889b;
      --fog: #d9dde0;
      --dark: #29262c;
      --shadow: rgba(50, 37, 35, 0.18);
      --page-pattern: url("/assets/images/bg-page.png");
      --panel-pattern: url("/assets/images/bg-panel.png");
    }
    * {
      box-sizing: border-box;
    }
    html {
      scroll-behavior: smooth;
    }
    body {
      margin: 0;
      min-height: 100vh;
      color: var(--ink);
      background:
        var(--page-pattern),
        radial-gradient(circle at 10% 0%, rgba(124, 47, 56, 0.20), transparent 25%),
        radial-gradient(circle at 100% 20%, rgba(113, 136, 155, 0.20), transparent 24%),
        linear-gradient(180deg, #f7f0e8 0%, var(--page-bg) 100%);
      background-repeat: repeat, no-repeat, no-repeat, no-repeat;
      font-family:
        Georgia,
        "Times New Roman",
        "Yu Mincho",
        "Hiragino Mincho ProN",
        "Noto Serif JP",
        serif;
    }
    a {
      color: var(--red);
      text-decoration: none;
    }
    a:hover {
      color: var(--red-soft);
      text-decoration: underline;
    }
    img {
      display: block;
      max-width: 100%;
    }
    code {
      background: #f1e6dd;
      border: 1px solid var(--line);
      border-radius: 6px;
      padding: 1px 5px;
      font-size: 12px;
    }
    .route-shell {
      width: min(1240px, calc(100% - 28px));
      margin: 24px auto 56px;
    }
    .route-frame {
      position: relative;
      overflow: hidden;
      border: 1px solid rgba(124, 47, 56, 0.25);
      border-radius: 26px;
      background:
        linear-gradient(rgba(255, 250, 244, 0.94), rgba(255, 250, 244, 0.94)),
        var(--panel-pattern);
      background-repeat: repeat;
      box-shadow: 0 18px 45px var(--shadow);
    }
    .top-ribbon {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 12px;
      padding: 8px 18px;
      background: var(--dark);
      color: #fffaf4;
      font-size: 12px;
      letter-spacing: 0.08em;
    }
    .top-ribbon a {
      color: #fffaf4;
      opacity: 0.9;
    }
    .top-ribbon a:hover {
      color: var(--yellow);
      text-decoration: none;
    }
    .hero {
      position: relative;
      display: grid;
      grid-template-columns: minmax(0, 1fr) 320px;
      gap: 22px;
      align-items: end;
      min-height: 330px;
      padding: 28px;
      overflow: hidden;
      background:
        linear-gradient(90deg, rgba(41, 38, 44, 0.72), rgba(41, 38, 44, 0.18)),
        url("/assets/images/header-banner.png");
      background-size: cover;
      background-position: center;
    }
    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      pointer-events: none;
      background:
        repeating-linear-gradient(
          0deg,
          rgba(255,255,255,0.06) 0 1px,
          transparent 1px 6px
        );
      mix-blend-mode: screen;
    }
    .hero-titlebox {
      position: relative;
      z-index: 1;
      max-width: 720px;
      padding: 24px;
      border: 1px solid rgba(255, 250, 244, 0.36);
      border-radius: 20px;
      background: rgba(27, 24, 29, 0.64);
      color: #fffaf4;
      backdrop-filter: blur(5px);
    }
    .kicker {
      font-size: 12px;
      letter-spacing: 0.25em;
      text-transform: uppercase;
      color: #eadfce;
    }
    .hero-title {
      margin: 8px 0 6px;
      font-size: clamp(42px, 7vw, 76px);
      line-height: 0.95;
      letter-spacing: 0.04em;
      font-weight: normal;
    }
    .hero-title small {
      display: block;
      margin-top: 10px;
      color: #eadfce;
      font-size: 16px;
      letter-spacing: 0.22em;
    }
    .hero-text {
      margin: 14px 0 0;
      font-size: 15px;
      line-height: 1.8;
    }
    .hero-art-card {
      position: relative;
      z-index: 1;
      align-self: stretch;
      min-height: 230px;
      border: 1px solid rgba(255, 250, 244, 0.46);
      border-radius: 22px;
      background:
        linear-gradient(rgba(255,250,244,0.12), rgba(255,250,244,0.58)),
        url("/assets/images/mini-art.png");
      background-size: cover;
      background-position: center;
      box-shadow: 0 12px 30px rgba(0,0,0,0.22);
    }
    .hero-art-card::after {
      content: "main visual slot";
      position: absolute;
      right: 12px;
      bottom: 12px;
      padding: 5px 10px;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: rgba(255, 250, 244, 0.88);
      color: var(--muted);
      font-size: 11px;
    }
    .route-layout {
      display: grid;
      grid-template-columns: 285px minmax(0, 1fr) 305px;
      gap: 18px;
      align-items: start;
      padding: 20px;
    }
    .panel,
    .main-card {
      border: 1px solid var(--line);
      border-radius: 20px;
      background:
        linear-gradient(rgba(255, 250, 244, 0.95), rgba(255, 250, 244, 0.95)),
        var(--panel-pattern);
      background-repeat: repeat;
      box-shadow: 0 8px 18px rgba(50, 37, 35, 0.08);
    }
    .panel {
      position: sticky;
      top: 16px;
      padding: 14px;
    }
    .main-card {
      position: relative;
      overflow: hidden;
      padding: 20px;
    }
    .panel-title {
      display: flex;
      align-items: center;
      gap: 8px;
      margin: 0 0 12px;
      padding: 8px 10px;
      border-radius: 14px;
      background: var(--dark);
      color: #fffaf4;
      font-size: 13px;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      font-weight: normal;
    }
    .panel-title::before {
      content: "✦";
      color: var(--yellow);
    }
    .profile-icon {
      width: 178px;
      height: 178px;
      margin: 2px auto 12px;
      border: 1px solid var(--line);
      border-radius: 24px;
      background:
        linear-gradient(rgba(255,250,244,0.05), rgba(255,250,244,0.20)),
        url("/assets/images/profile-icon.png");
      background-size: cover;
      background-position: center;
      box-shadow: 0 10px 20px rgba(50, 37, 35, 0.14);
    }
    .name-plate {
      margin-bottom: 12px;
      padding: 10px;
      border: 1px dashed var(--line);
      border-radius: 16px;
      background: rgba(248, 239, 231, 0.78);
      text-align: center;
    }
    .name-plate strong {
      display: block;
      color: var(--red);
      font-size: 18px;
      letter-spacing: 0.08em;
    }
    .name-plate span {
      display: block;
      margin-top: 4px;
      color: var(--muted);
      font-size: 12px;
    }
    .category-list {
      display: grid;
      gap: 8px;
    }
    .category-list a {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 8px;
      padding: 9px 11px;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: #fffdf9;
      color: var(--ink);
      font-size: 13px;
      transition: 0.16s ease;
    }
    .category-list a:hover {
      transform: translateX(2px);
      background: #f3e1dc;
      color: var(--red);
      text-decoration: none;
    }
    .category-list em {
      color: var(--muted);
      font-size: 11px;
      font-style: normal;
    }
    .mini-note {
      margin-top: 12px;
      padding: 12px;
      border: 1px solid rgba(216, 201, 189, 0.75);
      border-radius: 16px;
      background: #f3ebe2;
      color: var(--muted);
      font-size: 12px;
      line-height: 1.7;
    }
    .tiny-banner {
      margin-top: 12px;
      overflow: hidden;
      border: 1px solid var(--line);
      border-radius: 14px;
      background: #fff;
    }
    .tiny-banner img {
      width: 100%;
      height: 68px;
      object-fit: cover;
    }
    .clap-button {
      display: block;
      margin-top: 10px;
      padding: 9px 12px;
      border: 1px solid var(--red);
      border-radius: 999px;
      background: var(--red);
      color: #fffaf4 !important;
      text-align: center;
      font-size: 12px;
    }
    .clap-button:hover {
      background: var(--red-soft);
      text-decoration: none;
    }
    .section {
      margin-bottom: 22px;
    }
    .section:last-child {
      margin-bottom: 0;
    }
    .section h2 {
      margin: 0 0 12px;
      padding-bottom: 8px;
      border-bottom: 1px solid var(--line);
      color: var(--red);
      font-size: 19px;
      letter-spacing: 0.08em;
      font-weight: normal;
    }
    .section p {
      margin: 0 0 12px;
      font-size: 14px;
      line-height: 1.85;
    }
    .notice-box {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 14px;
    }
    .notice-copy {
      padding: 16px;
      border: 1px solid var(--line);
      border-radius: 18px;
      background: rgba(255,255,255,0.64);
    }
    .stamp-card {
      display: flex;
      align-items: end;
      min-height: 210px;
      padding: 12px;
      border: 1px dashed var(--line);
      border-radius: 18px;
      background:
        linear-gradient(rgba(255,250,244,0.28), rgba(255,250,244,0.88)),
        url("/assets/images/banner-main.png");
      background-size: cover;
      background-position: center;
    }
    .stamp-card span {
      display: inline-block;
      padding: 5px 10px;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: rgba(255,250,244,0.92);
      color: var(--muted);
      font-size: 11px;
    }
    .button-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 14px;
    }
    .route-button {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 14px;
      border: 1px solid var(--red);
      border-radius: 999px;
      background: var(--red);
      color: #fffaf4 !important;
      font-size: 13px;
    }
    .route-button:hover {
      background: var(--red-soft);
      text-decoration: none;
    }
    .route-button.secondary {
      background: #fffaf4;
      color: var(--red) !important;
    }
    .route-button.secondary:hover {
      background: #f3e1dc;
    }
    .ticker {
      overflow: hidden;
      margin-bottom: 16px;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: #fffdf9;
    }
    .ticker span {
      display: inline-block;
      white-space: nowrap;
      padding: 8px 0;
      color: var(--muted);
      font-size: 12px;
      animation: tickerMove 22s linear infinite;
    }
    @keyframes tickerMove {
      from { transform: translateX(100%); }
      to { transform: translateX(-100%); }
    }
    .archive-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 12px;
    }
    .archive-card {
      position: relative;
      min-height: 112px;
      overflow: hidden;
      padding: 14px;
      border: 1px solid var(--line);
      border-radius: 18px;
      background: #fffdf9;
      color: var(--ink);
    }
    a.archive-card:hover {
      text-decoration: none;
      transform: translateY(-1px);
      box-shadow: 0 8px 16px rgba(50, 37, 35, 0.10);
    }
    .archive-card::after {
      content: "";
      position: absolute;
      right: -24px;
      bottom: -24px;
      width: 82px;
      height: 82px;
      border-radius: 50%;
      background: rgba(124, 47, 56, 0.08);
    }
    .archive-card strong {
      display: block;
      margin-bottom: 6px;
      color: var(--red);
    }
    .archive-card p {
      margin: 0;
      color: var(--muted);
      font-size: 12px;
      line-height: 1.65;
    }
    .gallery-strip {
      display: grid;
      grid-template-columns: 1.25fr 1fr 1fr;
      gap: 12px;
    }
    .gallery-item {
      position: relative;
      min-height: 170px;
      overflow: hidden;
      border: 1px solid var(--line);
      border-radius: 18px;
      background-size: cover;
      background-position: center;
    }
    .gallery-item:nth-child(1) {
      background-image:
        linear-gradient(rgba(255,250,244,0.10), rgba(41,38,44,0.36)),
        url("/assets/images/gallery-1.png");
    }
    .gallery-item:nth-child(2) {
      background-image:
        linear-gradient(rgba(255,250,244,0.10), rgba(41,38,44,0.36)),
        url("/assets/images/gallery-2.png");
    }
    .gallery-item:nth-child(3) {
      background-image:
        linear-gradient(rgba(255,250,244,0.10), rgba(41,38,44,0.36)),
        url("/assets/images/gallery-3.png");
    }
    .gallery-item span {
      position: absolute;
      left: 10px;
      bottom: 10px;
      padding: 5px 10px;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: rgba(255,250,244,0.90);
      color: var(--muted);
      font-size: 11px;
    }
    .rules-box {
      padding: 15px;
      border: 1px solid rgba(124, 47, 56, 0.36);
      border-radius: 18px;
      background: #fff5f3;
      font-size: 13px;
      line-height: 1.75;
    }
    .rules-box ul {
      margin: 8px 0 0 18px;
      padding: 0;
    }
    .search-input {
      width: 100%;
      padding: 10px 12px;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: #fffdf9;
      color: var(--ink);
      font-family: inherit;
    }
    .search-help {
      margin: 8px 0 0;
      color: var(--muted);
      font-size: 11px;
      line-height: 1.6;
    }
    .calendar {
      overflow: hidden;
      border: 1px solid var(--line);
      border-radius: 16px;
      background: #fffdf9;
    }
    .cal-head {
      padding: 10px;
      background: var(--dark);
      color: #fffaf4;
      text-align: center;
      font-size: 12px;
      letter-spacing: 0.14em;
    }
    .cal-grid {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      text-align: center;
      font-size: 11px;
    }
    .cal-grid div {
      min-height: 18px;
      padding: 7px 2px;
      border-right: 1px solid #eee4dc;
      border-bottom: 1px solid #eee4dc;
    }
    .cal-grid div:nth-child(7n) {
      border-right: 0;
    }
    .cal-dayname {
      background: #f3ebe2;
      color: var(--red);
      font-weight: bold;
    }
    .cal-rain {
      background: rgba(113, 136, 155, 0.14);
    }
    .cal-fog {
      background: rgba(124, 47, 56, 0.12);
      color: var(--red);
      font-weight: bold;
    }
    .audio-box {
      padding: 12px;
      border: 1px solid var(--line);
      border-radius: 16px;
      background: #fffdf9;
    }
    .audio-box audio,
    .video-box video {
      width: 100%;
    }
    .track-title {
      margin-bottom: 8px;
      color: var(--muted);
      font-size: 12px;
      line-height: 1.5;
    }
    .video-box {
      overflow: hidden;
      border: 1px solid var(--line);
      border-radius: 16px;
      background: #fffdf9;
    }
    .video-box video {
      display: block;
      background: #1f1d22;
    }
    .video-caption {
      padding: 9px 10px;
      color: var(--muted);
      font-size: 11px;
      line-height: 1.6;
    }
    .image-links {
      display: grid;
      gap: 9px;
    }
    .image-link {
      display: block;
      overflow: hidden;
      border: 1px solid var(--line);
      border-radius: 12px;
      background: #fffdf9;
    }
    .image-link:hover {
      transform: translateY(-1px);
      box-shadow: 0 8px 16px rgba(50, 37, 35, 0.12);
    }
    .image-link img {
      width: 100%;
      height: 54px;
      object-fit: cover;
    }
    .footer {
      padding: 18px 20px 22px;
      border-top: 1px solid var(--line);
      background: rgba(243, 235, 226, 0.82);
      color: var(--muted);
      text-align: center;
      font-size: 12px;
    }
    .deco {
      position: absolute;
      z-index: 2;
      pointer-events: none;
      filter: drop-shadow(0 8px 8px rgba(50, 37, 35, 0.18));
    }
    .deco-tv {
      width: 92px;
      right: 28px;
      top: 358px;
      opacity: 0.94;
    }
    .deco-rain {
      width: 76px;
      left: 20px;
      top: 424px;
      opacity: 0.88;
    }
    .empty-result {
      display: none;
      margin-top: 10px;
      color: var(--red);
      font-size: 12px;
    }
    .is-hidden {
      display: none !important;
    }
    @media (max-width: 980px) {
      .hero {
        grid-template-columns: 1fr;
      }
      .hero-art-card {
        min-height: 220px;
      }
      .route-layout {
        grid-template-columns: 1fr;
      }
      .panel {
        position: relative;
        top: auto;
      }
      .deco {
        display: none;
      }
      .notice-box,
      .archive-grid,
      .gallery-strip {
        grid-template-columns: 1fr;
      }
      .profile-icon {
        width: 150px;
        height: 150px;
      }
    }
    @media (max-width: 560px) {
      .route-shell {
        width: calc(100% - 14px);
        margin-top: 8px;
      }
      .route-frame {
        border-radius: 18px;
      }
      .top-ribbon {
        flex-direction: column;
        align-items: flex-start;
        padding: 9px 12px;
      }
      .hero {
        min-height: auto;
        padding: 16px;
      }
      .hero-titlebox {
        padding: 18px;
      }
      .hero-title {
        font-size: 42px;
      }
      .hero-title small {
        font-size: 12px;
      }
      .route-layout {
        gap: 12px;
        padding: 12px;
      }
      .main-card,
      .panel {
        padding: 12px;
        border-radius: 16px;
      }
      .category-list a {
        padding: 11px 12px;
      }
      .ticker span {
        animation-duration: 16s;
      }
    }
  </style>
</head>
<body>
  <div class="route-shell">
    <div class="route-frame">
  <div class="top-ribbon">
    <div>朝霧 ROUTE　/　personal yume archive</div>
    <div>
      <a href="/notice/">notice</a> ·
      <a href="/channel/">link</a> ·
      <a href="#rules">rules</a>
    </div>
  </div>
  <header class="hero">
    <div class="hero-titlebox">
      <div class="kicker">room 203 / rainy midnight / personal backup</div>
      <h1 class="hero-title">
        朝霧 ROUTE
        <small>朝霧美雨 × 足立透</small>
      </h1>
      <p class="hero-text">
        個人夢創作・OC保管庫。設定、文章、イラスト記録、依頼資料、日記の断片を置いています。
        <br>
        A small personal archive for yume, OC notes, writing fragments, commissioned artwork records, and quiet route memories.
      </p>
      <div class="button-row">
        <a class="route-button" href="/profile/">profile</a>
        <a class="route-button secondary" href="/text/">text archive</a>
        <a class="route-button secondary" href="/image/">gallery</a>
        <a class="route-button secondary" href="/channel/">channel</a>
      </div>
    </div>
    <div class="hero-art-card"></div>
  </header>
  <img class="deco deco-tv" src="/assets/images/deco-tv.png" alt="">
  <img class="deco deco-rain" src="/assets/images/deco-rain.png" alt="">
  <div class="route-layout">
    <aside class="panel left-panel">
      <h2 class="panel-title">category</h2>
      <div class="profile-icon"></div>
      <div class="name-plate">
        <strong>朝霧美雨</strong>
        <span>Asagiri Miu / yume OC</span>
      </div>
      <nav class="category-list">
        <a href="/notice/">notice <em>はじめに</em></a>
        <a href="/profile/">profile <em>設定</em></a>
        <a href="/image/">image <em>絵置き場</em></a>
        <a href="/text/">text <em>文章</em></a>
        <a href="/diary/">diary <em>日記</em></a>
        <a href="/backup/">backup <em>保管</em></a>
        <a href="/channel/">channel <em>リンク</em></a>
      </nav>
      <div class="mini-note">
        <strong>site memo</strong><br>
        Web view recommended.<br>
        個人観賞用の夢創作・OC archive.<br>
        Please read rules before using or sharing links.
      </div>
      <div class="tiny-banner">
        <img src="/assets/images/banner-small.png" alt="small banner">
      </div>
      <a class="clap-button" href="/channel/">guestbook / banner exchange</a>
    </aside>
    <main class="main-card">
      <div class="ticker">
        <span>
          ♪ welcome to 朝霧 ROUTE　—　do not repost / do not use for AI training　—　profile, image, text, diary, backup, channel　　
        </span>
      </div>
      <section class="section">
        <h2>はじめに / welcome</h2>
        <div class="notice-box">
          <div class="notice-copy">
            <p>
              ここは <strong>朝霧美雨 × 足立透</strong> を中心にした個人夢創作・OC保管サイトです。
              キャラクター設定、関係性メモ、文章、イラスト記録、依頼資料、日記のような断片を静かに置いています。
            </p>
            <p>
              This site is a personal yume / OC archive for <strong>Miu Asagiri × Tohru Adachi</strong>.
              It contains profiles, route notes, writing fragments, commissioned artwork records, and backup materials.
            </p>
            <p>
              非公式・非営利の個人サイトです。公式作品・企業・権利者とは関係ありません。
            </p>
          </div>
          <div class="stamp-card">
            <span>/assets/images/banner-main.png</span>
          </div>
        </div>
      </section>
      <section class="section">
        <h2>route menu</h2>
        <div class="archive-grid">
          <a class="archive-card searchable" href="/profile/" data-search="profile miu adachi relationship ship names setting character">
            <strong>profile</strong>
            <p>OC profile, relationship summary, name notes, route setting, and character references.</p>
          </a>
          <a class="archive-card searchable" href="/image/" data-search="image gallery commission art icon reference sheet">
            <strong>image</strong>
            <p>Commission gallery, icons, banners, reference sheets, artist credits, and visual archive.</p>
          </a>
          <a class="archive-card searchable" href="/text/" data-search="text writing scene headcanon timeline route domestic jealousy">
            <strong>text</strong>
            <p>Writing archive, short scenes, headcanons, emotional notes, and timeline fragments.</p>
          </a>
          <a class="archive-card searchable" href="/backup/" data-search="backup old drafts skeb request translation private notes">
            <strong>backup</strong>
            <p>Old drafts, unused ideas, Skeb request texts, translation notes, and private scraps.</p>
          </a>
        </div>
        <div id="emptyResult" class="empty-result">
          No matching item on this homepage.
        </div>
      </section>
      <section class="section">
        <h2>image preview</h2>
        <div class="gallery-strip">
          <a class="gallery-item" href="/image/">
            <span>gallery-1.png</span>
          </a>
          <a class="gallery-item" href="/image/">
            <span>gallery-2.png</span>
          </a>
          <a class="gallery-item" href="/image/">
            <span>gallery-3.png</span>
          </a>
        </div>
      </section>
      <section class="section">
        <h2>updates</h2>
        <div class="archive-grid">
          <div class="archive-card searchable" data-search="2026 site opened update">
            <strong>2026.06</strong>
            <p>Site opened. Homepage layout preparing. Profile, gallery, and writing archive will be added later.</p>
          </div>
          <div class="archive-card searchable" data-search="todo profile gallery banner commission credit">
            <strong>todo</strong>
            <p>Add profile pages, commission credits, banner exchange, image buttons, and writing index.</p>
          </div>
        </div>
      </section>
      <section class="section" id="rules">
        <h2>site rules / 禁止事項</h2>
        <div class="rules-box">
          <strong>Please read before browsing.</strong><br>
          当サイト内の文章・画像・キャラクター設定・依頼資料はすべて個人観賞用です。
          <ul>
            <li>Do not repost, reupload, copy, trace, edit, redistribute, or claim as your own.</li>
            <li>Do not use my OC designs, writing, relationship notes, or commissioned artworks.</li>
            <li>Do not feed, scrape, train, reference, or use any content from this site for AI generation, AI datasets, AI model training, or AI image/text prompts.</li>
            <li>無断転載・無断使用・加工・トレス・自作発言・AI学習利用を禁止します。</li>
            <li>Commissioned artworks belong to their respective artists. Please follow each artist’s rules.</li>
            <li>This is an unofficial, non-commercial personal fan/yume archive.</li>
          </ul>
        </div>
      </section>
    </main>
    <aside class="panel right-panel">
      <h2 class="panel-title">side tools</h2>
      <section class="section">
        <h2>search</h2>
        <input id="routeSearch" class="search-input" type="search" placeholder="search: profile, text, gallery...">
        <p class="search-help">
          This search filters the homepage cards only. Later, you can replace it with full-site search.
        </p>
      </section>
      <section class="section">
        <h2>calendar</h2>
        <div class="calendar">
          <div class="cal-head">JUNE 2026 / 八十神</div>
          <div class="cal-grid">
            <div class="cal-dayname">月</div>
            <div class="cal-dayname">火</div>
            <div class="cal-dayname">水</div>
            <div class="cal-dayname">木</div>
            <div class="cal-dayname">金</div>
            <div class="cal-dayname">土</div>
            <div class="cal-dayname">日</div>
            <div>1</div>
            <div>2</div>
            <div>3</div>
            <div class="cal-rain">4</div>
            <div>5</div>
            <div>6</div>
            <div>7</div>
            <div>8</div>
            <div class="cal-rain">9</div>
            <div>10</div>
            <div>11</div>
            <div>12</div>
            <div>13</div>
            <div>14</div>
            <div>15</div>
            <div>16</div>
            <div class="cal-fog">17</div>
            <div>18</div>
            <div>19</div>
            <div>20</div>
            <div>21</div>
            <div>22</div>
            <div>23</div>
            <div>24</div>
            <div class="cal-rain">25</div>
            <div>26</div>
            <div>27</div>
            <div>28</div>
            <div>29</div>
            <div>30</div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
          </div>
        </div>
      </section>
      <section class="section">
        <h2>music</h2>
        <div class="audio-box">
          <div class="track-title">
            ♪ route bgm / replace with your own permitted audio file
          </div>
          <audio controls preload="metadata" controlslist="nodownload">
            <source src="/assets/audio/bgm.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
          </audio>
        </div>
      </section>
      <section class="section">
        <h2>video</h2>
        <div class="video-box">
          <video controls preload="metadata" poster="/assets/images/video-poster.png">
            <source src="/assets/video/preview.mp4" type="video/mp4">
            Your browser does not support the video element.
          </video>
          <div class="video-caption">
            Put a short edit, trailer, PV, or commission showcase here.
          </div>
        </div>
      </section>
      <section class="section">
        <h2>official / links</h2>
        <div class="image-links">
          <a class="image-link" href="https://p-atlus.jp/p4g/" target="_blank" rel="noopener">
            <img src="/assets/images/link-official-1.png" alt="official link 1">
          </a>
          <a class="image-link" href="https://www.atlus.com/" target="_blank" rel="noopener">
            <img src="/assets/images/link-official-2.png" alt="official link 2">
          </a>
        </div>
      </section>
      <section class="section">
        <h2>banner</h2>
        <div class="mini-note">
          Banner exchange welcome.<br>
          バナー交換・リンク報告などお気軽に。
        </div>
      </section>
    </aside>
  </div>
  <footer class="footer">
    朝霧 ROUTE © personal yume / OC archive. Do not repost, copy, trace, edit, redistribute, or use for AI training.
  </footer>
</div>
  </div>
  <script>
    const routeSearch = document.getElementById("routeSearch");
    const searchableCards = document.querySelectorAll(".searchable");
    const emptyResult = document.getElementById("emptyResult");
    if (routeSearch) {
      routeSearch.addEventListener("input", function () {
        const query = routeSearch.value.toLowerCase().trim();
        let visibleCount = 0;
        searchableCards.forEach(function (card) {
          const text = (card.textContent + " " + (card.dataset.search || "")).toLowerCase();
          const shouldShow = text.includes(query);
          card.classList.toggle("is-hidden", !shouldShow);
          if (shouldShow) {
            visibleCount++;
          }
        });
        if (emptyResult) {
          emptyResult.style.display = visibleCount === 0 ? "block" : "none";
        }
      });
    }
  </script>
</body>
</html>
