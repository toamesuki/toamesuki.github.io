<style>
  :root {
    --bg: #f7f2ec;
    --paper: #fffaf5;
    --ink: #2f2f35;
    --muted: #8c8782;
    --line: #d8cec3;
    --mist: #9faab5;
    --red: #7a2d35;
    --red-soft: #b45b68;
    --shadow: rgba(67, 55, 48, 0.13);
  }
  body {
    background:
      radial-gradient(circle at top left, rgba(180, 91, 104, 0.12), transparent 28%),
      linear-gradient(180deg, #f8f3ee 0%, #eee7df 100%);
    color: var(--ink);
  }
  a {
    color: var(--red);
    text-decoration: none;
  }
  a:hover {
    color: var(--red-soft);
    text-decoration: underline;
  }
  .sb-wrap {
    max-width: 980px;
    margin: 0 auto;
    padding: 36px 18px 60px;
    font-family: "Georgia", "Times New Roman", "Yu Mincho", "Hiragino Mincho ProN", serif;
  }
  .sb-card {
    background: rgba(255, 250, 245, 0.92);
    border: 1px solid var(--line);
    box-shadow: 0 10px 30px var(--shadow);
    border-radius: 22px;
    overflow: hidden;
  }
  .sb-header {
    position: relative;
    min-height: 260px;
    background:
      linear-gradient(rgba(47, 47, 53, 0.22), rgba(47, 47, 53, 0.42)),
      url("/assets/images/header.png");
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: end;
    padding: 34px;
    color: #fffaf5;
  }
  .sb-header-fallback {
    background:
      linear-gradient(135deg, rgba(122,45,53,0.9), rgba(47,47,53,0.92)),
      repeating-linear-gradient(90deg, rgba(255,255,255,0.05) 0 1px, transparent 1px 8px);
  }
  .sb-titlebox {
    background: rgba(28, 24, 25, 0.52);
    border: 1px solid rgba(255, 250, 245, 0.35);
    border-radius: 18px;
    padding: 22px 24px;
    backdrop-filter: blur(4px);
  }
  .sb-kicker {
    font-size: 13px;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    opacity: 0.85;
  }
  .sb-title {
    margin: 8px 0 4px;
    font-size: 42px;
    line-height: 1.05;
    letter-spacing: 0.04em;
  }
  .sb-subtitle {
    margin: 0;
    font-size: 16px;
    opacity: 0.95;
  }
  .sb-body {
    display: grid;
    grid-template-columns: 250px 1fr;
    gap: 24px;
    padding: 26px;
  }
  .sb-sidebar {
    border-right: 1px dashed var(--line);
    padding-right: 20px;
  }
  .sb-icon {
    width: 160px;
    height: 160px;
    margin: 0 auto 18px;
    border-radius: 18px;
    border: 1px solid var(--line);
    background:
      url("/assets/images/icon.png"),
      linear-gradient(135deg, #e4ddd5, #fffaf5);
    background-size: cover;
    background-position: center;
    box-shadow: 0 8px 18px var(--shadow);
  }
  .sb-side-title {
    font-size: 13px;
    letter-spacing: 0.2em;
    color: var(--muted);
    text-align: center;
    margin-bottom: 12px;
  }
  .sb-menu {
    display: grid;
    gap: 9px;
  }
  .sb-menu a {
    display: block;
    padding: 10px 12px;
    border: 1px solid var(--line);
    border-radius: 999px;
    background: #fffdf9;
    text-align: center;
    font-size: 14px;
    color: var(--ink);
  }
  .sb-menu a:hover {
    background: #f4e8e4;
    color: var(--red);
    text-decoration: none;
  }
  .sb-mini {
    margin-top: 18px;
    padding: 14px;
    border-radius: 14px;
    background: #f3ece5;
    font-size: 12px;
    line-height: 1.7;
    color: var(--muted);
  }
  .sb-main {
    min-width: 0;
  }
  .sb-section {
    margin-bottom: 26px;
  }
  .sb-section h2 {
    font-size: 18px;
    letter-spacing: 0.08em;
    border-bottom: 1px solid var(--line);
    padding-bottom: 8px;
    margin: 0 0 14px;
    color: var(--red);
  }
  .sb-section p {
    line-height: 1.9;
    margin: 0 0 12px;
  }
  .sb-buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 16px;
  }
  .sb-button {
    display: inline-block;
    padding: 10px 15px;
    border-radius: 999px;
    background: var(--red);
    color: #fffaf5 !important;
    border: 1px solid var(--red);
    font-size: 14px;
  }
  .sb-button:hover {
    background: var(--red-soft);
    text-decoration: none;
  }
  .sb-button.secondary {
    background: transparent;
    color: var(--red) !important;
  }
  .sb-button.secondary:hover {
    background: #f4e8e4;
  }
  .sb-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 14px;
  }
  .sb-box {
    border: 1px solid var(--line);
    border-radius: 16px;
    padding: 16px;
    background: #fffdf9;
    line-height: 1.75;
  }
  .sb-box strong {
    color: var(--red);
  }
  .sb-image-row {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 12px;
    margin-top: 14px;
  }
  .sb-image-slot {
    min-height: 120px;
    border-radius: 14px;
    border: 1px dashed var(--line);
    background:
      linear-gradient(rgba(255,250,245,0.55), rgba(255,250,245,0.85)),
      url("/assets/images/gallery-1.png");
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: end;
    padding: 10px;
    color: var(--muted);
    font-size: 12px;
  }
  .sb-image-slot:nth-child(2) {
    background-image:
      linear-gradient(rgba(255,250,245,0.55), rgba(255,250,245,0.85)),
      url("/assets/images/gallery-2.png");
  }
  .sb-image-slot:nth-child(3) {
    background-image:
      linear-gradient(rgba(255,250,245,0.55), rgba(255,250,245,0.85)),
      url("/assets/images/gallery-3.png");
  }
  .sb-warning {
    border: 1px solid rgba(122, 45, 53, 0.35);
    background: #fff7f5;
    border-radius: 16px;
    padding: 16px;
    font-size: 13px;
    line-height: 1.8;
  }
  .sb-warning ul {
    margin: 8px 0 0 18px;
    padding: 0;
  }
  .sb-footer {
    text-align: center;
    color: var(--muted);
    font-size: 12px;
    padding: 20px;
    border-top: 1px solid var(--line);
    background: #f3ece5;
  }
  @media (max-width: 760px) {
    .sb-body {
      grid-template-columns: 1fr;
    }
    .sb-sidebar {
      border-right: 0;
      border-bottom: 1px dashed var(--line);
      padding-right: 0;
      padding-bottom: 20px;
    }
    .sb-title {
      font-size: 34px;
    }
    .sb-grid,
    .sb-image-row {
      grid-template-columns: 1fr;
    }
  }
