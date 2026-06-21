<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Press-Sport-Lens | Media &amp; Photography Analysis</title>
<script src="https://cdn.plot.ly/plotly-2.32.0.min.js"></script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --gold:#946E1C;--navy:#263D69;--blue:#1C4694;--brown:#614E26;
  --cream:#FFEEC9;--light:#F8F3E8;--white:#FFFFFF;
  --text:#1A2540;--muted:#6B7280;--border:#E5D9BE;
  --shadow:0 4px 24px rgba(38,61,105,.10);--radius:16px;
}
html{scroll-behavior:smooth}
body{font-family:'Inter',sans-serif;background:var(--light);color:var(--text);line-height:1.6}

header{background:linear-gradient(135deg,var(--navy) 0%,var(--blue) 60%,var(--gold) 100%);color:var(--white);position:relative;overflow:hidden}
.hdr{max-width:1280px;margin:0 auto;padding:56px 32px 48px;display:flex;align-items:center;gap:40px;position:relative;z-index:2}
.hdr-lens{flex-shrink:0;width:96px;height:96px;border-radius:50%;background:rgba(255, 136, 0, 0.12);border:3px solid rgba(255,238,201,.5);display:flex;align-items:center;justify-content:center;font-size:44px}
.hdr-text h1{font-family:'Playfair Display',serif;font-size:clamp(2rem,5vw,3.5rem);font-weight:900;letter-spacing:-.5px;line-height:1.1;color:var(--cream)}
.hdr-sub{font-size:1rem;color:rgba(255, 174, 0, 0.85);margin-top:8px}
.hdr-badge{margin-top:16px;display:inline-flex;align-items:center;gap:8px;background:rgba(255,238,201,.15);border:1px solid rgba(255,238,201,.3);border-radius:100px;padding:6px 16px;font-size:.8rem;font-weight:600;color:var(--cream)}
.hdr-circle{position:absolute;top:-80px;right:-80px;width:400px;height:400px;border-radius:50%;background:rgba(255,255,255,.04);z-index:1}
.hdr-circle::after{content:'';position:absolute;top:80px;right:80px;width:220px;height:220px;border-radius:50%;background:rgba(255,255,255,.06)}

nav{background:var(--white);border-bottom:2px solid var(--border);position:sticky;top:0;z-index:100;box-shadow:0 2px 12px rgba(38,61,105,.08)}
.nav-inner{max-width:1680px;margin:0 auto;padding:0 32px;display:flex;gap:4px;overflow-x:auto;scrollbar-width:none}
.nav-inner::-webkit-scrollbar{display:none}
.nav-tab{padding:16px 20px;font-size:.85rem;font-weight:600;color:var(--muted);text-decoration:none;border-bottom:3px solid transparent;white-space:nowrap;transition:color .2s,border-color .2s;cursor:pointer;background:none;border-top:none;border-left:none;border-right:none;font-family:inherit}
.nav-tab:hover{color:var(--blue)}
.nav-tab.active{color:var(--blue);border-bottom-color:var(--gold)}

main{max-width:1680px;margin:0 auto;padding:40px 24px 80px}
.section{display:none}
.section.active{display:block}

.kpi-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:10px;margin-bottom:28px}
.kpi-card{background:var(--white);border-radius:var(--radius);padding:28px 24px;box-shadow:var(--shadow);border-left:5px solid var(--gold);transition:transform .2s,box-shadow .2s}
.kpi-card:hover{transform:translateY(-3px);box-shadow:0 8px 32px rgba(38,61,105,.14)}
.kpi-card:nth-child(2){border-left-color:var(--blue)}
.kpi-card:nth-child(3){border-left-color:var(--navy)}
.kpi-card:nth-child(4){border-left-color:var(--brown)}
.kpi-icon{font-size:28px;margin-bottom:12px;display:block}
.kpi-value{font-family:'Playfair Display',serif;font-size:2rem;font-weight:700;color:var(--navy);line-height:1}
.kpi-label{font-size:.82rem;font-weight:600;color:var(--muted);text-transform:uppercase;letter-spacing:.6px;margin-top:6px}

