<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Venom Editz | Creator Analytics Dashboard</title>
<style>
:root{--bg:#0b0d13;--panel:#141823;--panel2:#191f2d;--line:#272e3d;--muted:#929bad;--text:#f5f7fb;--pink:#ff3b78;--cyan:#26d9d0;--purple:#9b7bff;--green:#45d49a}
*{box-sizing:border-box}body{margin:0;background:radial-gradient(ellipse at 80% 0%,#1a1830 0,transparent 35%),var(--bg);font-family:Inter,ui-sans-serif,system-ui,-apple-system,Segoe UI,sans-serif;color:var(--text)}
.wrap{max-width:1450px;margin:auto;padding:28px}.top{display:flex;justify-content:space-between;align-items:center;gap:18px;flex-wrap:wrap;margin-bottom:28px}.brand{display:flex;gap:13px;align-items:center}.logo{width:48px;height:48px;border-radius:15px;display:grid;place-items:center;background:linear-gradient(135deg,var(--pink),#8c59ff);font-size:24px;font-weight:900;box-shadow:0 8px 30px #ff3b7833}.eyebrow{font-size:11px;color:var(--cyan);font-weight:800;letter-spacing:2px;text-transform:uppercase}.brand h1{font-size:23px;margin:3px 0 0;letter-spacing:-.6px}.actions{display:flex;gap:10px;flex-wrap:wrap}.btn,select{background:var(--panel2);border:1px solid var(--line);color:var(--text);padding:11px 14px;border-radius:11px;font-size:13px}.btn{cursor:pointer}.btn.primary{background:var(--pink);border-color:var(--pink);font-weight:750}.hero{display:flex;justify-content:space-between;align-items:center;gap:18px;padding:22px 24px;border:1px solid var(--line);border-radius:20px;background:linear-gradient(110deg,#171b29,#171625);margin-bottom:20px}.profile{display:flex;gap:14px;align-items:center}.avatar{width:56px;height:56px;border-radius:50%;display:grid;place-items:center;background:linear-gradient(135deg,#2cdae0,#b35cff);font-size:23px;font-weight:900;color:#111}.profile h2{margin:0 0 5px;font-size:18px}.profile p{margin:0;color:var(--muted);font-size:13px}.status{font-size:11px;color:#ffcf76;border:1px solid #725b2c;background:#3a2d18;padding:7px 10px;border-radius:20px;font-weight:800;white-space:nowrap}.note{color:var(--muted);font-size:12px;margin:0 0 18px;line-height:1.6}.grid{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:15px}.card{background:linear-gradient(145deg,var(--panel),#11151e);border:1px solid var(--line);border-radius:17px;padding:19px;min-width:0}.metric-head{display:flex;justify-content:space-between;align-items:center;color:var(--muted);font-size:13px}.ico{width:34px;height:34px;display:grid;place-items:center;border-radius:10px;background:#ffffff0c;font-size:17px}.value{font-size:30px;font-weight:800;letter-spacing:-1px;margin:18px 0 8px}.trend{font-size:12px;color:var(--green)}.sub{font-size:12px;color:var(--muted)}.content{display:grid;grid-template-columns:1.45fr 1fr;gap:15px;margin-top:15px}.card h3{font-size:15px;margin:0 0 5px}.desc{color:var(--muted);font-size:12px;margin:0 0 20px}.chart{width:100%;height:210px;display:block}.legend{display:flex;gap:18px;color:var(--muted);font-size:12px;margin-top:8px}.dot{display:inline-block;width:8px;height:8px;border-radius:50%;margin-right:6px}.hours{display:grid;grid-template-columns:repeat(7,1fr);gap:7px;align-items:end;height:160px;margin:8px 0 12px}.hourcol{display:flex;flex-direction:column;justify-content:end;align-items:center;height:100%;gap:8px}.bar{width:100%;max-width:30px;border-radius:7px 7px 3px 3px;background:linear-gradient(180deg,var(--pink),#8d55ff);min-height:7px}.hourlabel{font-size:10px;color:var(--muted)}.callout{padding:12px 13px;border-radius:12px;background:#ff3b7810;border:1px solid #ff3b7833;color:#e8c8d4;font-size:12px;line-height:1.5}.bottom{display:grid;grid-template-columns:1fr 1fr;gap:15px;margin-top:15px}.rowline{display:flex;align-items:center;justify-content:space-between;padding:13px 0;border-bottom:1px solid var(--line);gap:12px;font-size:13px}.rowline:last-child{border-bottom:0}.pill{background:#202638;color:#cbd4e6;padding:5px 8px;border-radius:7px;font-size:11px}.editable{background:#0d1119;border:1px solid #343d50;color:var(--text);border-radius:8px;padding:8px;width:100%;margin-top:6px}.settings{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}.field label{font-size:11px;color:var(--muted)}.foot{text-align:center;color:#6f788b;font-size:11px;padding:25px 0 5px}.hidden{display:none}

.social-section{margin-top:16px}.social-grid{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:12px}.social-card{display:flex;align-items:center;gap:12px;padding:16px;background:linear-gradient(145deg,var(--panel),#11151e);border:1px solid var(--line);border-radius:15px;min-width:0}.social-icon{width:42px;height:42px;border-radius:12px;display:grid;place-items:center;font-size:20px;font-weight:800;flex-shrink:0}.social-meta{min-width:0;flex:1}.social-meta strong{display:block;font-size:13px;margin-bottom:5px}.social-meta span{display:block;color:var(--muted);font-size:11px;overflow-wrap:anywhere;direction:ltr;text-align:left}.social-link{display:inline-block;margin-top:8px;font-size:11px;color:var(--cyan);font-weight:750}.social-link:hover{text-decoration:underline}
@media(max-width:950px){.grid{grid-template-columns:repeat(2,minmax(0,1fr))}.content,.bottom{grid-template-columns:1fr}}@media(max-width:700px){.social-grid{grid-template-columns:repeat(2,minmax(0,1fr))}}@media(max-width:560px){.wrap{padding:16px}.brand h1{font-size:19px}.hero{align-items:flex-start;flex-direction:column}.grid{gap:10px}.card{padding:14px}.value{font-size:25px}.settings{grid-template-columns:1fr}.social-grid{grid-template-columns:1fr}.actions{width:100%}.actions>*{flex:1}.status{white-space:normal}}
</style>
</head>
<body>
<div class="wrap">
<header class="top">
  <div class="brand"><div class="logo">♪</div><div><div class="eyebrow">VENOM EDITZ · CREATOR STUDIO</div><h1>Social Media Analytics Dashboard</h1></div></div>
  <div class="actions"><select id="period" aria-label="Reporting period"><option>Last 7 days</option><option>Last 28 days</option><option>Last 60 days</option></select><button class="btn" onclick="document.getElementById('settings').classList.toggle('hidden')">⚙ Edit data</button><button class="btn primary" onclick="window.print()">Export / Print ↗</button></div>
</header>
<section class="hero">
  <div class="profile"><div class="avatar">♪</div><div><h2 id="displayName">Venom Editz</h2><p id="handle">@geniusfacts2 · TikTok Creator Overview</p></div></div>
  <span class="status">● DEMO ANALYTICS — edit with real account data</span>
</section>
<p class="note">This dashboard includes your TikTok profile and all four social links. Analytics figures are demonstration values, not live data from TikTok. Enter your current figures using “Edit data”. Automatic live follower/view counts require an authorized data connection.</p>
<section class="grid">
  <article class="card"><div class="metric-head">Total followers <span class="ico">♙</span></div><div class="value" id="followers">8,420</div><div class="trend">↑ <span id="growth">12.8%</span> <span class="sub">vs previous period</span></div></article>
  <article class="card"><div class="metric-head">Total likes <span class="ico">♥</span></div><div class="value" id="likes">126.4K</div><div class="trend">↑ 8.4% <span class="sub">engagement signal</span></div></article>
  <article class="card"><div class="metric-head">Total video views <span class="ico">▷</span></div><div class="value" id="views">1.28M</div><div class="trend">↑ 21.6% <span class="sub">vs previous period</span></div></article>
  <article class="card"><div class="metric-head">Profile views <span class="ico">◉</span></div><div class="value" id="profileViews">34.8K</div><div class="trend">↑ 6.2% <span class="sub">vs previous period</span></div></article>
</section>
<section class="content">
  <article class="card"><h3>Performance overview</h3><p class="desc">Illustrative daily views and likes · last 7 days</p>
    <svg class="chart" viewBox="0 0 620 220" preserveAspectRatio="none" role="img" aria-label="Sample line chart for views and likes">
      <defs><linearGradient id="area" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#ff3b78" stop-opacity=".3"/><stop offset="1" stop-color="#ff3b78" stop-opacity="0"/></linearGradient></defs>
      <g stroke="#2a3040" stroke-width="1"><line x1="42" y1="25" x2="605" y2="25"/><line x1="42" y1="70" x2="605" y2="70"/><line x1="42" y1="115" x2="605" y2="115"/><line x1="42" y1="160" x2="605" y2="160"/><line x1="42" y1="195" x2="605" y2="195"/></g>
      <g fill="#8f98ab" font-size="10"><text x="4" y="28">40k</text><text x="4" y="73">30k</text><text x="4" y="118">20k</text><text x="4" y="163">10k</text><text x="12" y="198">0</text><text x="43" y="215">Mon</text><text x="128" y="215">Tue</text><text x="213" y="215">Wed</text><text x="298" y="215">Thu</text><text x="383" y="215">Fri</text><text x="468" y="215">Sat</text><text x="553" y="215">Sun</text></g>
      <path d="M45 155 L130 128 L215 142 L300 82 L385 100 L470 49 L555 31 L555 195 L45 195 Z" fill="url(#area)"/>
      <polyline points="45,155 130,128 215,142 300,82 385,100 470,49 555,31" fill="none" stroke="#ff3b78" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
      <polyline points="45,178 130,166 215,171 300,145 385,152 470,127 555,118" fill="none" stroke="#26d9d0" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
      <g fill="#ff3b78"><circle cx="45" cy="155" r="4"/><circle cx="130" cy="128" r="4"/><circle cx="215" cy="142" r="4"/><circle cx="300" cy="82" r="4"/><circle cx="385" cy="100" r="4"/><circle cx="470" cy="49" r="4"/><circle cx="555" cy="31" r="4"/></g>
    </svg><div class="legend"><span><i class="dot" style="background:#ff3b78"></i>Video views</span><span><i class="dot" style="background:#26d9d0"></i>Likes</span></div>
  </article>
  <article class="card"><h3>Follower activity</h3><p class="desc">Best time to post · sample activity by hour</p>
    <div class="hours">
      <div class="hourcol"><div class="bar" style="height:27%"></div><span class="hourlabel">6 AM</span></div><div class="hourcol"><div class="bar" style="height:43%"></div><span class="hourlabel">9 AM</span></div><div class="hourcol"><div class="bar" style="height:36%"></div><span class="hourlabel">12 PM</span></div><div class="hourcol"><div class="bar" style="height:63%"></div><span class="hourlabel">3 PM</span></div><div class="hourcol"><div class="bar" style="height:78%"></div><span class="hourlabel">6 PM</span></div><div class="hourcol"><div class="bar" style="height:100%"></div><span class="hourlabel">9 PM</span></div><div class="hourcol"><div class="bar" style="height:59%"></div><span class="hourlabel">12 AM</span></div>
    </div>
    <div class="callout">✨ Sample insight: evening activity appears strongest. Replace this with the “Most active times” information from your TikTok analytics before relying on it.</div>
  </article>
</section>
<section class="bottom">
  <article class="card"><h3>Audience & engagement</h3><p class="desc">Useful creator health indicators</p>
    <div class="rowline"><span>Average views per video</span><strong id="avgViews">18.3K</strong></div>
    <div class="rowline"><span>Likes per view</span><strong>9.9%</strong></div>
    <div class="rowline"><span>Follower growth</span><strong id="growth2">+12.8%</strong></div>
    <div class="rowline"><span>Suggested posting window</span><span class="pill">6 PM – 9 PM*</span></div>
    <p class="desc" style="margin:12px 0 0">*Example only; check your own audience activity.</p>
  </article>
  <article class="card"><h3>Recent content snapshot</h3><p class="desc">Example video performance — replace with your posts</p>
    <div class="rowline"><span>Video 01 · latest post</span><span><strong>42.6K</strong> <span class="sub">views</span></span></div>
    <div class="rowline"><span>Video 02 · comedy clip</span><span><strong>28.1K</strong> <span class="sub">views</span></span></div>
    <div class="rowline"><span>Video 03 · trending sound</span><span><strong>16.7K</strong> <span class="sub">views</span></span></div>
    <div class="rowline"><span>Top-performing post</span><span class="pill">Video 01</span></div>
  </article>
</section>
<section id="settings" class="card hidden" style="margin-top:15px"><h3>Edit dashboard data</h3><p class="desc">Enter the real values from TikTok Analytics, then press Apply. This changes the displayed values in this page only.</p>
  <div class="settings">
    <div class="field"><label>Account display name</label><input class="editable" id="inName" value="Venom Editz"></div>
    <div class="field"><label>TikTok username</label><input class="editable" id="inHandle" value="@geniusfacts2"></div>
    <div class="field"><label>Total followers</label><input class="editable" id="inFollowers" type="number" value="8420"></div>
    <div class="field"><label>Total likes</label><input class="editable" id="inLikes" value="126.4K"></div>
    <div class="field"><label>Total video views</label><input class="editable" id="inViews" value="1.28M"></div>
    <div class="field"><label>Profile views</label><input class="editable" id="inProfile" value="34.8K"></div>
    <div class="field"><label>Follower growth (%)</label><input class="editable" id="inGrowth" value="12.8"></div>
    <div class="field"><label>Average views per video</label><input class="editable" id="inAvg" value="18.3K"></div>
  </div><button class="btn primary" style="margin-top:15px" onclick="applyData()">Apply changes</button>
</section>

<section class="social-section">
  <div style="display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap;margin:25px 0 12px">
    <h3 style="font-size:16px;margin:0">Your Social Media Links</h3>
    <span class="sub">Official profile shortcuts</span>
  </div>
  <div class="social-grid">
    <article class="social-card">
      <div class="social-icon" style="background:#252735;color:#fff">♪</div>
      <div class="social-meta"><strong>TikTok</strong><span>@geniusfacts2</span><a class="social-link" href="https://www.tiktok.com/@geniusfacts2" target="_blank" rel="noopener noreferrer">Open TikTok ↗</a></div>
    </article>
    <article class="social-card">
      <div class="social-icon" style="background:#ff2638;color:#fff">▶</div>
      <div class="social-meta"><strong>YouTube</strong><span>@factzilla1122-p9j</span><a class="social-link" href="https://youtube.com/@factzilla1122-p9j" target="_blank" rel="noopener noreferrer">Open YouTube ↗</a></div>
    </article>
    <article class="social-card">
      <div class="social-icon" style="background:linear-gradient(135deg,#ffb347,#ff3d81,#8b4dff);color:#fff">◎</div>
      <div class="social-meta"><strong>Instagram</strong><span>@venom.editz6</span><a class="social-link" href="https://www.instagram.com/venom.editz6/" target="_blank" rel="noopener noreferrer">Open Instagram ↗</a></div>
    </article>
    <article class="social-card">
      <div class="social-icon" style="background:#20c76a;color:#fff">☏</div>
      <div class="social-meta"><strong>WhatsApp</strong><span>Direct contact</span><a class="social-link" href="https://wa.me/923295721430" target="_blank" rel="noopener noreferrer">Message on WhatsApp ↗</a></div>
    </article>
  </div>
</section>

<footer class="foot">VENOM EDITZ · Creator Studio · Demo analytics are not connected to TikTok</footer>
</div>
<script>
function applyData(){
 const val=id=>document.getElementById(id).value.trim();
 document.getElementById('displayName').textContent=val('inName')||'Venom Editz';
 document.getElementById('handle').textContent=(val('inHandle')||'@geniusfacts2')+' · Creator overview';
 document.getElementById('followers').textContent=Number(val('inFollowers')||0).toLocaleString();
 document.getElementById('likes').textContent=val('inLikes')||'0';
 document.getElementById('views').textContent=val('inViews')||'0';
 document.getElementById('profileViews').textContent=val('inProfile')||'0';
 document.getElementById('growth').textContent=(val('inGrowth')||'0')+'%';
 document.getElementById('growth2').textContent='+'+(val('inGrowth')||'0')+'%';
 document.getElementById('avgViews').textContent=val('inAvg')||'0';
}
</script>
</body>
</html>