</style>
<div class="sb-wrap">
  <div class="sb-card">
<header class="sb-header sb-header-fallback">
  <div class="sb-titlebox">
    <div class="sb-kicker">personal yume / OC archive</div>
    <h1 class="sb-title">— 朝霧 ROUTE —</h1>
    <p class="sb-subtitle">朝霧美雨 × 足立透　|　a quiet backup room for fragments, dreams, and rain.</p>
  </div>
</header>
<div class="sb-body">
  <aside class="sb-sidebar">
    <div class="sb-icon"></div>
    <div class="sb-side-title">ROOM 203 MENU</div>
    <nav class="sb-menu">
      <a href="/notice/">notice</a>
      <a href="/profile/">profile</a>
      <a href="/image/">image</a>
      <a href="/text/">text</a>
      <a href="/diary/">diary</a>
      <a href="/backup/">backup</a>
      <a href="/channel/">channel</a>
    </nav>
    <div class="sb-mini">
      <strong>site note</strong><br>
      個人用OC・夢創作保管庫。<br>
      This is a personal archive for yume, OC notes, writing, and commissioned artwork.
    </div>
  </aside>
  <main class="sb-main">
    <section class="sb-section">
      <h2>はじめに / Welcome</h2>
      <p>
        ここは <strong>朝霧美雨 × 足立透</strong> を中心にした個人夢創作・OC保管サイトです。
        キャラクター設定、関係性メモ、文章、イラスト記録、依頼資料、日記のような断片を静かに置いています。
      </p>
      <p>
        This site is a small personal archive for <strong>Miu Asagiri × Tohru Adachi</strong>:
        character profiles, relationship notes, AU timelines, commissioned artwork records,
        writing fragments, and backup materials.
      </p>
      <div class="sb-buttons">
        <a class="sb-button" href="/profile/">enter profile</a>
        <a class="sb-button secondary" href="/text/">read archive</a>
        <a class="sb-button secondary" href="/image/">view gallery</a>
      </div>
    </section>
    <section class="sb-section">
      <h2>about this archive</h2>
      <div class="sb-grid">
        <div class="sb-box">
          <strong>profile</strong><br>
          OC profile, canon character notes, relationship summary, ship names, and AU setting.
        </div>
        <div class="sb-box">
          <strong>image</strong><br>
          Commission gallery, reference sheets, icons, banners, and credit notes.
        </div>
        <div class="sb-box">
          <strong>text</strong><br>
          Writing archive, short scenes, headcanons, timelines, and route fragments.
        </div>
        <div class="sb-box">
          <strong>backup</strong><br>
          Old drafts, unused ideas, request text, translation notes, and private worldbuilding scraps.
        </div>
      </div>
    </section>
    <section class="sb-section">
      <h2>featured image slots</h2>
      <p>
        Replace these placeholder paths later with your own images inside
        <code>/assets/images/</code>.
      </p>
      <div class="sb-image-row">
        <div class="sb-image-slot">/assets/images/gallery-1.png</div>
        <div class="sb-image-slot">/assets/images/gallery-2.png</div>
        <div class="sb-image-slot">/assets/images/gallery-3.png</div>
      </div>
    </section>
    <section class="sb-section">
      <h2>site rules / 禁止事項</h2>
      <div class="sb-warning">
        <strong>Please read before browsing.</strong><br>
        当サイト内の文章・画像・キャラクター設定・依頼資料はすべて個人観賞用です。
        <ul>
          <li>Do not repost, reupload, copy, trace, edit, redistribute, or claim as your own.</li>
          <li>Do not use my OC designs, writing, relationship notes, or commissioned artworks.</li>
          <li>Do not feed, train, scrape, reference, or use any content from this site for AI generation, AI datasets, AI model training, or AI image/text prompts.</li>
          <li>無断転載・無断使用・加工・トレス・自作発言・AI学習利用を禁止します。</li>
          <li>Commissioned artworks belong to their respective artists. Please follow each artist’s rules.</li>
          <li>This is an unofficial, non-commercial personal fan/yume archive.</li>
        </ul>
      </div>
    </section>
    <section class="sb-section">
      <h2>updates</h2>
      <p>
        2026.06 — site opened / archive preparing.
      </p>
      <p>
        Future updates will include profile pages, writing index, commission credits,
        banner exchange, and reference pages.
      </p>
    </section>
  </main>
</div>
<footer class="sb-footer">
  Static Bloom © personal archive. Please do not repost, copy, or use for AI training.
</footer>
  </div>
</div>