.sec-hdr{display:flex;align-items:center;gap:14px;margin-bottom:28px;margin-top:48px}
.sec-hdr:first-child{margin-top:0}
.sec-num{width:40px;height:40px;border-radius:10px;background:linear-gradient(135deg,var(--blue),var(--navy));color:var(--white);font-weight:700;font-size:.9rem;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.sec-hdr h2{font-family:'Playfair Display',serif;font-size:1.4rem;color:var(--navy)}
.sec-hdr p{font-size:.85rem;color:var(--muted);margin-top:2px}

.chart-card{background:var(--white);border-radius:var(--radius);padding:28px 24px;box-shadow:var(--shadow);margin-bottom:28px;transition:box-shadow .2s}
.chart-card:hover{box-shadow:0 8px 36px rgba(38,61,105,.13)}
.chart-grid-2{display:grid;grid-template-columns:repeat(auto-fit,minmax(480px,1fr));gap:10px;margin-bottom:10px}
.chart-grid-2 .chart-card{margin-bottom:0}
.plotly-div{width:100%;min-height:380px}

.table-wrap{overflow-x:auto;border-radius:12px;box-shadow:var(--shadow);margin-bottom:28px}
table{width:100%;border-collapse:collapse;background:var(--white);font-size:.88rem}
thead tr{background:linear-gradient(90deg,var(--navy),var(--blue));color:var(--white)}
thead th{padding:14px 16px;font-weight:600;text-align:left;letter-spacing:.3px}
tbody tr{border-bottom:1px solid var(--border);transition:background .15s}
tbody tr:hover{background:var(--light)}
tbody tr:last-child{border-bottom:none}
tbody td{padding:12px 16px}
tbody td:first-child{font-weight:600;color:var(--navy)}

.ins-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:20px;margin-bottom:28px}
.ins-card{background:var(--white);border-radius:var(--radius);padding:24px;box-shadow:var(--shadow);border-top:4px solid var(--gold);transition:transform .2s}
.ins-card:hover{transform:translateY(-2px)}
.ins-card:nth-child(2){border-top-color:var(--blue)}
.ins-card:nth-child(3){border-top-color:var(--navy)}
.ins-card:nth-child(4){border-top-color:var(--brown)}
.ins-card:nth-child(5){border-top-color:var(--gold)}
.ins-card:nth-child(6){border-top-color:var(--blue)}
.ins-emoji{font-size:28px;margin-bottom:10px}
.ins-card h3{font-size:.95rem;font-weight:700;color:var(--navy);margin-bottom:8px}
.ins-card p{font-size:.85rem;color:var(--muted);line-height:1.6}
.hl{display:inline-block;background:var(--cream);color:var(--brown);font-weight:700;padding:2px 8px;border-radius:6px;font-size:.82rem}

footer{background:linear-gradient(135deg,var(--navy),var(--blue));color:rgba(255,238,201,.75);text-align:center;padding:40px 24px;font-size:.85rem}
footer .ft{font-family:'Playfair Display',serif;font-size:1.4rem;color:var(--cream);margin-bottom:8px}

@media(max-width:768px){
  .hdr{flex-direction:column;text-align:center;padding:40px 20px}
  .chart-grid-2{grid-template-columns:1fr}
  main{padding:24px 16px 60px}
  .kpi-grid{grid-template-columns:repeat(2,1fr)}
}
@media(max-width:480px){
  .kpi-grid{grid-template-columns:1fr}
  .kpi-value{font-size:1.6rem}
}
</style>
</head>
<body>

<header>
  <div class="hdr-circle"></div>
  <div class="hdr">
    <div class="hdr-lens">📸</div>
    <div class="hdr-text">
      <h1>Photography-Press عدسة الصحافة الفوتوغرافية</h1>
      <p class="hdr-sub">Introduction to coding for journalists AAUP - Done by: Balqees Arar</p>
      <span class="hdr-badge">📊 10 Creators &middot; Interactive Report &middot; June 2026</span>
    </div>
  </div>
</header>

<nav>
  <div class="nav-inner">
    <button class="nav-tab" onclick="showSection('about',this)">🎬 عن المشروع</button>
    <button class="nav-tab active" onclick="showSection('overview',this)">📋 Overview</button>
    <button class="nav-tab" onclick="showSection('experience',this)">📈 Experience</button>
    <button class="nav-tab" onclick="showSection('engagement',this)">💬 Engagement</button>
    <button class="nav-tab" onclick="showSection('cameras',this)">📷 Cameras</button>
    <button class="nav-tab" onclick="showSection('projects',this)">🎬 Projects</button>
    <button class="nav-tab" onclick="showSection('distribution',this)">📊 Distribution</button>
    <button class="nav-tab" onclick="showSection('stats',this)">🔢 Statistics</button>
    <button class="nav-tab" onclick="showSection('insights',this)">💡 Insights</button>
    <button class="nav-tab" onclick="showSection('data',this)">🗃️ Data</button>
  </div>
</nav>

<main>

