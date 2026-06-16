[style.css](https://github.com/user-attachments/files/29000516/style.css)
# -/* ===========================================
   くらしハック - Common Stylesheet
   Notion風 × Apple風 / 白基調・余白・カード
=========================================== */

:root {
  --bg: #ffffff;
  --bg-soft: #fafafa;
  --bg-card: #ffffff;
  --border: #ececec;
  --text: #1d1d1f;
  --text-sub: #6e6e73;
  --text-faint: #a0a0a5;
  --accent: #2f6f4f;
  --accent-soft: #eef5f0;
  --accent-gold: #c9a227;
  --radius: 18px;
  --radius-sm: 12px;
  --shadow-sm: 0 2px 10px rgba(0,0,0,0.04);
  --shadow-md: 0 8px 30px rgba(0,0,0,0.07);
  --shadow-lg: 0 20px 60px rgba(0,0,0,0.10);
  --maxw: 1140px;
  --font: -apple-system, "SF Pro Text", "Hiragino Sans", "Noto Sans JP", "Yu Gothic", sans-serif;
}

* { box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  margin: 0;
  font-family: var(--font);
  color: var(--text);
  background: var(--bg);
  line-height: 1.75;
  -webkit-font-smoothing: antialiased;
  letter-spacing: 0.01em;
}

a { color: inherit; text-decoration: none; }

img { max-width: 100%; display: block; }

.wrap {
  max-width: var(--maxw);
  margin: 0 auto;
  padding: 0 32px;
}

/* ---------- Header ---------- */
.site-header {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(255,255,255,0.85);
  backdrop-filter: saturate(180%) blur(20px);
  border-bottom: 1px solid var(--border);
}

.site-header .wrap {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 72px;
}

.logo {
  font-size: 20px;
  font-weight: 700;
  letter-spacing: 0.02em;
  display: flex;
  align-items: center;
  gap: 8px;
}

.logo .dot { color: var(--accent); }

.nav-links {
  display: flex;
  gap: 32px;
  font-size: 14px;
  font-weight: 500;
}

.nav-links a {
  color: var(--text-sub);
  transition: color 0.2s;
}

.nav-links a:hover { color: var(--text); }

.nav-cta {
  font-size: 13px;
  font-weight: 600;
  background: var(--text);
  color: #fff;
  padding: 9px 18px;
  border-radius: 999px;
  transition: opacity 0.2s;
}

.nav-cta:hover { opacity: 0.8; }

.menu-toggle { display: none; }

/* ---------- Hero ---------- */
.hero {
  padding: 140px 0 120px;
  text-align: center;
  background:
    radial-gradient(60% 60% at 50% 0%, var(--accent-soft) 0%, rgba(255,255,255,0) 70%);
}

.hero .eyebrow {
  font-size: 13px;
  font-weight: 600;
  letter-spacing: 0.12em;
  color: var(--accent);
  text-transform: uppercase;
  margin-bottom: 22px;
}

.hero h1 {
  font-size: clamp(40px, 6vw, 72px);
  font-weight: 800;
  letter-spacing: -0.02em;
  line-height: 1.25;
  margin: 0 0 28px;
}

.hero h1 span {
  display: block;
}

.hero p.lead {
  font-size: clamp(16px, 2vw, 19px);
  color: var(--text-sub);
  max-width: 520px;
  margin: 0 auto 44px;
}

.hero-actions {
  display: flex;
  gap: 16px;
  justify-content: center;
  flex-wrap: wrap;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 15px 30px;
  border-radius: 999px;
  font-size: 15px;
  font-weight: 600;
  transition: transform 0.2s, box-shadow 0.2s, opacity 0.2s;
  border: 1px solid transparent;
}

.btn-primary {
  background: var(--text);
  color: #fff;
  box-shadow: var(--shadow-sm);
}

.btn-primary:hover { transform: translateY(-2px); box-shadow: var(--shadow-md); }

.btn-secondary {
  background: #fff;
  color: var(--text);
  border-color: var(--border);
}

.btn-secondary:hover { transform: translateY(-2px); box-shadow: var(--shadow-sm); }

/* ---------- Section heading ---------- */
.section {
  padding: 96px 0;
}

.section.alt { background: var(--bg-soft); }

.section-head {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  margin-bottom: 48px;
  gap: 24px;
  flex-wrap: wrap;
}

.section-head .tag {
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 10px;
  display: block;
}

.section-head h2 {
  font-size: clamp(26px, 3vw, 34px);
  font-weight: 800;
  letter-spacing: -0.01em;
  margin: 0;
}

.section-head p {
  color: var(--text-sub);
  font-size: 15px;
  margin: 10px 0 0;
}

.more-link {
  font-size: 14px;
  font-weight: 600;
  color: var(--accent);
  white-space: nowrap;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s;
}

.more-link:hover { border-color: var(--accent); }

/* ---------- Category Cards ---------- */
.category-scroll {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  gap: 18px;
}

.cat-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 28px 20px;
  text-align: center;
  transition: transform 0.25s ease, box-shadow 0.25s ease, border-color 0.25s;
}

