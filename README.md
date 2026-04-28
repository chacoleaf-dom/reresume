<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>謝沛宸｜藥學資訊作品集</title>
  <meta name="description" content="謝沛宸的 GitHub Pages 作品集：藥學資訊、資料庫查詢系統、Excel/Google Sheets 資料整合與臨床決策輔助工具。" />
  <style>
    :root {
      --bg: #0d1117;
      --bg-soft: #161b22;
      --card: rgba(255, 255, 255, 0.06);
      --card-border: rgba(255, 255, 255, 0.12);
      --text: #f0f6fc;
      --muted: #8b949e;
      --brand: #2f81f7;
      --brand-2: #7c3aed;
      --success: #3fb950;
      --shadow: 0 20px 60px rgba(0, 0, 0, 0.35);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Noto Sans TC", Roboto, Arial, sans-serif;
      color: var(--text);
      background:
        radial-gradient(circle at top left, rgba(47, 129, 247, 0.28), transparent 34rem),
        radial-gradient(circle at top right, rgba(124, 58, 237, 0.22), transparent 32rem),
        var(--bg);
      line-height: 1.65;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1120px, calc(100% - 40px));
      margin: 0 auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 10;
      backdrop-filter: blur(16px);
      background: rgba(13, 17, 23, 0.72);
      border-bottom: 1px solid rgba(255, 255, 255, 0.08);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 18px 0;
    }

    .logo {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      font-weight: 800;
      letter-spacing: 0.4px;
    }

    .logo-mark {
      width: 34px;
      height: 34px;
      display: grid;
      place-items: center;
      border-radius: 11px;
      background: linear-gradient(135deg, var(--brand), var(--brand-2));
      box-shadow: 0 10px 30px rgba(47, 129, 247, 0.35);
    }

    .nav-links {
      display: flex;
      gap: 22px;
      color: var(--muted);
      font-size: 0.95rem;
    }

    .nav-links a:hover {
      color: var(--text);
    }

    .hero {
      min-height: 72vh;
      display: grid;
      grid-template-columns: 1.15fr 0.85fr;
      gap: 42px;
      align-items: center;
      padding: 82px 0 58px;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: #c9d1d9;
      background: rgba(255, 255, 255, 0.07);
      border: 1px solid var(--card-border);
      padding: 8px 12px;
      border-radius: 999px;
      font-size: 0.92rem;
      margin-bottom: 22px;
    }

    .pulse {
      width: 9px;
      height: 9px;
      border-radius: 999px;
      background: var(--success);
      box-shadow: 0 0 0 6px rgba(63, 185, 80, 0.15);
    }

    h1 {
      font-size: clamp(2.4rem, 6vw, 5.2rem);
      line-height: 1.05;
      letter-spacing: -0.06em;
      margin-bottom: 22px;
    }

    .gradient-text {
      background: linear-gradient(135deg, #79c0ff, #d2a8ff 58%, #ffa657);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .hero p {
      max-width: 680px;
      color: var(--muted);
      font-size: 1.12rem;
      margin-bottom: 30px;
    }

    .actions {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      margin-bottom: 30px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      min-height: 46px;
      padding: 0 18px;
      border-radius: 14px;
      font-weight: 700;
      transition: transform 0.2s ease, border 0.2s ease, background 0.2s ease;
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--brand), var(--brand-2));
      box-shadow: 0 16px 36px rgba(47, 129, 247, 0.24);
    }

    .btn-ghost {
      border: 1px solid var(--card-border);
      background: rgba(255, 255, 255, 0.05);
      color: #c9d1d9;
    }

    .tech-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .chip {
      color: #c9d1d9;
      background: rgba(255, 255, 255, 0.06);
      border: 1px solid rgba(255, 255, 255, 0.09);
      border-radius: 999px;
      padding: 7px 11px;
      font-size: 0.9rem;
    }

    .profile-card {
      position: relative;
      background: linear-gradient(180deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0.035));
      border: 1px solid var(--card-border);
      border-radius: 28px;
      padding: 26px;
      box-shadow: var(--shadow);
      overflow: hidden;
    }

    .profile-card::before {
      content: "";
      position: absolute;
      inset: -2px;
      background: radial-gradient(circle at 80% 10%, rgba(47, 129, 247, 0.32), transparent 18rem);
      pointer-events: none;
    }

    .profile-inner {
      position: relative;
    }

    .avatar {
      width: 82px;
      height: 82px;
      border-radius: 26px;
      display: grid;
      place-items: center;
      font-size: 2.2rem;
      font-weight: 900;
      background: linear-gradient(135deg, #2f81f7, #7c3aed);
      margin-bottom: 20px;
    }

    .profile-card h2 {
      font-size: 1.45rem;
      margin-bottom: 8px;
    }

    .profile-card p {
      color: var(--muted);
      margin-bottom: 20px;
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
      margin-top: 18px;
    }

    .stat {
      background: rgba(255, 255, 255, 0.055);
      border: 1px solid rgba(255, 255, 255, 0.08);
      border-radius: 18px;
      padding: 14px;
    }

    .stat strong {
      display: block;
      font-size: 1.35rem;
    }

    .stat span {
      color: var(--muted);
      font-size: 0.82rem;
    }

    section {
      padding: 54px 0;
    }

    .section-title {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 24px;
      margin-bottom: 24px;
    }

    .section-title h2 {
      font-size: clamp(1.7rem, 3vw, 2.6rem);
      letter-spacing: -0.04em;
    }

    .section-title p {
      color: var(--muted);
      max-width: 560px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .card {
      background: var(--card);
      border: 1px solid var(--card-border);
      border-radius: 24px;
      padding: 22px;
      box-shadow: 0 12px 36px rgba(0, 0, 0, 0.18);
      transition: transform 0.2s ease, border 0.2s ease;
    }

    .card:hover {
      transform: translateY(-4px);
      border-color: rgba(88, 166, 255, 0.45);
    }

    .card-icon {
      width: 44px;
      height: 44px;
      display: grid;
      place-items: center;
      border-radius: 15px;
      background: rgba(47, 129, 247, 0.16);
      margin-bottom: 16px;
      font-size: 1.25rem;
    }

    .card h3 {
      margin-bottom: 8px;
      font-size: 1.15rem;
    }

    .card p {
      color: var(--muted);
      font-size: 0.96rem;
    }

    .project-link {
      display: inline-flex;
      margin-top: 16px;
      color: #79c0ff;
      font-weight: 700;
    }

    .timeline {
      display: grid;
      gap: 14px;
    }

    .timeline-item {
      display: grid;
      grid-template-columns: 130px 1fr;
      gap: 18px;
      background: rgba(255, 255, 255, 0.045);
      border: 1px solid rgba(255, 255, 255, 0.09);
      border-radius: 20px;
      padding: 18px;
    }

    .timeline-date {
      color: #79c0ff;
      font-weight: 800;
    }

    .timeline-item p {
      color: var(--muted);
    }

    .cta {
      text-align: center;
      background: linear-gradient(135deg, rgba(47, 129, 247, 0.2), rgba(124, 58, 237, 0.18));
      border: 1px solid var(--card-border);
      border-radius: 30px;
      padding: 46px 24px;
      box-shadow: var(--shadow);
    }

    .cta h2 {
      font-size: clamp(1.8rem, 4vw, 3rem);
      letter-spacing: -0.04em;
      margin-bottom: 12px;
    }

    .cta p {
      color: var(--muted);
      margin-bottom: 24px;
    }

    footer {
      color: var(--muted);
      text-align: center;
      padding: 34px 0 46px;
    }

    @media (max-width: 860px) {
      .hero {
        grid-template-columns: 1fr;
        padding-top: 54px;
      }

      .grid {
        grid-template-columns: 1fr;
      }

      .section-title {
        align-items: start;
        flex-direction: column;
      }

      .nav-links {
        display: none;
      }

      .timeline-item {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <a class="logo" href="#top" aria-label="回到首頁">
        <span class="logo-mark">P</span>
        <span>Pharm Informatics Portfolio</span>
      </a>
      <nav class="nav-links" aria-label="主選單">
        <a href="#projects">專案</a>
        <a href="#skills">技能</a>
        <a href="#timeline">歷程</a>
        <a href="#contact">聯絡</a>
      </nav>
    </div>
  </header>

  <main id="top">
    <div class="container hero">
      <div>
        <div class="badge"><span class="pulse"></span> GitHub Pages Ready · 純 HTML / CSS / JS</div>
        <h1>藥學 × 資訊 ×<br /><span class="gradient-text">資料庫查詢系統</span><br />作品集</h1>
        <p>
          我關注臨床藥學、醫療資料整理、院內藥品資料庫、ICD-10-CM 檢索、ATC/AHFS 分類對照，以及可維護的 Google Apps Script / Excel / GitHub Pages 工具開發。
        </p>
        <div class="actions">
          <a class="btn btn-primary" href="#projects">查看藥學資訊專案</a>
          <a class="btn btn-ghost" href="https://github.com/" target="_blank" rel="noreferrer">前往我的 GitHub</a>
        </div>
        <div class="tech-row" aria-label="技術標籤">
          <span class="chip">HTML</span>
          <span class="chip">CSS</span>
          <span class="chip">JavaScript</span>
          <span class="chip">Google Apps Script</span>
          <span class="chip">Excel / Google Sheets</span>
          <span class="chip">GitHub Pages</span>
        </div>
      </div>

      <aside class="profile-card" aria-label="個人資料卡">
        <div class="profile-inner">
          <div class="avatar">謝</div>
          <h2>謝沛宸</h2>
          <p>藥師背景，專注於藥學資訊、臨床資料整理、院內查詢工具與醫療資料庫應用。</p>
          <div class="stats">
            <div class="stat"><strong>藥學</strong><span>Domain</span></div>
            <div class="stat"><strong>資料</strong><span>Database</span></div>
            <div class="stat"><strong>工具</strong><span>Web Apps</span></div>
          </div>
        </div>
      </aside>
    </div>

    <section id="projects">
      <div class="container">
        <div class="section-title">
          <h2>精選專案</h2>
          <p>以下整理目前最適合放在 GitHub 首頁的代表作品，呈現藥學專業與資訊工具開發能力。</p>
        </div>
        <div class="grid">
          <article class="card">
            <div class="card-icon">💊</div>
            <h3>院內藥品資料快速檢索系統</h3>
            <p>以 Google Sheets 作為資料源，支援成分、英文品名、中文品名、院內碼、健保碼與 ATC code 查詢，協助藥師快速取得藥品資訊。</p>
            <a class="project-link" href="#">查看專案 →</a>
          </article>
          <article class="card">
            <div class="card-icon">🧬</div>
            <h3>ICD-10-CM 快速檢索器</h3>
            <p>支援代碼、英文疾病名、中文疾病名查詢，並可呈現父層、子項、USE 狀態與階層式結果，適合臨床編碼與資料查核使用。</p>
            <a class="project-link" href="#">查看專案 →</a>
          </article>
          <article class="card">
            <div class="card-icon">📊</div>
            <h3>ATC / AHFS / 健保資料整合流程</h3>
            <p>整合衛福部資料集、健保給付資料、ATC/AHFS 分類與院內藥品表，建立可定期更新、可比對、可輸出的藥品資料庫雛形。</p>
            <a class="project-link" href="#">查看專案 →</a>
          </article>
        </div>
      </div>
    </section>

    <section id="skills">
      <div class="container">
        <div class="section-title">
          <h2>技能重點</h2>
          <p>結合藥師專業、資料表設計與前端查詢介面，將臨床資料轉換成可使用、可維護的資訊工具。</p>
        </div>
        <div class="grid">
          <div class="card">
            <div class="card-icon">⚙️</div>
            <h3>Web App 與查詢介面</h3>
            <p>使用 HTML、CSS、JavaScript 與 Google Apps Script 設計可部署、可維護、跨平台的資料查詢工具。</p>
          </div>
          <div class="card">
            <div class="card-icon">🗂️</div>
            <h3>醫療資料表設計</h3>
            <p>熟悉 Excel、Google Sheets、欄位標準化、資料清理、跨表合併、版本管理與定期更新流程。</p>
          </div>
          <div class="card">
            <div class="card-icon">🚀</div>
            <h3>GitHub Pages 部署</h3>
            <p>以純 HTML/CSS/JS 建置靜態網站，適合展示作品集、專案說明文件與醫療資訊工具入口。</p>
          </div>
        </div>
      </div>
    </section>

    <section id="timeline">
      <div class="container">
        <div class="section-title">
          <h2>開發歷程</h2>
          <p>從臨床需求出發，逐步把藥品資料、疾病分類與醫療資料表轉換成可查詢、可維護的資訊系統。</p>
        </div>
        <div class="timeline">
          <div class="timeline-item">
            <div class="timeline-date">2026</div>
            <div>
              <h3>建立 GitHub Pages 作品集首頁</h3>
              <p>整理藥學資訊專案、資料查詢工具與開發紀錄，作為公開展示與專案入口。</p>
            </div>
          </div>
          <div class="timeline-item">
            <div class="timeline-date">2025</div>
            <div>
              <h3>藥品與 ICD 資料查詢系統開發</h3>
              <p>將院內藥品資料、ICD-10-CM、ATC/AHFS 分類與健保資料整理成可查詢、可更新、可比對的資料流程。</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="cta">
          <h2>讓藥學專業變成可被使用的資訊工具</h2>
          <p>此頁面可作為 GitHub 作品集、專案展示、學習紀錄與未來醫療資訊工具入口。</p>
          <a class="btn btn-primary" href="mailto:your.email@example.com">聯絡我</a>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">© <span id="year"></span> 謝沛宸. Built with GitHub Pages.</div>
  </footer>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