<!-- OVERVIEW -->
<section id="overview" class="section active">
  <div class="sec-hdr" style="margin-top:0">
    <div class="sec-num">KPI</div>
    <div><h2>Key Performance Indicators</h2><p>Summary metrics across all 10 content creators</p></div>
  </div>
  <div class="kpi-grid">
    <div class="kpi-card"><span class="kpi-icon">👁️</span><div class="kpi-value">5.3M</div><div class="kpi-label">Total Monthly Views</div></div>
    <div class="kpi-card"><span class="kpi-icon">💬</span><div class="kpi-value">7.53%</div><div class="kpi-label">Avg Engagement Rate</div></div>
    <div class="kpi-card"><span class="kpi-icon">🏆</span><div class="kpi-value">8.1 yrs</div><div class="kpi-label">Avg Experience</div></div>
    <div class="kpi-card"><span class="kpi-icon">🎬</span><div class="kpi-value">948</div><div class="kpi-label">Total Projects Completed</div></div>
  </div>
  <div class="sec-hdr">
    <div class="sec-num">🏆</div>
    <div><h2>Top Performers</h2><p>Leading creators by engagement rate and monthly views</p></div>
  </div>
  <div class="chart-grid-2">
    <div class="chart-card"><div id="c_topEng" class="plotly-div"></div></div>
    <div class="chart-card"><div id="c_topViews" class="plotly-div"></div></div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience" class="section">
  <div class="sec-hdr" style="margin-top:0">
    <div class="sec-num">01</div>
    <div><h2>Experience vs Monthly Views</h2><p>Relationship between years of experience and monthly audience reach</p></div>
  </div>
  <div class="chart-card"><div id="c_expViews" class="plotly-div"></div></div>
  <div class="chart-card"><div id="c_engLine" class="plotly-div"></div></div>
</section>

<!-- ENGAGEMENT -->
<section id="engagement" class="section">
  <div class="sec-hdr" style="margin-top:0">
    <div class="sec-num">02</div>
    <div><h2>Content Type &amp; Engagement</h2><p>How different content categories compare by average engagement rate</p></div>
  </div>
  <div class="chart-card"><div id="c_contentEng" class="plotly-div"></div></div>
  <div class="chart-card"><div id="c_contentPie" class="plotly-div"></div></div>
  <div class="sec-hdr"><div class="sec-num">📋</div><div><h2>Engagement by Content Type</h2></div></div>
  <div class="table-wrap"><table>
    <thead><tr><th>Content Type</th><th>Avg Engagement Rate (%)</th></tr></thead>
    <tbody><tr><td>Sports Photography</td><td>9.55</td></tr><tr><td>Wedding Photography</td><td>8.35</td></tr><tr><td>Documentary</td><td>8.15</td></tr><tr><td>Street Photography</td><td>6.65</td></tr><tr><td>Press Photography</td><td>4.95</td></tr></tbody>
  </table></div>
  <div class="sec-hdr"><div class="sec-num">🏅</div><div><h2>Top 5 – Engagement Rate</h2></div></div>
  <div class="table-wrap"><table>
    <thead><tr><th>#</th><th>Creator</th><th>City</th><th>Content Type</th><th>Engagement Rate (%)</th></tr></thead>
    <tbody><tr><td>1</td><td>Rima Barakat</td><td>Hebron</td><td>Sports Photography</td><td>11.3</td></tr><tr><td>2</td><td>Sara Khalil</td><td>Jerusalem</td><td>Documentary</td><td>9.1</td></tr><tr><td>3</td><td>Nour Saleh</td><td>Bethlehem</td><td>Wedding Photography</td><td>8.6</td></tr><tr><td>4</td><td>Khalid Zubari</td><td>Nablus</td><td>Wedding Photography</td><td>8.1</td></tr><tr><td>5</td><td>Layla Hassan</td><td>Ramallah</td><td>Sports Photography</td><td>7.8</td></tr></tbody>
  </table></div>
</section>

<!-- CAMERAS -->
<section id="cameras" class="section">
  <div class="sec-hdr" style="margin-top:0">
    <div class="sec-num">03</div>
    <div><h2>Camera Brand Analysis</h2><p>Average monthly views by camera brand used</p></div>
  </div>
  <div class="chart-grid-2">
    <div class="chart-card"><div id="c_cameraViews" class="plotly-div"></div></div>
    <div class="chart-card"><div id="c_cameraPie" class="plotly-div"></div></div>
  </div>
  <div class="sec-hdr"><div class="sec-num">📋</div><div><h2>Camera Brand – Avg Views</h2></div></div>
  <div class="table-wrap"><table>
    <thead><tr><th>Camera Brand</th><th>Avg Monthly Views</th></tr></thead>
    <tbody><tr><td>Canon</td><td>805000</td></tr><tr><td>Sony</td><td>620000</td></tr><tr><td>Fujifilm</td><td>392500</td></tr><tr><td>Nikon</td><td>290000</td></tr></tbody>
  </table></div>
</section>