.cat-card:hover {
  transform: translateY(-6px);
  box-shadow: var(--shadow-md);
  border-color: transparent;
}

.cat-card .icon {
  font-size: 30px;
  margin-bottom: 14px;
}

.cat-card .name {
  font-weight: 700;
  font-size: 15px;
  margin-bottom: 6px;
}

.cat-card .count {
  font-size: 12px;
  color: var(--text-faint);
}

/* ---------- Featured (today's pick) ---------- */
.featured-card {
  display: grid;
  grid-template-columns: 1.1fr 1fr;
  gap: 0;
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  overflow: hidden;
  box-shadow: var(--shadow-sm);
  transition: box-shadow 0.3s, transform 0.3s;
}

.featured-card:hover { box-shadow: var(--shadow-lg); transform: translateY(-4px); }

.featured-img {
  background: linear-gradient(135deg, #2f6f4f, #1d3f2c);
  min-height: 360px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 64px;
}

.featured-body {
  padding: 56px 52px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.featured-body .badge {
  display: inline-block;
  background: var(--accent-soft);
  color: var(--accent);
  font-size: 12px;
  font-weight: 700;
  padding: 6px 14px;
  border-radius: 999px;
  margin-bottom: 20px;
  width: fit-content;
}

.featured-body h3 {
  font-size: clamp(22px, 3vw, 30px);
  font-weight: 800;
  line-height: 1.45;
  margin: 0 0 16px;
}

.featured-body p {
  color: var(--text-sub);
  font-size: 15px;
  margin: 0 0 28px;
}

.featured-body .meta {
  font-size: 13px;
  color: var(--text-faint);
}

/* ---------- Article Grid ---------- */
.article-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}

.article-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  overflow: hidden;
  transition: transform 0.25s, box-shadow 0.25s;
  display: flex;
  flex-direction: column;
}

.article-card:hover { transform: translateY(-6px); box-shadow: var(--shadow-md); }

.article-thumb {
  height: 160px;
  background: var(--accent-soft);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 40px;
}

.article-body {
  padding: 24px 24px 28px;
  flex: 1;
  display: flex;
  flex-direction: column;
}

.article-cat {
  font-size: 11px;
  font-weight: 700;
  color: var(--accent);
  letter-spacing: 0.05em;
  margin-bottom: 10px;
}

.article-body h3 {
  font-size: 17px;
  font-weight: 700;
  line-height: 1.55;
  margin: 0 0 14px;
  flex: 1;
}

.article-meta {
  font-size: 12px;
  color: var(--text-faint);
  display: flex;
  justify-content: space-between;
  margin-top: auto;
}

/* ---------- Ranking ---------- */
.ranking-list {
  display: flex;
  flex-direction: column;
  border: 1px solid var(--border);
  border-radius: var(--radius);
  overflow: hidden;
  background: var(--bg-card);
}

.ranking-item {
  display: flex;
  align-items: center;
  gap: 24px;
  padding: 24px 32px;
  border-bottom: 1px solid var(--border);
  transition: background 0.2s;
}

