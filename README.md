:root{
  --bg: #0b1220;
  --card: #111b2e;
  --alt: #0f1930;
  --text: #e8eefc;
  --muted: #b8c3e0;
  --line: rgba(255,255,255,0.12);
  --brand: #6ea8ff;
  --brand2: #89f7d0;
  --shadow: 0 10px 30px rgba(0,0,0,.35);
}

* { box-sizing: border-box; }
html, body { height: 100%; }
body{
  margin:0;
  font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
  background: radial-gradient(1200px 600px at 20% 0%, rgba(110,168,255,.25), transparent 60%),
              radial-gradient(900px 500px at 100% 30%, rgba(137,247,208,.18), transparent 60%),
              var(--bg);
  color: var(--text);
  line-height: 1.5;
}

a{ color: inherit; text-decoration: none; }
.container{
  width: min(1100px, calc(100% - 32px));
  margin-inline: auto;
}

.site-header{
  position: sticky;
  top: 0;
  z-index: 50;
  background: rgba(11,18,32,0.75);
  backdrop-filter: blur(10px);
  border-bottom: 1px solid var(--line);
}

.header-inner{
  display:flex;
  align-items:center;
  justify-content: space-between;
  padding: 14px 0;
  gap: 16px;
}

.logo{
  font-weight: 800;
  letter-spacing: .3px;
}

.nav{
  display:flex;
  gap: 14px;
  align-items:center;
}

.nav a{
  padding: 8px 10px;
  border-radius: 10px;
  color: var(--muted);
}
.nav a:hover{ background: rgba(255,255,255,.06); color: var(--text); }

.nav-toggle{
  display:none;
  border: 1px solid var(--line);
  background: rgba(255,255,255,.04);
  color: var(--text);
  padding: 8px 10px;
  border-radius: 10px;
}

.hero{
  padding: 56px 0 22px;
}
.hero-grid{
  display:grid;
  grid-template-columns: 1.2fr .8fr;
  gap: 22px;
  align-items: start;
}

.badge{
  display:inline-block;
  border: 1px solid var(--line);
  background: rgba(255,255,255,.04);
  padding: 6px 10px;
  border-radius: 999px;
  color: var(--muted);
  margin: 0 0 10px;
  font-size: 14px;
}

h1{
  margin: 0 0 12px;
  font-size: clamp(30px, 4vw, 44px);
  line-height: 1.12;
}

.subhead{
  color: var(--muted);
  margin: 0 0 18px;
  max-width: 62ch;
}

.cta-row{ display:flex; gap: 12px; flex-wrap: wrap; }
.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap: 8px;
  border-radius: 12px;
  padding: 10px 14px;
  border: 1px solid var(--line);
  background: rgba(255,255,255,.04);
  color: var(--text);
  font-weight: 700;
}
.btn.primary{
  background: linear-gradient(135deg, rgba(110,168,255,.95), rgba(137,247,208,.65));
  border-color: transparent;
  color: #071021;
}
.btn.ghost:hover, .btn:hover{ filter: brightness(1.05); }
.btn.full{ width: 100%; }

.fineprint{ margin-top: 14px; color: var(--muted); font-size: 14px; }

.hero-card{
  background: linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02));
  border: 1px solid var(--line);
  border-radius: 16px;
  box-shadow: var(--shadow);
  padding: 16px;
}
.hero-card-title{ margin: 0 0 10px; font-size: 18px; }
.quick-picks{ margin: 0; padding-left: 18px; color: var(--muted); }
.small{ font-size: 14px; }
.muted{ color: var(--muted); }

.section{
  padding: 44px 0;
}
.section.alt{
  background: rgba(255,255,255,.03);
  border-top: 1px solid var(--line);
  border-bottom: 1px solid var(--line);
}

.section-head{
  margin-bottom: 18px;
}
.section-head h2{
  margin:0 0 6px;
  font-size: 26px;
}
.section-head p{ margin:0; color: var(--muted); }

.grid.cards{
  display:grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
}

.card{
  background: rgba(255,255,255,.04);
  border: 1px solid var(--line);
  border-radius: 16px;
  overflow: hidden;
  box-shadow: var(--shadow);
  display:flex;
  flex-direction: column;
  min-height: 240px;
}
.card-body{ padding: 16px; }
.card-footer{ padding: 16px; border-top: 1px solid var(--line); }

.pros{
  margin: 12px 0 0;
  padding-left: 18px;
  color: var(--muted);
}

.table-wrap{
  overflow:auto;
  border: 1px solid var(--line);
  border-radius: 14px;
  background: rgba(255,255,255,.03);
}
table.compare{
  width: 100%;
  border-collapse: collapse;
  min-width: 720px;
}
.compare th, .compare td{
  padding: 12px 14px;
  border-bottom: 1px solid var(--line);
  text-align: left;
}
.compare th{ color: var(--muted); font-weight: 700; }
.compare tr:last-child td{ border-bottom: none; }
.link{ color: var(--brand); font-weight: 700; }

.newsletter{
  display:flex;
  align-items:center;
  justify-content: space-between;
  gap: 16px;
  padding: 18px;
  border-radius: 16px;
  border: 1px solid var(--line);
  background: rgba(255,255,255,.04);
}
.newsletter-form{
  display:flex;
  gap: 10px;
  flex-wrap: wrap;
}
.newsletter-form input{
  width: min(360px, 80vw);
  padding: 10px 12px;
  border-radius: 12px;
  border: 1px solid var(--line);
  background: rgba(0,0,