<!-- PROJECTS -->
<section id="projects" class="section">
  <div class="sec-hdr" style="margin-top:0">
    <div class="sec-num">06</div>
    <div><h2>Projects vs Monthly Views</h2><p>Does a higher project count translate to more monthly views?</p></div>
  </div>
  <div class="chart-card"><div id="c_projViews" class="plotly-div"></div></div>
  <div class="sec-hdr"><div class="sec-num">🏅</div><div><h2>Top 5 – Monthly Views</h2></div></div>
  <div class="table-wrap"><table>
    <thead><tr><th>#</th><th>Creator</th><th>City</th><th>Content Type</th><th>Monthly Views</th></tr></thead>
    <tbody><tr><td>1</td><td>Rima Barakat</td><td>Hebron</td><td>Sports Photography</td><td>1200000</td></tr><tr><td>2</td><td>Sara Khalil</td><td>Jerusalem</td><td>Documentary</td><td>810000</td></tr><tr><td>3</td><td>Faris Qasim</td><td>Tulkarm</td><td>Documentary</td><td>675000</td></tr><tr><td>4</td><td>Layla Hassan</td><td>Ramallah</td><td>Sports Photography</td><td>540000</td></tr><tr><td>5</td><td>Dina Awad</td><td>Ramallah</td><td>Street Photography</td><td>510000</td></tr></tbody>
  </table></div>
</section>

<!-- DISTRIBUTION -->
<section id="distribution" class="section">
  <div class="sec-hdr" style="margin-top:0">
    <div class="sec-num">📊</div>
    <div><h2>Distribution Analysis</h2><p>How monthly views are spread across creators</p></div>
  </div>
  <div class="chart-card"><div id="c_dist" class="plotly-div"></div></div>
</section>

<!-- STATS -->
<section id="stats" class="section">
  <div class="sec-hdr" style="margin-top:0">
    <div class="sec-num">07</div>
    <div><h2>Descriptive Statistics</h2><p>Summary statistics for all numerical columns</p></div>
  </div>
  <div class="table-wrap"><table>
    <thead><tr><th>Statistic</th><th>Age</th><th>MonthlyViews</th><th>ProjectCount</th><th>EngagementRate</th><th>ExperienceYears</th></tr></thead>
    <tbody><tr><td><strong>count</strong></td><td>10.0</td><td>10.0</td><td>10.0</td><td>10.0</td><td>10.0</td></tr><tr><td><strong>mean</strong></td><td>31.3</td><td>531000.0</td><td>94.8</td><td>7.53</td><td>8.1</td></tr><tr><td><strong>std</strong></td><td>5.21</td><td>300146.26</td><td>31.84</td><td>1.93</td><td>3.93</td></tr><tr><td><strong>min</strong></td><td>24.0</td><td>195000.0</td><td>45.0</td><td>4.7</td><td>3.0</td></tr><tr><td><strong>25%</strong></td><td>27.5</td><td>328750.0</td><td>75.0</td><td>6.52</td><td>5.25</td></tr><tr><td><strong>50%</strong></td><td>30.5</td><td>470000.0</td><td>93.5</td><td>7.5</td><td>7.5</td></tr><tr><td><strong>75%</strong></td><td>34.5</td><td>641250.0</td><td>109.75</td><td>8.48</td><td>10.5</td></tr><tr><td><strong>max</strong></td><td>40.0</td><td>1200000.0</td><td>156.0</td><td>11.3</td><td>15.0</td></tr></tbody>
  </table></div>
  <div class="sec-hdr"><div class="sec-num">📌</div><div><h2>Categorical Summary</h2></div></div>
  <div class="kpi-grid" style="grid-template-columns:repeat(auto-fit,minmax(260px,1fr))">
    <div class="kpi-card"><span class="kpi-icon">📹</span><div class="kpi-value" style="font-size:1.5rem">Documentary</div><div class="kpi-label">Most Common Content Type</div></div>
    <div class="kpi-card"><span class="kpi-icon">📷</span><div class="kpi-value" style="font-size:1.5rem">Canon</div><div class="kpi-label">Most Common Camera Brand</div></div>
  </div>
</section>

