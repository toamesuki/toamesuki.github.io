<style>
  /*
    朝霧 ROUTE homepage
    Put this whole file in index.md.

    Image files to upload later:
    /assets/images/bg-page.png
    /assets/images/bg-panel.png
    /assets/images/header-banner.png
    /assets/images/profile-icon.png
    /assets/images/mini-miu.png
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

    Audio/video files to upload later:
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

  /* makes it wider if you are using the default GitHub Pages / Minima layout */
  .page-content,
  .page-content .wrapper,
  .post,
  .post-content {
    max-width: none !important;
    padding: 0 !important;
    margin: 0 !important;
  }

  .site-header,
  .site-footer,
  .post-header {
    display: none !important;
  }

  html {
    scroll-behavior: smooth;
  }

  body {
    margin: 0;
    color: var(--ink);
    background:
      radial-gradient(circle at 10% 0%, rgba(124, 47, 56, 0.20), transparent 25%),
      radial-gradient(circle at 100% 20%, rgba(113, 136, 155, 0.20), transparent 24%),
      linear-gradient(180deg, #f7f0e8 0%, var(--page-bg) 100%);
    background-image:
      var(--page-pattern),
      radial-gradient(circle at 10% 0%, rgba(124, 47, 56, 0.20), transparent 25%),
      radial-gradient(circle at 100% 20%, rgba(113, 136, 155, 0.20), transparent 24%),
      linear-gradient(180deg, #f7f0e8 0%, var(--page-bg) 100%);
    background-repeat: repeat, no-repeat, no-repeat, no-repeat;
    font-family:
      "Georgia",
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
    max-width: 100%;
    display: block;
  }

  .route-shell {
    width: min(1220px, calc(100% - 28px));
    margin: 24px auto 56px;
  }

  .route-frame {
    border: 1px solid rgba(124, 47, 56, 0.25);
    border-radius: 26px;
    background:
      linear-gradient(rgba(255, 250, 244, 0.92), rgba(255, 250, 244, 0.92)),
      var(--panel-pattern);
    background-repeat: repeat;
    box-shadow: 0 18px 45px var(--shadow);
    overflow: hidden;
    position: relative;
  }

  .top-ribbon {
    display: flex;
    justify-content: space-between;
    gap: 12px;
    align-items: center;
    padding: 8px 18px;
    background: var(--dark);
    color: #fffaf4;
    font-size: 12px;
    letter-spacing: 0.08em;
  }

  .top-ribbon a {
    color: #fffaf4;
    opacity: 0.88;
  }

  .top-ribbon a:hover {
    color: var(--yellow);
    text-decoration: none;
  }

  .hero {
    min-height: 320px;
    padding: 28px;
    display: grid;
    grid-template-columns: 1fr 320px;
    gap: 22px;
    align-items: end;
    position: relative;
    overflow: hidden;
    background:
      linear-gradient(90deg, rgba(41, 38, 44, 0.70), rgba(41, 38, 44, 0.18)),
      url("/assets/images/header-banner.png");
    background-size: cover;
    background-position: center;
  }

  .hero::before {
    content: "";
    position: absolute;
    inset: 0;
    background:
      repeating-linear-gradient(
        0deg,
        rgba(255,255,255,0.06) 0 1px,
        transparent 1px 6px
      );
    pointer-events: none;
    mix-blend-mode: screen;
  }

  .hero-titlebox {
    position: relative;
    z-index: 1;
    max-width: 680px;
    background: rgba(27, 24, 29, 0.62);
    border: 1px solid rgba(255, 250, 244, 0.36);
    border-radius: 20px;
    padding: 24px;
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
  }

  .hero-title small {
    display: block;
    margin-top: 10px;
    font-size: 16px;
    letter-spacing: 0.22em;
    color: #eadfce;
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
    border-radius: 22px;
    border: 1px solid rgba(255, 250, 244, 0.46);
    background:
      linear-gradient(rgba(255,250,244,0.16), rgba(255,250,244,0.58)),
      url("/assets/images/mini-miu.png");
    background-size: cover;
    background-position: center;
    box-shadow: 0 12px 30px rgba(0,0,0,0.22);
  }

  .hero-art-card::after {
    content: "main visual slot";
    position: absolute;
    right: 12px;
    bottom: 12px;
    background: rgba(255, 250, 244, 0.88);
    color: var(--muted);
    border: 1px solid var(--line);
    border-radius: 999px;
    padding: 5px 10px;
    font-size: 11px;
  }

  .route-layout {
    display: grid;
    grid-template-columns: 265px minmax(0, 1fr) 285px;
    gap: 18px;
    padding: 20px;
    align-items: start;
  }

  .panel,
  .main-card {
    border: 1px solid var(--line);
    border-radius: 20px;
    background:
      linear-gradient(rgba(255, 250, 244, 0.94), rgba(255, 250, 244, 0.94)),
      var(--panel-pattern);
    background-repeat: repeat;
    box-shadow: 0 8px 18px rgba(50, 37, 35, 0.08);
  }

  .panel {
    padding: 14px;
    position: sticky;
    top: 16px;
  }

  .main-card {
    padding: 20px;
    position: relative;
    overflow: hidden;
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
  }

  .panel-title::before {
    content: "✦";
    color: var(--yellow);
  }

  .profile-icon {
    width: 172px;
    height: 172px;
    margin: 2px auto 12px;
    border-radius: 24px;
    border: 1px solid var(--line);
    background:
      linear-gradient(rgba(255,250,244,0.05), rgba(255,250,244,0.20)),
      url("/assets/images/profile-icon.png");
    background-size: cover;
    background-position: center;
    box-shadow: 0 10px 20px rgba(50, 37, 35, 0.14);
  }

  .name-plate {
    text-align: center;
    padding: 10px;
    border: 1px dashed var(--line);
    border-radius: 16px;
    background: rgba(248, 239, 231, 0.78);
    margin-bottom: 12px;
  }

  .name-plate strong {
    display: block;
    color: var(--red);
    font-size: 18px;
    letter-spacing: 0.08em;
  }

  .name-plate span {
    display: block;
    color: var(--muted);
    font-size: 12px;
    margin-top: 4px;
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
    border-radius: 999px;
    border: 1px solid var(--line);
    background: #fffdf9;
    color: var(--ink);
    font-size: 13px;
  }

  .category-list a:hover {
    background: #f3e1dc;
    color: var(--red);
    text-decoration: none;
    transform: translateX(2px);
  }

  .category-list em {
    font-style: normal;
    color: var(--muted);
    font-size: 11px;
  }

  .mini-note {
    margin-top: 12px;
    padding: 12px;
    border-radius: 16px;
    background: #f3ebe2;
    border: 1px solid rgba(216, 201, 189, 0.75);
    color: var(--muted);
    font-size: 12px;
    line-height: 1.7;
  }

  .tiny-banner {
    margin-top: 12px;
    border-radius: 14px;
    overflow: hidden;
    border: 1px solid var(--line);
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
    text-align: center;
    border-radius: 999px;
    border: 1px solid var(--red);
    background: var(--red);
    color: #fffaf4 !important;
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
  }

  .section p {
    margin: 0 0 12px;
    line-height: 1.85;
    font-size: 14px;
  }

  .notice-box {
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    gap: 14px;
  }

  .notice-copy {
    padding: 16px;
    border-radius: 18px;
    background: rgba(255,255,255,0.62);
    border: 1px solid var(--line);
  }

  .stamp-card {
    min-height: 210px;
    border-radius: 18px;
    border: 1px dashed var(--line);
    background:
      linear-gradient(rgba(255,250,244,0.35), rgba(255,250,244,0.90)),
      url("/assets/images/banner-main.png");
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: end;
    padding: 12px;
  }

  .stamp-card span {
    display: inline-block;
    border: 1px solid var(--line);
    border-radius: 999px;
    background: rgba(255,250,244,0.92);
    padding: 5px 10px;
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
    border-radius: 999px;
    border: 1px solid var(--red);
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
    border-radius: 999px;
    border: 1px solid var(--line);
    background: #fffdf9;
    margin-bottom: 16px;
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
    border-radius: 18px;
    border: 1px solid var(--line);
    background: #fffdf9;
    padding: 14px;
    min-height: 112px;
    overflow: hidden;
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
    color: var(--red);
    margin-bottom: 6px;
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
    min-height: 170px;
    border-radius: 18px;
    border: 1px solid var(--line);
    background-size: cover;
    background-position: center;
    overflow: hidden;
    position: relative;
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
    border-radius: 999px;
    background: rgba(255,250,244,0.90);
    border: 1px solid var(--line);
    padding: 5px 10px;
    color: var(--muted);
    font-size: 11px;
  }

  .rules-box {
    border-radius: 18px;
    border: 1px solid rgba(124, 47, 56, 0.36);
    background: #fff5f3;
    padding: 15px;
    line-height: 1.75;
    font-size: 13px;
  }

  .rules-box ul {
    margin: 8px 0 0 18px;
    padding: 0;
  }

  .search-input {
    width: 100%;
    box-sizing: border-box;
    border: 1px solid var(--line);
    border-radius: 999px;
    padding: 10px 12px;
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
    border-radius: 16px;
    overflow: hidden;
    border: 1px solid var(--line);
    background: #fffdf9;
  }

  .cal-head {
    padding: 10px;
    text-align: center;
    background: var(--dark);
    color: #fffaf4;
    letter-spacing: 0.14em;
    font-size: 12px;
  }

  .cal-grid {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    text-align: center;
    font-size: 11px;
  }

  .cal-grid div {
    padding: 7px 2px;
    border-right: 1px solid #eee4dc;
    border-bottom: 1px solid #eee4dc;
    min-height: 18px;
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

  .audio-box audio,
  .video-box video {
    width: 100%;
  }

  .audio-box {
    border-radius: 16px;
    background: #fffdf9;
    border: 1px solid var(--line);
    padding: 12px;
  }

  .track-title {
    margin-bottom: 8px;
    color: var(--muted);
    font-size: 12px;
    line-height: 1.5;
  }

  .video-box {
    border-radius: 16px;
    overflow: hidden;
    background: #fffdf9;
    border: 1px solid var(--line);
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
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid var(--line);
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
    text-align: center;
    padding: 18px 20px 22px;
    color: var(--muted);
    font-size: 12px;
    border-top: 1px solid var(--line);
    background: rgba(243, 235, 226, 0.82);
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
    top: 350px;
    opacity: 0.94;
  }

  .deco-rain {
    width: 76px;
    left: 20px;
    top: 410px;
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
      padding: 16px;
      min-height: auto;
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
      padding: 12px;
      gap: 12px;
    }

    .main-card,
    .panel {
      border-radius: 16px;
      padding: 12px;
    }

    .category-list a {
      padding: 11px 12px;
    }

    .ticker span {
      animation-duration: 16s;
    }
  }
</style>