.ranking-item:last-child { border-bottom: none; }

.ranking-item:hover { background: var(--bg-soft); }

.rank-num {
  font-size: 22px;
  font-weight: 800;
  color: var(--text-faint);
  width: 36px;
  flex-shrink: 0;
}

.ranking-item:nth-child(1) .rank-num { color: var(--accent-gold); }
.ranking-item:nth-child(2) .rank-num { color: #9ba3a8; }
.ranking-item:nth-child(3) .rank-num { color: #b08d57; }

.rank-title {
  font-weight: 600;
  font-size: 15px;
  flex: 1;
}

.rank-cat {
  font-size: 12px;
  color: var(--text-faint);
  white-space: nowrap;
}

/* ---------- Feature banner ---------- */
.feature-banner {
  border-radius: var(--radius);
  padding: 64px 56px;
  background: linear-gradient(135deg, #1d3f2c 0%, #2f6f4f 60%, #4a8f6c 100%);
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 32px;
  flex-wrap: wrap;
}

.feature-banner .label {
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  opacity: 0.75;
  margin-bottom: 14px;
}

.feature-banner h3 {
  font-size: clamp(24px, 3vw, 34px);
  font-weight: 800;
  margin: 0 0 12px;
}

.feature-banner p {
  opacity: 0.85;
  font-size: 15px;
  margin: 0;
  max-width: 420px;
}

.feature-banner .btn-secondary {
  background: #fff;
  border-color: transparent;
}

/* ---------- Tools ---------- */
.tool-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
}

.tool-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 32px 26px;
  transition: transform 0.25s, box-shadow 0.25s;
}

.tool-card:hover { transform: translateY(-6px); box-shadow: var(--shadow-md); }

.tool-card .check {
  width: 38px;
  height: 38px;
  border-radius: 50%;
  background: var(--accent-soft);
  color: var(--accent);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 16px;
  margin-bottom: 18px;
  font-weight: 700;
}

.tool-card h3 {
  font-size: 16px;
  font-weight: 700;
  margin: 0 0 10px;
}

.tool-card p {
  font-size: 13px;
  color: var(--text-sub);
  margin: 0;
}

/* ---------- Tips ---------- */
.tips-row {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.tip-card {
  background: var(--bg-card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 30px;
}

.tip-card .tip-label {
  font-size: 12px;
  font-weight: 700;
  color: var(--accent);
  letter-spacing: 0.05em;
  margin-bottom: 16px;
}

.tip-card p.tip-text {
  font-size: 15px;
  font-weight: 500;
  line-height: 1.8;
  margin: 0;
}

/* ---------- Newsletter ---------- */
.newsletter {
  background: var(--bg-soft);
  border-radius: var(--radius);
  padding: 72px 56px;
  text-align: center;
}

.newsletter .tag { color: var(--accent); }

.newsletter h2 {
  font-size: clamp(24px, 3vw, 32px);
  font-weight: 800;
  margin: 0 0 14px;
}

.newsletter p {
  color: var(--text-sub);
  font-size: 15px;
  margin: 0 0 36px;
}

.newsletter-form {
  display: flex;
  justify-content: center;
  gap: 12px;
  max-width: 460px;
  margin: 0 auto;
  flex-wrap: wrap;
}

.newsletter-form input {
  flex: 1;
  min-width: 220px;
  padding: 15px 20px;
  border-radius: 999px;
  border: 1px solid var(--border);
  font-size: 14px;
  font-family: inherit;
  background: #fff;
}

.newsletter-form input:focus {
  outline: none;
  border-color: var(--accent);
}

.newsletter-form button {
  border: none;
  cursor: pointer;
}

/* ---------- Footer ---------- */
.site-footer {
  border-top: 1px solid var(--border);
  padding: 64px 0 40px;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.4fr 1fr 1fr 1fr;
  gap: 40px;
  margin-bottom: 48px;
}

.footer-brand .logo { margin-bottom: 14px; }

.footer-brand p {
  font-size: 14px;
  color: var(--text-sub);
  max-width: 260px;
}

.footer-col h4 {
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  color: var(--text-faint);
  margin: 0 0 18px;
}

.footer-col ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.footer-col a {
  font-size: 14px;
  color: var(--text-sub);
  transition: color 0.2s;
}

.footer-col a:hover { color: var(--text); }

.footer-bottom {
  border-top: 1px solid var(--border);
  padding-top: 28px;
  font-size: 13px;
  color: var(--text-faint);
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 12px;
}

/* ---------- Article page ---------- */
.breadcrumb {
  font-size: 13px;
  color: var(--text-faint);
  margin-bottom: 24px;
}

.breadcrumb a { color: var(--text-sub); }
.breadcrumb a:hover { color: var(--accent); }

.article-page {
  max-width: 760px;
  margin: 0 auto;
  padding: 64px 32px 100px;
}

.article-page .article-cat-label {
  font-size: 12px;
  font-weight: 700;
  color: var(--accent);
  letter-spacing: 0.06em;
  margin-bottom: 18px;
}

.article-page h1 {
  font-size: clamp(28px, 4vw, 40px);
  font-weight: 800;
  line-height: 1.4;
  margin: 0 0 20px;
}

.article-page .updated {
  font-size: 13px;
  color: var(--text-faint);
  margin-bottom: 48px;
  padding-bottom: 32px;
  border-bottom: 1px solid var(--border);
}

.toc {
  background: var(--bg-soft);
  border: 1px solid var(--border);
  border-radius: var(--radius-sm);
  padding: 28px 32px;
  margin-bottom: 48px;
}

.toc h2 {
  font-size: 14px;
  font-weight: 700;
  margin: 0 0 16px;
  color: var(--text-faint);
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

.toc ol {
  margin: 0;
  padding-left: 20px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.toc a {
  font-size: 15px;
  font-weight: 500;
  color: var(--text);
}

.toc a:hover { color: var(--accent); }

.article-content h2 {
  font-size: 24px;
  font-weight: 800;
  margin: 56px 0 20px;
  padding-top: 8px;
}

.article-content h3 {
  font-size: 18px;
  font-weight: 700;
  margin: 32px 0 14px;
}

.article-content p {
  font-size: 16px;
  color: #2c2c2e;
  margin: 0 0 20px;
}

.article-content ul, .article-content ol {
  margin: 0 0 20px;
  padding-left: 24px;
}

.article-content li { margin-bottom: 8px; font-size: 16px; }

.summary-box {
  background: var(--accent-soft);
  border-radius: var(--radius-sm);
  padding: 32px;
  margin: 48px 0;
}

.summary-box h2 {
  margin-top: 0 !important;
  font-size: 18px !important;
  color: var(--accent);
}

.related-articles {
  margin-top: 64px;
  padding-top: 48px;
  border-top: 1px solid var(--border);
}

.related-articles h2 {
  font-size: 20px;
  font-weight: 800;
  margin: 0 0 28px;
}

.related-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}

/* ---------- Responsive ---------- */
@media (max-width: 900px) {
  .category-scroll { grid-template-columns: repeat(3, 1fr); }
  .article-grid { grid-template-columns: repeat(2, 1fr); }
  .tool-grid { grid-template-columns: repeat(2, 1fr); }
  .tips-row { grid-template-columns: 1fr; }
  .featured-card { grid-template-columns: 1fr; }
  .featured-img { min-height: 220px; }
  .footer-grid { grid-template-columns: 1fr 1fr; }
  .related-grid { grid-template-columns: 1fr; }
}

@media (max-width: 640px) {
  .wrap { padding: 0 20px; }
  .nav-links { display: none; }
  .hero { padding: 100px 0 80px; }
  .section { padding: 64px 0; }
  .category-scroll { grid-template-columns: repeat(2, 1fr); }
  .article-grid { grid-template-columns: 1fr; }
  .tool-grid { grid-template-columns: 1fr; }
  .footer-grid { grid-template-columns: 1fr; gap: 32px; }
  .feature-banner { padding: 40px 28px; }
  .newsletter { padding: 48px 28px; }
  .featured-body { padding: 36px 28px; }
}