<!-- INSIGHTS -->
<section id="insights" class="section">
  <div class="sec-hdr" style="margin-top:0">
    <div class="sec-num">💡</div>
    <div><h2>Analytical Insights</h2><p>Key findings derived from the dataset</p></div>
  </div>
  <div class="ins-grid">
    <div class="ins-card"><div class="ins-emoji">📈</div><h3>Experience Paradox</h3><p>Less-experienced creators like <span class="hl">Rima Barakat (3 yrs)</span> can outperform veterans in views, suggesting that content type and audience engagement matter more than tenure alone.</p></div>
    <div class="ins-card"><div class="ins-emoji">🏆</div><h3>Sports Photography Leads</h3><p>Sports Photography achieves the highest average engagement rate at <span class="hl">9.55%</span>, driven by high-energy, shareable content that resonates strongly with online audiences.</p></div>
    <div class="ins-card"><div class="ins-emoji">📷</div><h3>Canon Dominates Reach</h3><p><span class="hl">Canon users</span> generate the highest average monthly views, likely reflecting brand preference among sports and high-production content creators in the dataset.</p></div>
    <div class="ins-card"><div class="ins-emoji">🔁</div><h3>Projects ≠ Views</h3><p>A higher project count does not guarantee higher monthly views. Creators with fewer, more focused projects — like Rima Barakat (45 projects, 1.2M views) — often reach larger audiences.</p></div>
    <div class="ins-card"><div class="ins-emoji">💬</div><h3>Engagement Beats Volume</h3><p>Press Photography creators average the most projects but lower engagement, indicating that quantity of output alone does not maximise audience interaction or loyalty.</p></div>
    <div class="ins-card"><div class="ins-emoji">🌍</div><h3>Geographic Diversity</h3><p>Creators span 7 cities across the West Bank, with <span class="hl">Ramallah</span> hosting the most creators. The region shows a vibrant, distributed media ecosystem.</p></div>
  </div>
</section>

<!-- DATA -->
<section id="data" class="section">
  <div class="sec-hdr" style="margin-top:0">
    <div class="sec-num">🗃️</div>
    <div><h2>Full Dataset</h2><p>Complete records for all 10 media creators and photographers</p></div>
  </div>
  <div class="table-wrap"><table>
    <thead><tr><th>ID</th><th>Creator</th><th>City</th><th>Content Type</th><th>Age</th><th>Monthly Views</th><th>Projects</th><th>Eng. Rate</th><th>Camera</th><th>Exp. Yrs</th></tr></thead>
    <tbody><tr><td>MC001</td><td>Layla Hassan</td><td>Ramallah</td><td>Sports Photography</td><td>29</td><td>540,000</td><td>87</td><td>7.8%</td><td>Canon</td><td>6</td></tr><tr><td>MC002</td><td>Omar Nassar</td><td>Nablus</td><td>Press Photography</td><td>35</td><td>320,000</td><td>124</td><td>5.2%</td><td>Nikon</td><td>11</td></tr><tr><td>MC003</td><td>Sara Khalil</td><td>Jerusalem</td><td>Documentary</td><td>27</td><td>810,000</td><td>63</td><td>9.1%</td><td>Sony</td><td>4</td></tr><tr><td>MC004</td><td>Youssef Amin</td><td>Gaza</td><td>Street Photography</td><td>31</td><td>275,000</td><td>98</td><td>6.4%</td><td>Fujifilm</td><td>8</td></tr><tr><td>MC005</td><td>Rima Barakat</td><td>Hebron</td><td>Sports Photography</td><td>24</td><td>1,200,000</td><td>45</td><td>11.3%</td><td>Canon</td><td>3</td></tr><tr><td>MC006</td><td>Tariq Mansour</td><td>Jenin</td><td>Press Photography</td><td>40</td><td>195,000</td><td>156</td><td>4.7%</td><td>Nikon</td><td>15</td></tr><tr><td>MC007</td><td>Nour Saleh</td><td>Bethlehem</td><td>Wedding Photography</td><td>33</td><td>430,000</td><td>112</td><td>8.6%</td><td>Sony</td><td>9</td></tr><tr><td>MC008</td><td>Faris Qasim</td><td>Tulkarm</td><td>Documentary</td><td>26</td><td>675,000</td><td>71</td><td>7.2%</td><td>Canon</td><td>5</td></tr><tr><td>MC009</td><td>Dina Awad</td><td>Ramallah</td><td>Street Photography</td><td>38</td><td>510,000</td><td>89</td><td>6.9%</td><td>Fujifilm</td><td>13</td></tr><tr><td>MC010</td><td>Khalid Zubari</td><td>Nablus</td><td>Wedding Photography</td><td>30</td><td>355,000</td><td>103</td><td>8.1%</td><td>Nikon</td><td>7</td></tr></tbody>
  </table></div>
</section>

<!-- ABOUT -->
<section id="about" class="section">
  <div class=WordSection1>

<p class=MsoNormal dir=RTL style='text-align:right;direction:rtl;unicode-bidi:
embed'><img width=313 height=209 src="image001.jpg" align=left
hspace=12><img width=921 height=297 src="image002.jpg" align=right
hspace=12>فكرة المشروع:<
<p class=MsoNormal dir=RTL style='text-align:justify;text-justify:kashida;
text-kashida:0%;direction:rtl;unicode-bidi:embed'>هذا المشروع عبارة عن تحليل بيانات لصناع المحتوى والمصورين باستخدام لغة Python يتضمن المشروع بيانات لعشرة مصورين تحتوي على معلومات مثل الاسم، العمر، المدينة</span><span dir=LTR></span><span
dir=LTR style='font-size:12.0pt;line-height:115%;font-family:"Mada Black"'><span
dir=LTR></span> </span><span lang=AR-SA style='font-size:12.0pt;
line-height:115%;font-family:"Mada Black"'>، نوع المحتوى، عدد المشاهدات الشهرية، عدد المشاريع المنجزة، معدل التفاعل، نوع الكاميرا المستخدمة، وسنوات الخبرة تم جمع هذه البيانات بهدف دراسة العوامل التي تؤثر في نجاح صناع المحتوى والمصورين وفهم العلاقة بين الخبرة والأداء الرقمي من خلال المشروع تم استخدام أدوات تحليل البيانات والرسوم البيانية لإجراء  </span><span dir=LTR></span><span lang=AR-SA dir=LTR style='font-size:
12.0pt;line-height:115%;font-family:"Mada Black"'><span dir=LTR></span> </span><span
lang=AR-SA style='font-size:12.0pt;line-height:115%;font-family:"Mada Black"'>مقارنات</span><span
dir=LTR></span><span lang=AR-SA dir=LTR style='font-size:16.0pt;line-height:
115%;font-family:"Mada Black"'><span dir=LTR></span> </span><span lang=AR-SA
style='font-size:12.0pt;line-height:115%;font-family:"Mada Black"'>بين صناع المحتوى والمصورين من حيث عدد المشاهدات ومعدل التفاعل وعدد المشاريع المنجزة. كما تم تحليل تأثير الخبرة ونوع المحتوى على مستوى الأداء، مما ساعد في استخراج نتائج واستنتاجات توضح أهم العوامل المرتبطة بالنجاح في مجال الإعلام الرقمي والتصوير.</span><span
dir=LTR></span><span dir=LTR style='font-size:12.0pt;line-height:115%;
font-family:"Mada Black"'><span dir=LTR></span></span></p>

<p class=MsoNormal dir=RTL style='text-align:right;direction:rtl;unicode-bidi:
embed'><span dir=LTR>&nbsp;</span></p>

</div>
</section>

</main>

<footer>
  <div class="ft">Photography-Lens مشروع عدسة الصحافة الفوتوغرافية</div>
  <p>Introduction to coding for journalists AAUP - Instructor: Amjad Khalil</p>
  <p style="margin-top:8px;font-size:1rem;opacity:.7">Arab American University · Ramallah Campus · Faculty of Modern Media</p>
</footer>

<script>
const CHARTS = {"expViews": {"data": [{"type": "scatter", "mode": "markers+text", "name": "Sports Photography", "x": [6, 3], "y": [540000, 1200000], "text": ["Layla Hassan", "Rima Barakat"], "textposition": "top center", "textfont": {"size": 10}, "marker": {"size": 14, "color": "#1C4694", "line": {"width": 2, "color": "white"}}}, {"type": "scatter", "mode": "markers+text", "name": "Press Photography", "x": [11, 15], "y": [320000, 195000], "text": ["Omar Nassar", "Tariq Mansour"], "textposition": "top center", "textfont": {"size": 10}, "marker": {"size": 14, "color": "#946E1C", "line": {"width": 2, "color": "white"}}}, {"type": "scatter", "mode": "markers+text", "name": "Documentary", "x": [4, 5], "y": [810000, 675000], "text": ["Sara Khalil", "Faris Qasim"], "textposition": "top center", "textfont": {"size": 10}, "marker": {"size": 14, "color": "#263D69", "line": {"width": 2, "color": "white"}}}, {"type": "scatter", "mode": "markers+text", "name": "Street Photography", "x": [8, 13], "y": [275000, 510000], "text": ["Youssef Amin", "Dina Awad"], "textposition": "top center", "textfont": {"size": 10}, "marker": {"size": 14, "color": "#614E26", "line": {"width": 2, "color": "white"}}}, {"type": "scatter", "mode": "markers+text", "name": "Wedding Photography", "x": [9, 7], "y": [430000, 355000], "text": ["Nour Saleh", "Khalid Zubari"], "textposition": "top center", "textfont": {"size": 10}, "marker": {"size": 14, "color": "#4A7BC4", "line": {"width": 2, "color": "white"}}}, {"type": "scatter", "mode": "lines", "name": "Trend", "x": [3, 4, 5, 6, 7, 8, 9, 11, 13, 15], "y": [822019.4384449238, 764956.8034557229, 707894.168466522, 650831.5334773212, 593768.8984881202, 536706.2634989193, 479643.6285097185, 365518.35853131674, 251393.08855291503, 137267.8185745132], "line": {"color": "#946E1C", "width": 2, "dash": "dash"}}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Experience Years vs Monthly Views", "font": {"size": 16}}, "xaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Experience (Years)"}, "yaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Monthly Views"}}}, "contentEng": {"data": [{"type": "bar", "orientation": "h", "x": [4.95, 6.65, 8.15, 8.35, 9.55], "y": ["Press Photography", "Street Photography", "Documentary", "Wedding Photography", "Sports Photography"], "marker": {"color": ["#1C4694", "#946E1C", "#263D69", "#614E26", "#4A7BC4"]}, "text": ["4.95%", "6.65%", "8.15%", "8.35%", "9.55%"], "textposition": "outside"}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Avg Engagement Rate by Content Type", "font": {"size": 16}}, "xaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Avg Engagement Rate (%)"}, "yaxis": {"automargin": true}}}, "cameraViews": {"data": [{"type": "bar", "x": ["Canon", "Sony", "Fujifilm", "Nikon"], "y": [805000, 620000, 392500, 290000], "marker": {"color": ["#1C4694", "#946E1C", "#263D69", "#614E26"]}, "text": ["805K", "620K", "392K", "290K"], "textposition": "outside"}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Avg Monthly Views by Camera Brand", "font": {"size": 16}}, "xaxis": {"title": "Camera Brand"}, "yaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Avg Monthly Views"}}}, "topEng": {"data": [{"type": "bar", "orientation": "h", "x": [7.8, 8.1, 8.6, 9.1, 11.3], "y": ["Layla Hassan", "Khalid Zubari", "Nour Saleh", "Sara Khalil", "Rima Barakat"], "marker": {"color": ["#1C4694", "#946E1C", "#263D69", "#614E26", "#4A7BC4"]}, "text": ["7.8%", "8.1%", "8.6%", "9.1%", "11.3%"], "textposition": "outside"}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Top 5 Creators \u2013 Engagement Rate", "font": {"size": 16}}, "xaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Engagement Rate (%)"}, "yaxis": {"automargin": true}}}, "topViews": {"data": [{"type": "bar", "orientation": "h", "x": [510000, 540000, 675000, 810000, 1200000], "y": ["Dina Awad", "Layla Hassan", "Faris Qasim", "Sara Khalil", "Rima Barakat"], "marker": {"color": ["#1C4694", "#946E1C", "#263D69", "#614E26", "#4A7BC4"]}, "text": ["510K", "540K", "675K", "810K", "1200K"], "textposition": "outside"}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Top 5 Creators \u2013 Monthly Views", "font": {"size": 16}}, "xaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Monthly Views"}, "yaxis": {"automargin": true}}}, "projViews": {"data": [{"type": "scatter", "mode": "markers+text", "name": "Canon", "x": [87, 45, 71], "y": [540000, 1200000, 675000], "text": ["Layla Hassan", "Rima Barakat", "Faris Qasim"], "textposition": "top center", "textfont": {"size": 10}, "marker": {"size": 14, "color": "#1C4694", "line": {"width": 2, "color": "white"}}}, {"type": "scatter", "mode": "markers+text", "name": "Nikon", "x": [124, 156, 103], "y": [320000, 195000, 355000], "text": ["Omar Nassar", "Tariq Mansour", "Khalid Zubari"], "textposition": "top center", "textfont": {"size": 10}, "marker": {"size": 14, "color": "#946E1C", "line": {"width": 2, "color": "white"}}}, {"type": "scatter", "mode": "markers+text", "name": "Sony", "x": [63, 112], "y": [810000, 430000], "text": ["Sara Khalil", "Nour Saleh"], "textposition": "top center", "textfont": {"size": 10}, "marker": {"size": 14, "color": "#263D69", "line": {"width": 2, "color": "white"}}}, {"type": "scatter", "mode": "markers+text", "name": "Fujifilm", "x": [98, 89], "y": [275000, 510000], "text": ["Youssef Amin", "Dina Awad"], "textposition": "top center", "textfont": {"size": 10}, "marker": {"size": 14, "color": "#614E26", "line": {"width": 2, "color": "white"}}}, {"type": "scatter", "mode": "lines", "name": "Trend", "x": [45, 63, 71, 87, 89, 98, 103, 112, 124, 156], "y": [947408.2598974094, 796899.2502959361, 730006.3571397258, 596220.5708273052, 579497.3475382527, 504242.84273751604, 462434.7845148846, 387180.279714148, 286840.9399798326, 19269.36735499138], "line": {"color": "#946E1C", "width": 2, "dash": "dash"}}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Project Count vs Monthly Views", "font": {"size": 16}}, "xaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Projects Completed"}, "yaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Monthly Views"}}}, "dist": {"data": [{"type": "histogram", "x": [540000, 320000, 810000, 275000, 1200000, 195000, 430000, 675000, 510000, 355000], "nbinsx": 6, "marker": {"color": "#1C4694", "opacity": 0.85, "line": {"width": 1, "color": "white"}}}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Monthly Views Distribution", "font": {"size": 16}}, "xaxis": {"title": "Monthly Views"}, "yaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Count", "dtick": 1}}}, "contentPie": {"data": [{"type": "pie", "labels": ["Sports Photography", "Press Photography", "Documentary", "Street Photography", "Wedding Photography"], "values": [2, 2, 2, 2, 2], "hole": 0.4, "marker": {"colors": ["#1C4694", "#946E1C", "#263D69", "#614E26", "#4A7BC4"], "line": {"color": "white", "width": 2}}, "textinfo": "label+percent"}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Content Type Distribution", "font": {"size": 16}}}}, "cameraPie": {"data": [{"type": "pie", "labels": ["Canon", "Nikon", "Sony", "Fujifilm"], "values": [3, 3, 2, 2], "hole": 0.4, "marker": {"colors": ["#1C4694", "#946E1C", "#263D69", "#614E26"], "line": {"color": "white", "width": 2}}, "textinfo": "label+percent"}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Camera Brand Distribution", "font": {"size": 16}}}}, "engLine": {"data": [{"type": "scatter", "mode": "lines+markers+text", "x": ["Rima Barakat", "Sara Khalil", "Faris Qasim", "Layla Hassan", "Khalid Zubari", "Youssef Amin", "Nour Saleh", "Omar Nassar", "Dina Awad", "Tariq Mansour"], "y": [11.3, 9.1, 7.2, 7.8, 8.1, 6.4, 8.6, 5.2, 6.9, 4.7], "line": {"color": "#946E1C", "width": 3}, "marker": {"size": 10, "color": "#1C4694", "line": {"width": 2, "color": "#946E1C"}}, "text": ["11.3%", "9.1%", "7.2%", "7.8%", "8.1%", "6.4%", "8.6%", "5.2%", "6.9%", "4.7%"], "textposition": "top center", "textfont": {"size": 9}, "fill": "tozeroy", "fillcolor": "rgba(148,110,28,0.08)"}], "layout": {"font": {"family": "Inter, sans-serif", "color": "#263D69"}, "paper_bgcolor": "rgba(0,0,0,0)", "plot_bgcolor": "rgba(0,0,0,0)", "margin": {"l": 40, "r": 30, "t": 60, "b": 60}, "legend": {"bgcolor": "rgba(0,0,0,0)"}, "title": {"text": "Engagement Rate per Creator (sorted by Experience)", "font": {"size": 16}}, "xaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Creator", "tickangle": -30}, "yaxis": {"gridcolor": "#EDE8DC", "showline": true, "linecolor": "#CCBF99", "zeroline": false, "title": "Engagement Rate (%)"}}}};
const CFG = {responsive:true};

function renderAll() {
  Plotly.newPlot('c_topEng',    CHARTS.topEng.data,    CHARTS.topEng.layout,    CFG);
  Plotly.newPlot('c_topViews',  CHARTS.topViews.data,  CHARTS.topViews.layout,  CFG);
  Plotly.newPlot('c_expViews',  CHARTS.expViews.data,  CHARTS.expViews.layout,  CFG);
  Plotly.newPlot('c_engLine',   CHARTS.engLine.data,   CHARTS.engLine.layout,   CFG);
  Plotly.newPlot('c_contentEng',CHARTS.contentEng.data,CHARTS.contentEng.layout,CFG);
  Plotly.newPlot('c_contentPie',CHARTS.contentPie.data,CHARTS.contentPie.layout,CFG);
  Plotly.newPlot('c_cameraViews',CHARTS.cameraViews.data,CHARTS.cameraViews.layout,CFG);
  Plotly.newPlot('c_cameraPie', CHARTS.cameraPie.data, CHARTS.cameraPie.layout, CFG);
  Plotly.newPlot('c_projViews', CHARTS.projViews.data, CHARTS.projViews.layout, CFG);
  Plotly.newPlot('c_dist',      CHARTS.dist.data,      CHARTS.dist.layout,      CFG);
}

function showSection(id, btn) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  if(btn) btn.classList.add('active');
  window.scrollTo({top:0,behavior:'smooth'});
  setTimeout(() => window.dispatchEvent(new Event('resize')), 80);
}

window.addEventListener('load', renderAll);
</script>
</body>
</html>
