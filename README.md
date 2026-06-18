<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>UNITAG CLEARANCE FESTIVAL - Strategic Foundation</title>
<style>
  :root{
    --bg: #0a0c10;
    --bg-panel: #11141a;
    --bg-card: #161a22;
    --bg-card-hover: #1c212b;
    --border: #232834;
    --border-soft: #1b1f29;
    --accent: #5b6ae3;
    --accent-soft: rgba(28,90,183,0.12);
    --accent-2: #ffb238;
    --accent-3: #36c5ff;
    --text: #eef0f4;
    --text-dim: #a7adba;
    --text-faint: #6b7180;
    --green: #3ddc97;
    --red: #ff5d6c;
    --radius: 14px;
    --serif: 'Georgia', 'Iowan Old Style', serif;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  body{
    background: var(--bg);
    color: var(--text);
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    line-height:1.6;
    font-size:15px;
  }
  body::before{
    content:"";
    position:fixed; inset:0;
    background:
      radial-gradient(circle at 15% 0%, rgba(255,90,54,0.08), transparent 45%),
      radial-gradient(circle at 85% 15%, rgba(54,197,255,0.06), transparent 40%);
    pointer-events:none;
    z-index:0;
  }

  /* ===== Sidebar ===== */
  .sidebar{
    position:fixed; top:0; left:0; bottom:0; width:280px;
    background: var(--bg-panel);
    border-right:1px solid var(--border);
    padding:28px 18px;
    overflow-y:auto;
    z-index:50;
  }
  .brand{
    display:flex; align-items:center; gap:10px;
    padding:0 10px 22px 10px;
    border-bottom:1px solid var(--border-soft);
    margin-bottom:18px;
  }
  .brand-mark{
    width:34px;height:34px;border-radius:9px;
    display:flex;align-items:center;justify-content:center;
    font-weight:800; font-size:14px; color:#10120f; flex-shrink:0;
  }
  .brand-text .t1{font-size:13px; font-weight:700; letter-spacing:0.5px; color:var(--text);}
  .brand-text .t2{font-size:10.5px; color:var(--text-faint); text-transform:uppercase; letter-spacing:0.8px;}

  .nav-group{margin-bottom:6px;}
  .nav-label{
    font-size:10.5px; text-transform:uppercase; letter-spacing:1.2px;
    color:var(--text-faint); padding:14px 10px 8px 10px; font-weight:700;
  }
  .nav-link{
    display:flex; align-items:center; gap:10px;
    padding:9px 10px; border-radius:9px;
    color:var(--text-dim); text-decoration:none; font-size:13.5px;
    cursor:pointer; transition: all .15s ease;
    border:1px solid transparent;
  }
  .nav-link:hover{ background:var(--bg-card); color:var(--text); }
  .nav-link.active{ background:var(--accent-soft); color:var(--accent); border-color:rgba(255,90,54,0.25); font-weight:600; }
  .nav-num{
    width:20px;height:20px;border-radius:6px;
    background:var(--bg-card); display:flex;align-items:center;justify-content:center;
    font-size:10.5px; font-weight:700; color:var(--text-faint); flex-shrink:0;
  }
  .nav-link.active .nav-num{ background:var(--accent); color:#1a0a05; }

  .sidebar-footer{
    margin-top:22px; padding:14px 12px; border-radius:10px;
    background:var(--bg-card); border:1px solid var(--border-soft);
    font-size:11.5px; color:var(--text-faint); line-height:1.5;
  }
  .sidebar-footer b{color:var(--text-dim);}

  /* ===== Main ===== */
  .main{ margin-left:280px; position:relative; z-index:1; }
  .container{ max-width:1080px; margin:0 auto; padding:48px 56px 100px; }

  .hero{
    padding:38px 0 30px;
    border-bottom:1px solid var(--border-soft);
    margin-bottom:40px;
  }
  .hero-tag{
    display:inline-block; padding:5px 12px; border-radius:20px;
    background:var(--accent-soft); color:var(--accent);
    font-size:11px; font-weight:700; letter-spacing:1px; text-transform:uppercase;
    margin-bottom:18px; border:1px solid rgba(255,90,54,0.25);
  }
  .hero h1{
    font-size:40px; font-weight:800; letter-spacing:-1px; line-height:1.15;
    margin-bottom:12px;
  }
  .hero h1 span{color:var(--accent);}
  .hero-sub{ font-size:16px; color:var(--text-dim); max-width:680px; margin-bottom:20px;}
  .hero-meta{ display:flex; gap:28px; flex-wrap:wrap; }
  .hero-meta-item{ font-size:12px; color:var(--text-faint); }
  .hero-meta-item b{ color:var(--text); display:block; font-size:14px; margin-bottom:2px; }

  section{ margin-bottom:64px; scroll-margin-top:30px; }
  .sec-head{ margin-bottom:28px; }
  .sec-eyebrow{
    font-size:11.5px; color:var(--accent); font-weight:700; letter-spacing:1.5px;
    text-transform:uppercase; margin-bottom:10px; display:flex; align-items:center; gap:10px;
  }
  .sec-eyebrow::before{
    content:""; width:24px; height:2px; background:var(--accent); display:inline-block;
  }
  .sec-head h2{ font-size:28px; font-weight:800; letter-spacing:-0.5px; margin-bottom:8px;}
  .sec-head p.lede{ font-size:15px; color:var(--text-dim); max-width:760px; }

  h3.sub{ font-size:18px; font-weight:700; margin:30px 0 14px; color:var(--text); display:flex; align-items:center; gap:8px;}
  h3.sub .dot{ width:7px;height:7px;border-radius:50%; background:var(--accent); display:inline-block;}
  h4.minor{ font-size:14px; font-weight:700; margin:18px 0 8px; color:var(--accent-2); text-transform:uppercase; letter-spacing:0.5px;}

  p{ color:var(--text-dim); margin-bottom:12px; }
  strong{ color:var(--text); font-weight:700; }

  .card{
    background:var(--bg-card); border:1px solid var(--border);
    border-radius:var(--radius); padding:22px 24px; margin-bottom:16px;
  }
  .card-title{ font-size:14px; font-weight:700; color:var(--text); margin-bottom:8px; display:flex; align-items:center; gap:8px;}

  .grid-2{ display:grid; grid-template-columns:1fr 1fr; gap:18px; }
  .grid-3{ display:grid; grid-template-columns:1fr 1fr 1fr; gap:16px; }
  .grid-4{ display:grid; grid-template-columns:repeat(4,1fr); gap:14px; }
  @media(max-width:900px){ .grid-2,.grid-3,.grid-4{grid-template-columns:1fr;} }

  .stat-card{
    background:var(--bg-card); border:1px solid var(--border); border-radius:12px;
    padding:18px 20px;
  }
  .stat-card .num{ font-size:26px; font-weight:800; color:var(--accent); margin-bottom:4px;}
  .stat-card .label{ font-size:12px; color:var(--text-faint); text-transform:uppercase; letter-spacing:0.5px;}

  table{ width:100%; border-collapse:collapse; margin:16px 0; font-size:13.5px; }
  thead th{
    background:var(--bg-card); color:var(--text-faint); text-transform:uppercase;
    font-size:10.5px; letter-spacing:0.8px; font-weight:700;
    padding:11px 14px; text-align:left; border-bottom:1px solid var(--border);
  }
  tbody td{ padding:11px 14px; border-bottom:1px solid var(--border-soft); color:var(--text-dim); vertical-align:top;}
  tbody tr:hover{ background:rgba(255,255,255,0.015); }
  tbody td b, tbody td strong{ color:var(--text); }
  tbody tr:last-child td{ border-bottom:none; }

  .pill{
    display:inline-block; padding:3px 10px; border-radius:20px;
    font-size:11px; font-weight:700; letter-spacing:0.3px;
  }
  .pill-orange{ background:var(--accent-soft); color:var(--accent); }
  .pill-blue{ background:rgba(54,197,255,0.12); color:var(--accent-3); }
  .pill-green{ background:rgba(61,220,151,0.12); color:var(--green); }
  .pill-yellow{ background:rgba(255,178,56,0.12); color:var(--accent-2); }
  .pill-red{ background:rgba(255,93,108,0.12); color:var(--red); }

  blockquote.insight{
    border-left:3px solid var(--accent); background:var(--bg-card);
    padding:18px 22px; border-radius:0 12px 12px 0; margin:18px 0;
    font-family:var(--serif); font-style:italic; font-size:17px; color:var(--text);
    line-height:1.55;
  }
  blockquote.insight cite{
    display:block; margin-top:10px; font-style:normal; font-family:inherit;
    font-size:11.5px; color:var(--text-faint); text-transform:uppercase; letter-spacing:0.5px;
  }

  ul.clean, ol.clean{ margin:10px 0 10px 0; padding-left:0; list-style:none; }
  ul.clean li, ol.clean li{
    position:relative; padding-left:22px; margin-bottom:9px; color:var(--text-dim);
  }
  ul.clean li::before{
    content:"›"; position:absolute; left:0; color:var(--accent); font-weight:800; font-size:15px;
  }
  ol.clean{ counter-reset:item; }
  ol.clean li{ counter-increment:item; }
  ol.clean li::before{
    content:counter(item); position:absolute; left:0; color:var(--accent); font-weight:800; font-size:12px;
    width:16px; height:16px; background:var(--accent-soft); border-radius:4px; display:flex; align-items:center; justify-content:center; top:1px;
  }

  /* Diagram blocks (architecture / hierarchy) */
  .diagram{
    background:var(--bg-card); border:1px solid var(--border); border-radius:var(--radius);
    padding:30px; margin:18px 0;
  }
  .tier{ display:flex; justify-content:center; margin-bottom:14px; }
  .node{
    border-radius:10px; padding:14px 20px; text-align:center; font-size:13px; font-weight:700;
    border:1px solid var(--border); min-width:170px;
  }
  .node-master{
    background:linear-gradient(135deg, var(--accent), #ff8a5a); color:#1a0a05;
    font-size:15px; padding:16px 28px; min-width:300px; box-shadow:0 8px 24px rgba(255,90,54,0.25);
  }
  .node-sub{ background:var(--bg-card-hover); color:var(--text); }
  .node-sub .sub-label{ display:block; font-size:9.5px; color:var(--accent-2); text-transform:uppercase; letter-spacing:0.5px; margin-bottom:3px; font-weight:700;}
  .connector{ width:1px; height:22px; background:var(--border); margin:0 auto; position:relative; }
  .connector::after{
    content:""; position:absolute; bottom:-1px; left:50%; transform:translateX(-50%);
    border:5px solid transparent; border-top-color:var(--border);
  }
  .row{ display:flex; gap:14px; justify-content:center; flex-wrap:wrap; }
  .tree-row{ position:relative; display:flex; justify-content:center; gap:18px; flex-wrap:wrap; padding-top:22px; }
  .tree-row::before{
    content:""; position:absolute; top:0; left:50%; width:80%; height:1px;
    background:var(--border); transform:translateX(-50%);
  }
  .tree-row .node{ position:relative; }
  .tree-row .node::before{
    content:""; position:absolute; top:-22px; left:50%; width:1px; height:22px;
    background:var(--border); transform:translateX(-50%);
  }

  /* Timeline / roadmap */
  .phase-block{
    border:1px solid var(--border); border-radius:var(--radius); margin-bottom:22px; overflow:hidden;
  }
  .phase-head{
    display:flex; align-items:center; justify-content:space-between;
    padding:18px 24px; background:var(--bg-card-hover); border-bottom:1px solid var(--border);
  }
  .phase-head-left{ display:flex; align-items:center; gap:14px; }
  .phase-num{
    width:42px; height:42px; border-radius:10px; display:flex; align-items:center; justify-content:center;
    font-weight:800; font-size:17px; flex-shrink:0;
  }
  .phase-title{ font-size:17px; font-weight:800; }
  .phase-days{ font-size:11.5px; color:var(--text-faint); margin-top:2px; }
  .phase-body{ padding:24px; background:var(--bg-card); }
  .phase-1 .phase-num{ background:rgba(54,197,255,0.15); color:var(--accent-3); }
  .phase-2 .phase-num{ background:rgba(255,90,54,0.15); color:var(--accent); }
  .phase-3 .phase-num{ background:rgba(255,178,56,0.15); color:var(--accent-2); }
  .phase-4 .phase-num{ background:rgba(255,93,108,0.15); color:var(--red); }

  .kpi-strip{ display:flex; gap:10px; flex-wrap:wrap; margin-top:14px; }
  .kpi-chip{
    background:var(--bg); border:1px solid var(--border); border-radius:8px;
    padding:8px 14px; font-size:12px; color:var(--text-dim);
  }
  .kpi-chip b{ color:var(--accent-2); }

  /* timeline bar at a glance */
  .timeline-bar{ display:flex; width:100%; border-radius:10px; overflow:hidden; margin:20px 0; border:1px solid var(--border);}
  .timeline-seg{ padding:16px 10px; text-align:center; font-size:12px; font-weight:700; color:#10120f; flex:1; position:relative;}
  .timeline-seg .days{ display:block; font-size:10px; font-weight:600; opacity:0.75; margin-top:2px;}
  .seg-1{ background:var(--accent-3); flex:0.8;}
  .seg-2{ background:var(--accent); flex:1;}
  .seg-3{ background:var(--accent-2); flex:1.2;}
  .seg-4{ background:var(--red); flex:0.8;}

  .callout{
    display:flex; gap:14px; padding:16px 20px; border-radius:12px; margin:16px 0;
    border:1px solid var(--border); background:var(--bg-card);
  }
  .callout-icon{ font-size:20px; flex-shrink:0; }
  .callout.warn{ border-color:rgba(255,178,56,0.3); background:rgba(255,178,56,0.06); }
  .callout.info{ border-color:rgba(54,197,255,0.3); background:rgba(54,197,255,0.06); }
  .callout.good{ border-color:rgba(61,220,151,0.3); background:rgba(61,220,151,0.06); }

  .divider{ height:1px; background:var(--border-soft); margin:36px 0; }

  .footer-nav{
    display:flex; justify-content:space-between; align-items:center;
    padding:24px 0; border-top:1px solid var(--border-soft); margin-top:20px;
  }
  .footer-nav a{
    color:var(--text-dim); text-decoration:none; font-size:13px; display:flex; align-items:center; gap:6px;
  }
  .footer-nav a:hover{ color:var(--accent); }

  ::-webkit-scrollbar{ width:9px; height:9px; }
  ::-webkit-scrollbar-track{ background:var(--bg); }
  ::-webkit-scrollbar-thumb{ background:#2a3040; border-radius:5px; }
  ::-webkit-scrollbar-thumb:hover{ background:#363d4f; }

  @media(max-width:1000px){
    .sidebar{ display:none; }
    .main{ margin-left:0; }
    .container{ padding:30px 22px 80px; }
    .hero h1{ font-size:30px; }
  }
</style>
</head>
<body>

<nav class="sidebar">
  <div class="brand">
    <div class="brand-mark"><img class="logo" src="https://i.ibb.co.com/bZqYpgQ/pp-1.png" style="width:100%"></div>
    <div class="brand-text">
      <div class="t1">UNITAG</div>
      <div class="t2">Clearance Festival</div>
    </div>
  </div>

  <div class="nav-group">
    <div class="nav-label">Strategic Foundation</div>
    <a class="nav-link" data-target="sec-exec"><span class="nav-num">01</span> Executive Summary</a>
    <a class="nav-link" data-target="sec-concept"><span class="nav-num">02</span> Campaign Concept</a>
    <a class="nav-link" data-target="sec-architecture"><span class="nav-num">03</span> Campaign Architecture</a>
    <a class="nav-link" data-target="sec-roadmap"><span class="nav-num">04</span> 30-Day Roadmap</a>
    <a class="nav-link" data-target="sec-layout"><span class="nav-num">05</span> Store Layout</a>
    <a class="nav-link" data-target="sec-online"><span class="nav-num">06</span> Online Strategy</a>
    <a class="nav-link" data-target="sec-marketplace"><span class="nav-num">07</span> Marketplace Strategy</a>
  </div>
</nav>

<main class="main">
  <div class="container">

    <div class="hero">
      <span class="hero-tag">Strategic Foundation Document</span>
      <h1>UNITAG <span>CLEARANCE FESTIVAL</span></h1>
      <p class="hero-sub">Master campaign umbrella untuk seluruh tim - Marketing, Sales, Store Staff, Marketplace, dan Management - agar bergerak dengan satu fokus, satu pesan, satu timeline.</p>
      <div class="hero-meta">
        <div class="hero-meta-item"><b>"Original Accessories, Clearance Price"</b>Tagline Utama</div>
        <div class="hero-meta-item"><b>30 Hari</b>Durasi Kampanye</div>
        <div class="hero-meta-item"><b>4 Fase</b>Teasing → Launch → Scale → Last Chance</div>
        <div class="hero-meta-item"><b>Spigen · Aulumu · Sharge · Momax</b>Brand Portfolio</div>
      </div>
    </div>

    <!-- SECTION 1: EXECUTIVE SUMMARY -->
    <section id="sec-exec">
      <div class="sec-head">
        <div class="sec-eyebrow">Bagian 01</div>
        <h2>Executive Summary</h2>
        <p class="lede">Ringkasan strategis untuk Management: mengapa kampanye ini dibutuhkan sekarang, dampak bisnis dan marketing yang diharapkan, serta rasionalisasi mengapa pendekatan satu payung kampanye adalah keputusan yang tepat dibanding menjalankan promo per-brand secara terpisah.</p>
      </div>

      <h3 class="sub"><span class="dot"></span>Mengapa Kampanye Ini Dibutuhkan</h3>
      <p>UniTAG saat ini menghadapi tumpukan overstock di beberapa brand portfolio (Spigen, Aulumu, Sharge, Momax) yang menahan cash flow dan menyita ruang gudang serta display toko. Tanpa intervensi terstruktur, ada tiga risiko yang berjalan paralel: pertama, biaya penyimpanan dan opportunity cost dari modal yang terkunci di stok lama; kedua, tekanan untuk melakukan diskon parsial dan tidak terkoordinasi oleh masing-masing tim/cabang, yang justru merusak persepsi harga brand premium secara perlahan; ketiga, hilangnya momentum karena tidak ada satu narasi besar yang bisa digaungkan serempak di semua channel.</p>
      <p>Pendekatan "diskon diam-diam per SKU" adalah opsi paling berisiko bagi brand premium - pelanggan justru mengasosiasikan brand dengan murahan tanpa mendapat keuntungan urgency/FOMO yang biasanya menyertai clearance terstruktur. <strong>UNITAG CLEARANCE FESTIVAL dirancang sebagai satu peristiwa besar bertahun sekali</strong> - bukan diskon biasa - sehingga clearance terasa sebagai kesempatan emas yang sengaja diciptakan, bukan tanda kegagalan inventory.</p>

      <blockquote class="insight">
        Pelanggan tidak keberatan brand premium memberi harga clearance, yang mereka curigai adalah ketika diskon muncul tanpa alasan, tanpa batas waktu, dan tanpa peristiwa. Festival memberi diskon itu sebuah cerita.
      </blockquote>

      <h3 class="sub"><span class="dot"></span>Dampak Bisnis yang Diharapkan</h3>
      <div class="grid-4">
        <div class="stat-card"><div class="num">↓ Overstock</div><div class="label">Reduksi Inventory Lama</div></div>
        <div class="stat-card"><div class="num">↑ Cash Flow</div><div class="label">Perputaran Modal Lebih Cepat</div></div>
        <div class="stat-card"><div class="num">↑ AOV</div><div class="label">Melalui Bundling Terstruktur</div></div>
        <div class="stat-card"><div class="num">↑ New + Reaktivasi</div><div class="label">Akuisisi & Database Lama</div></div>
      </div>
      <p style="margin-top:14px;">Target angka spesifik (persentase reduksi stok, target omzet, target jumlah transaksi) akan ditetapkan bersama tim Finance & Inventory begitu data SKU dan jumlah unit overstock per brand tersedia - dashboard KPI di bagian akhir dokumen sudah disiapkan strukturnya agar angka tersebut bisa langsung diisi tanpa mengubah framework.</p>

      <h3 class="sub"><span class="dot"></span>Dampak Marketing yang Diharapkan</h3>
      <table>
        <thead><tr><th>Area</th><th>Dampak yang Diharapkan</th><th>Mekanisme</th></tr></thead>
        <tbody>
          <tr><td><b>Brand Awareness</b></td><td>UniTAG dikenal sebagai destinasi gadget accessories terpercaya, bukan sekadar reseller</td><td>Satu nama kampanye besar yang diulang di semua channel selama 30 hari</td></tr>
          <tr><td><b>Database CRM</b></td><td>Reaktivasi pelanggan lama + pertumbuhan database WhatsApp/member baru</td><td>Broadcast bertahap + insentif eksklusif untuk pelanggan terdaftar</td></tr>
          <tr><td><b>Traffic Online & Offline</b></td><td>Lonjakan kunjungan toko fisik dan trafik marketplace/website selama periode festival</td><td>FOMO dari urgency mechanics (flash sale, clearance hour, last chance)</td></tr>
          <tr><td><b>Engagement Sosial Media</b></td><td>Peningkatan interaksi organik di Instagram & TikTok dari konten festival</td><td>Konten berseri (teaser → reveal → urgency) yang membangun antisipasi</td></tr>
          <tr><td><b>Marketplace Ranking</b></td><td>Naiknya posisi listing di Shopee/Tokopedia/TikTok Shop dari lonjakan transaksi</td><td>Flash sale terkoordinasi + voucher + livestream selama periode festival</td></tr>
        </tbody>
      </table>

      <h3 class="sub"><span class="dot"></span>Rasionalisasi Strategis</h3>
      <p>Tiga prinsip yang mendasari seluruh keputusan dalam dokumen ini:</p>
      <ol class="clean">
        <li><strong>Clearance sebagai Peristiwa, Bukan Kegagalan.</strong> Framing komunikasi selalu memposisikan festival sebagai kesempatan tahunan yang dirancang untuk pelanggan ("kesempatan dapat barang original harga clearance"), bukan sebagai sinyal bahwa produk tidak terjual.</li>
        <li><strong>Satu Bahasa di Semua Titik Kontak.</strong> Dari banner toko hingga caption Instagram hingga script staff penjualan - semua menggunakan nama kampanye, tagline, dan visual identity yang sama, sehingga pelanggan mengenali festival ini di manapun mereka bertemu UniTAG.</li>
        <li><strong>Bertingkat, Bukan Serentak Habis.</strong> 30 hari dipecah menjadi 4 fase dengan eskalasi urgency yang terukur (Teasing → Launch → Scale → Last Chance), sehingga momentum dibangun bertahap dan tidak "habis energi" di minggu pertama.</li>
      </ol>

      <div class="callout info">
        <div class="callout-icon">💡</div>
        <div><strong>Catatan implementasi:</strong> Dokumen ini adalah fondasi strategis. Detail eksekusi per-channel (Instagram, TikTok, Shopee, WhatsApp, Meta Ads, Google Ads), daftar bundle, mekanik promo, POSM, dan playbook staff toko akan disusun sebagai dokumen lanjutan yang merujuk kembali ke Big Idea dan Roadmap di sini sebagai sumber kebenaran tunggal.</div>
      </div>
    </section>

    <!-- SECTION 2: CAMPAIGN CONCEPT -->
    <section id="sec-concept">
      <div class="sec-head">
        <div class="sec-eyebrow">Bagian 02</div>
        <h2>Campaign Concept</h2>
        <p class="lede">Fondasi kreatif yang menjadi rujukan seluruh komunikasi - dari Big Idea sampai naskah staff toko. Setiap konten yang dibuat tim manapun harus bisa ditarik garis lurus ke konsep ini.</p>
      </div>

      <h3 class="sub"><span class="dot"></span>Consumer Insight</h3>
      <blockquote class="insight">
        "Aku tahu barang original itu bagus, tapi harganya bikin aku mikir dua kali - akhirnya beli yang KW karena lebih masuk akal di kantong, walau aku tahu kualitasnya nggak akan sama."
        <cite>Insight Konsumen - Gadget User Usia 18–40</cite>
      </blockquote>
      <p>Target audiens UniTAG (pengguna Apple, Samsung, mobile gamer, profesional, mahasiswa) secara umum <strong>menginginkan kualitas original</strong> tapi sering terhambat oleh persepsi bahwa aksesoris premium "tidak sepadan" dibeli dengan harga normal untuk barang sekunder seperti case, charger, atau power bank - barang yang dianggap pelengkap, bukan kebutuhan utama. Inilah yang membuat banyak dari mereka akhirnya memilih produk KW meski tahu risikonya (cepat rusak, tidak melindungi gadget utama dengan baik, tidak ada garansi). Kesempatan untuk mendapatkan brand yang sama dengan harga jauh lebih masuk akal adalah pemicu psikologis yang sangat kuat - ini bukan sekadar "diskon", ini <strong>"izin" untuk akhirnya membeli yang original</strong>.</p>

      <h3 class="sub"><span class="dot"></span>Big Idea</h3>
      <div class="card" style="border-color:rgba(255,90,54,0.35); background:linear-gradient(135deg, rgba(255,90,54,0.08), rgba(255,178,56,0.04));">
        <div class="card-title" style="font-size:18px; color:var(--accent);">"Akhirnya, Saatnya Upgrade ke yang Asli."</div>
        <p style="margin:0;">UNITAG CLEARANCE FESTIVAL adalah momen di mana barrier harga yang selama ini menahan orang dari memilih aksesoris original - dihapus untuk sementara. Bukan festival "buang stok lama", tapi festival <strong>"kesempatan naik kelas"</strong> dari aksesoris abal-abal ke brand premium yang mereka sebenarnya inginkan.</p>
      </div>

      <h3 class="sub"><span class="dot"></span>Key Message</h3>
      <div class="grid-2">
        <div class="card">
          <div class="card-title">Tagline Utama</div>
          <p style="font-family:var(--serif); font-size:20px; color:var(--text); font-style:italic; margin:0;">"Original Accessories, Clearance Price"</p>
        </div>
        <div class="card">
          <div class="card-title">Pesan Alternatif</div>
          <p style="font-family:var(--serif); font-size:20px; color:var(--text); font-style:italic; margin:0;">"Premium Brands. Crazy Deals."</p>
        </div>
      </div>
      <p>Kedua pesan ini digunakan secara komplementer: tagline utama untuk konteks formal (banner toko, judul campaign, materi resmi), pesan alternatif untuk konteks yang lebih kasual dan energik (caption sosial media, hook video TikTok, headline iklan).</p>

      <h3 class="sub"><span class="dot"></span>Emotional Hook</h3>
      <table>
        <thead><tr><th>Emosi</th><th>Bagaimana Dipicu</th></tr></thead>
        <tbody>
          <tr><td><span class="pill pill-orange">FOMO</span></td><td>Stok terbatas + waktu terbatas yang dikomunikasikan jujur dan konsisten di semua channel - bukan FOMO palsu yang diulang tiap bulan.</td></tr>
          <tr><td><span class="pill pill-green">Validasi Diri</span></td><td>"Akhirnya aku bisa punya yang original" - rasa bangga memiliki brand premium tanpa rasa bersalah soal harga.</td></tr>
          <tr><td><span class="pill pill-blue">Smart Shopper Pride</span></td><td>Pelanggan merasa cerdas karena "tahu momennya" untuk belanja, bukan merasa dimanfaatkan oleh obral murahan.</td></tr>
          <tr><td><span class="pill pill-yellow">Excitement Komunal</span></td><td>Festival = sesuatu yang ramai dan dirayakan bersama (livestream, pop-up, antrian toko), bukan transaksi sepi sendirian.</td></tr>
        </tbody>
      </table>

      <h3 class="sub"><span class="dot"></span>Value Proposition</h3>
      <div class="grid-3">
        <div class="card">
          <div class="card-title">Untuk Pelanggan</div>
          <p style="margin:0;">Kesempatan terbatas memiliki aksesoris gadget brand global dengan harga yang biasanya hanya bisa didapat dari barang tiruan - tanpa mengorbankan kualitas, garansi, dan keaslian.</p>
        </div>
        <div class="card">
          <div class="card-title">Untuk UniTAG</div>
          <p style="margin:0;">Satu momentum terstruktur untuk mempercepat perputaran inventory, memperkuat database pelanggan, dan membangun posisi UniTAG sebagai destinasi utama gadget accessories - bukan sekadar toko diskon.</p>
        </div>
        <div class="card">
          <div class="card-title">Untuk Brand Partner</div>
          <p style="margin:0;">Clearance terstruktur dengan narasi positif menjaga ekuitas brand (Spigen, Aulumu, Sharge, Momax, ) dibanding diskon liar yang tidak terkoordinasi dan merusak persepsi harga jangka panjang.</p>
        </div>
      </div>

      <h3 class="sub"><span class="dot"></span>Campaign Narrative</h3>
      <p>Narasi besar yang dibangun selama 30 hari mengikuti arc dramatis sederhana: <strong>Rahasia → Pengumuman → Pesta → Penutupan.</strong> Festival diperkenalkan sebagai sesuatu yang "akan terjadi" (membangun rasa penasaran), kemudian "resmi dimulai" dengan kejutan harga, berkembang menjadi puncak keramaian dengan partisipasi luas (komunitas, kreator, toko ramai), dan ditutup dengan rasa urgensi terakhir sebelum kembali ke harga normal - memberi pelanggan yang belum bertindak alasan kuat untuk segera memutuskan.</p>

      <h3 class="sub"><span class="dot"></span>Campaign Storytelling Framework</h3>
      <div class="diagram">
        <div class="row" style="margin-bottom:0; align-items:stretch;">
          <div class="node node-sub" style="min-width:200px;">
            <span class="sub-label">Babak 1 · Hook</span>
            "Ada sesuatu yang akan terjadi di UniTAG..."
          </div>
          <div class="node node-sub" style="min-width:200px;">
            <span class="sub-label">Babak 2 · Reveal</span>
            "Festival resmi dimulai - harga clearance brand original!"
          </div>
          <div class="node node-sub" style="min-width:200px;">
            <span class="sub-label">Babak 3 · Proof</span>
            Testimoni, keramaian toko, livestream, UGC pelanggan asli
          </div>
          <div class="node node-sub" style="min-width:200px;">
            <span class="sub-label">Babak 4 · Urgency</span>
            "Jam-jam terakhir sebelum harga normal kembali."
          </div>
        </div>
      </div>
      <p>Framework ini menjadi rujukan setiap tim ketika menyusun konten - baik itu Reels Instagram, video TikTok, broadcast WhatsApp, maupun naskah staff toko. Setiap babak punya nada emosional yang berbeda namun tetap dalam satu Big Idea yang sama, sehingga pelanggan yang mengikuti dari Hari 1 sampai Hari 30 merasakan satu cerita utuh, bukan kumpulan promo acak.</p>
    </section>

    <!-- SECTION 3: CAMPAIGN ARCHITECTURE -->
    <section id="sec-architecture">
      <div class="sec-head">
        <div class="sec-eyebrow">Bagian 03</div>
        <h2>Campaign Architecture</h2>
        <p class="lede">Struktur hierarki yang menjelaskan bagaimana satu Master Campaign menaungi seluruh sub-campaign brand, tema mingguan, dan aktivasi harian - supaya semua tim tahu di mana posisi pekerjaan mereka dalam keseluruhan festival.</p>
      </div>

      <h3 class="sub"><span class="dot"></span>Diagram Hierarki Kampanye</h3>
      <div class="diagram">
        <div class="tier">
          <div class="node node-master">🎉 UNITAG CLEARANCE FESTIVAL<br><span style="font-size:11px; font-weight:600; opacity:0.85;">Master Campaign - 30 Hari</span></div>
        </div>
        <div class="connector"></div>
        <div class="tree-row">
          <div class="node node-sub"><span class="sub-label">Supporting</span>Spigen Spotlight</div>
          <div class="node node-sub"><span class="sub-label">Supporting</span>Aulumu Days</div>
          <div class="node node-sub"><span class="sub-label">Supporting</span>Sharge Power Week</div>
          <div class="node node-sub"><span class="sub-label">Supporting</span>Momax Mega Deals</div>
          <div class="node node-sub"><span class="sub-label">Supporting</span> Sound Sale</div>
        </div>
        <div class="connector"></div>
        <div class="tree-row">
          <div class="node node-sub"><span class="sub-label">Minggu 1</span>Teasing</div>
          <div class="node node-sub"><span class="sub-label">Minggu 2</span>Launch</div>
          <div class="node node-sub"><span class="sub-label">Minggu 3</span>Scale</div>
          <div class="node node-sub"><span class="sub-label">Minggu 4</span>Last Chance</div>
        </div>
        <div class="connector"></div>
        <div class="tree-row">
          <div class="node node-sub" style="min-width:130px; font-size:12px;"><span class="sub-label">Harian</span>Tema Konten</div>
          <div class="node node-sub" style="min-width:130px; font-size:12px;"><span class="sub-label">Harian</span>Promo Mekanik</div>
          <div class="node node-sub" style="min-width:130px; font-size:12px;"><span class="sub-label">Harian</span>Channel Fokus</div>
        </div>
      </div>

      <h3 class="sub"><span class="dot"></span>Master Campaign vs Supporting Campaigns</h3>
      <p>Setiap brand tetap punya momen "spotlight"-nya sendiri di dalam festival besar - ini menjaga partner brand tetap merasa diperhatikan secara individual, sekaligus memberi variasi konten 30 hari sehingga tidak monoton. Namun seluruh komunikasi <strong>selalu membawa nama dan visual UNITAG CLEARANCE FESTIVAL</strong> sebagai induk; brand spotlight adalah "chapter", bukan campaign terpisah.</p>
      <table>
        <thead><tr><th>Supporting Campaign</th><th>Brand Fokus</th><th>Kategori Produk Utama</th><th>Posisi dalam Festival</th></tr></thead>
        <tbody>
          <tr><td><b>Spigen Spotlight</b></td><td>Spigen</td><td>Case, screen protector, mounting</td><td>Anchor brand - paling dikenal, dijadwalkan di minggu Launch untuk daya tarik maksimal</td></tr>
          <tr><td><b>Aulumu Days</b></td><td>Aulumu</td><td>Lifestyle gadget accessories</td><td>Variasi konten di minggu Teasing/Scale</td></tr>
          <tr><td><b>Sharge Power Week</b></td><td>Sharge</td><td>Charger, power bank, kabel</td><td>Tema "fungsional & daily-use" di minggu Scale</td></tr>
          <tr><td><b>Momax Mega Deals</b></td><td>Momax</td><td>Charging & mobile accessories</td><td>Pendukung bundle cross-category di minggu Scale</td></tr>
          <tr><td><b> Sound Sale</b></td><td></td><td>Audio - earbuds, speaker</td><td>Penutup festival di minggu Last Chance - kategori dengan emotional appeal tinggi (musik/gaming)</td></tr>
        </tbody>
      </table>

      <h3 class="sub"><span class="dot"></span>Tema Mingguan</h3>
      <table>
        <thead><tr><th>Minggu</th><th>Tema</th><th>Tujuan Utama</th><th>Nada Komunikasi</th></tr></thead>
        <tbody>
          <tr><td><span class="pill pill-blue">M1</span></td><td><b>"Sesuatu Sedang Disiapkan"</b></td><td>Bangun penasaran, jangan reveal harga dulu</td><td>Misterius, playful, sedikit menggoda</td></tr>
          <tr><td><span class="pill pill-orange">M2</span></td><td><b>"Festival Resmi Dimulai"</b></td><td>Reveal besar, dorong transaksi pertama secepat mungkin</td><td>Meriah, energik, penuh kejutan</td></tr>
          <tr><td><span class="pill pill-yellow">M3</span></td><td><b>"Puncak Pesta, Semua Ikut Rame"</b></td><td>Maksimalkan volume transaksi & partisipasi komunitas/kreator</td><td>Sosial, ramai, banyak bukti sosial (UGC, livestream)</td></tr>
          <tr><td><span class="pill pill-red">M4</span></td><td><b>"Detik Terakhir Sebelum Normal"</b></td><td>Konversi sisa pelanggan ragu, habiskan sisa stok prioritas</td><td>Mendesak, jujur tentang batas waktu, emosional penutup</td></tr>
        </tbody>
      </table>

      <h3 class="sub"><span class="dot"></span>Tema Aktivasi Harian (Pola yang Berulang Tiap Minggu)</h3>
      <p>Untuk menjaga konsistensi tanpa membuat tim kehabisan ide setiap hari, ditetapkan satu pola 7 hari yang berulang dengan konten yang disesuaikan temanya sesuai minggu berjalan:</p>
      <table>
        <thead><tr><th>Hari</th><th>Tema Aktivasi</th><th>Fokus Konten</th></tr></thead>
        <tbody>
          <tr><td><b>Senin</b></td><td>Motivation Monday</td><td>Kick-off energi minggu - highlight produk/bundle andalan minggu ini</td></tr>
          <tr><td><b>Selasa</b></td><td>Tips & Trick Tuesday</td><td>Edukasi produk - cara pilih case/charger yang tepat, dibungkus soft-sell</td></tr>
          <tr><td><b>Rabu</b></td><td>Wishlist Wednesday</td><td>Showcase produk impian dengan harga clearance - angle aspirational</td></tr>
          <tr><td><b>Kamis</b></td><td>Throwback/Testimonial Thursday</td><td>UGC, testimoni pelanggan, before-after pakai aksesoris original vs KW</td></tr>
          <tr><td><b>Jumat</b></td><td>Flash Sale Friday</td><td>Mekanik promo flash sale jam tertentu - momentum akhir pekan</td></tr>
          <tr><td><b>Sabtu</b></td><td>Shopping Saturday</td><td>Dorongan kuat ke marketplace & toko fisik - peak traffic weekend</td></tr>
          <tr><td><b>Minggu</b></td><td>Sunday Recap & Countdown</td><td>Rekap highlight minggu + reminder hari tersisa hingga festival selesai</td></tr>
        </tbody>
      </table>

      <div class="callout good">
        <div class="callout-icon">✅</div>
        <div>Pola harian ini akan diturunkan menjadi <strong>30-Day Content Calendar</strong> yang lebih rinci (dengan konsep Reel/TikTok/Story spesifik per hari) di dokumen Channel Execution selanjutnya - arsitektur di atas adalah kerangka acuannya.</div>
      </div>
    </section>

    <!-- SECTION 4: 30-DAY ROADMAP -->
    <section id="sec-roadmap">
      <div class="sec-head">
        <div class="sec-eyebrow">Bagian 04</div>
        <h2>30-Day Campaign Roadmap</h2>
        <p class="lede">Peta eksekusi lengkap yang membagi 30 hari menjadi 4 fase dengan eskalasi urgency terukur. Setiap fase memuat objective, key message, strategi konten, promosi, channel, dan KPI agar tim bisa langsung eksekusi tanpa perlu briefing tambahan.</p>
      </div>

      <h3 class="sub"><span class="dot"></span>Timeline at a Glance</h3>
      <div class="timeline-bar">
        <div class="timeline-seg seg-1">TEASING<span class="days">Hari 1–5</span></div>
        <div class="timeline-seg seg-2">LAUNCH<span class="days">Hari 6–12</span></div>
        <div class="timeline-seg seg-3">SCALE<span class="days">Hari 13–24</span></div>
        <div class="timeline-seg seg-4">LAST CHANCE<span class="days">Hari 25–30</span></div>
      </div>

      <!-- PHASE 1 -->
      <div class="phase-block phase-1">
        <div class="phase-head">
          <div class="phase-head-left">
            <div class="phase-num">01</div>
            <div>
              <div class="phase-title">Phase 1 - Teasing</div>
              <div class="phase-days">Hari 1–5 · Membangun penasaran tanpa membongkar harga</div>
            </div>
          </div>
          <span class="pill pill-blue">Awareness</span>
        </div>
        <div class="phase-body">
          <h4 class="minor">Objectives</h4>
          <ul class="clean">
            <li>Membangun rasa ingin tahu tentang "sesuatu yang akan terjadi" di UniTAG tanpa mengungkap detail diskon.</li>
            <li>Memaksimalkan reach awal agar database existing customer dan calon pelanggan baru sama-sama "terpapar" sebelum launch.</li>
            <li>Mengumpulkan early-bird signup/WhatsApp list untuk dijadikan target broadcast pertama saat Launch.</li>
          </ul>
          <h4 class="minor">Key Messages</h4>
          <ul class="clean">
            <li>"Ada sesuatu yang sedang disiapkan di UniTAG..."</li>
            <li>"Yang selama ini nahan beli karena harga - tunggu tanggalnya."</li>
            <li>"Siap-siap, festival aksesoris original terbesar tahun ini akan datang."</li>
          </ul>
          <h4 class="minor">Content Strategy</h4>
          <ul class="clean">
            <li>Teaser visual bertema "misteri" - close-up produk dengan elemen tersembunyi/blur, countdown sticker di Stories.</li>
            <li>Polling/quiz interaktif ("Tebak produk apa yang bakal clearance gede-gedean") untuk memancing engagement dan komentar.</li>
            <li>Soft-launch landing page "Daftar untuk Akses Duluan" - mengumpulkan WhatsApp/email sebelum harga dibuka ke publik.</li>
          </ul>
          <h4 class="minor">Promotions</h4>
          <ul class="clean">
            <li>Belum ada diskon yang diumumkan terbuka - hanya "early access" untuk yang signup, menciptakan eksklusivitas.</li>
            <li>Insentif kecil untuk signup (contoh: voucher tambahan khusus pendaftar awal, dijelaskan detail di dokumen CRM).</li>
          </ul>
          <h4 class="minor">Marketing Channels</h4>
          <p style="margin-bottom:6px;"><span class="pill pill-orange">Instagram</span> <span class="pill pill-orange">TikTok</span> <span class="pill pill-blue">WhatsApp Broadcast (existing customer)</span> <span class="pill pill-blue">In-store teaser POSM</span></p>
          <div class="kpi-strip">
            <div class="kpi-chip">Reach teaser content <b>↑</b></div>
            <div class="kpi-chip">Jumlah signup early-access <b>↑</b></div>
            <div class="kpi-chip">Engagement rate teaser post <b>↑</b></div>
            <div class="kpi-chip">Pertumbuhan WhatsApp list <b>↑</b></div>
          </div>
        </div>
      </div>

      <!-- PHASE 2 -->
      <div class="phase-block phase-2">
        <div class="phase-head">
          <div class="phase-head-left">
            <div class="phase-num">02</div>
            <div>
              <div class="phase-title">Phase 2 - Launch</div>
              <div class="phase-days">Hari 6–12 · Reveal besar dan dorongan transaksi pertama</div>
            </div>
          </div>
          <span class="pill pill-orange">Conversion Start</span>
        </div>
        <div class="phase-body">
          <h4 class="minor">Objectives</h4>
          <ul class="clean">
            <li>Membuka festival secara resmi dengan reveal harga clearance - momen "big bang" yang harus terasa besar di semua channel serempak.</li>
            <li>Mendorong transaksi awal secepat mungkin untuk membangun momentum sosial (orderan masuk, testimoni cepat muncul).</li>
            <li>Mengaktifkan seluruh channel sekaligus - toko, marketplace, media sosial, WhatsApp - pada hari/jam launch yang sama.</li>
          </ul>
          <h4 class="minor">Key Messages</h4>
          <ul class="clean">
            <li>"UNITAG CLEARANCE FESTIVAL resmi dimulai - Original Accessories, Clearance Price!"</li>
            <li>"Yang kamu tunggu sudah di sini. Brand favoritmu, harga yang nggak bakal kamu sesali."</li>
            <li>"Stok terbatas, harga ini nggak akan kembali setelah festival selesai."</li>
          </ul>
          <h4 class="minor">Content Strategy</h4>
          <ul class="clean">
            <li>"Reveal video" - countdown live ke 0, lalu tampilkan harga clearance produk-produk hero secara dramatis.</li>
            <li>Carousel "before vs after harga" untuk produk-produk unggulan tiap brand.</li>
            <li>Live shopping perdana di TikTok/Shopee Live untuk hari pertama launch - menampilkan reaksi real-time terhadap harga.</li>
          </ul>
          <h4 class="minor">Promotions</h4>
          <ul class="clean">
            <li>Diskon clearance resmi dibuka untuk produk overstock prioritas - harga ditampilkan terbuka di semua channel.</li>
            <li>Flash sale "Launch Day" 24 jam pertama dengan insentif tambahan (voucher ongkir/cashback) untuk transaksi tercepat.</li>
            <li>Bundle pembuka festival - kombinasi cross-brand pertama diperkenalkan (detail di dokumen Bundle Strategy).</li>
          </ul>
          <h4 class="minor">Marketing Channels</h4>
          <p style="margin-bottom:6px;"><span class="pill pill-orange">Instagram</span> <span class="pill pill-orange">TikTok</span> <span class="pill pill-orange">Facebook</span> <span class="pill pill-blue">Shopee/Tokopedia/TikTok Shop</span> <span class="pill pill-blue">Website</span> <span class="pill pill-blue">WhatsApp Broadcast (full database)</span> <span class="pill pill-green">In-store launch activation</span></p>
          <div class="kpi-strip">
            <div class="kpi-chip">Transaksi 24 jam pertama <b>↑</b></div>
            <div class="kpi-chip">Trafik toko & marketplace <b>↑</b></div>
            <div class="kpi-chip">CTR iklan launch <b>↑</b></div>
            <div class="kpi-chip">Konversi WhatsApp broadcast <b>↑</b></div>
          </div>
        </div>
      </div>

      <!-- PHASE 3 -->
      <div class="phase-block phase-3">
        <div class="phase-head">
          <div class="phase-head-left">
            <div class="phase-num">03</div>
            <div>
              <div class="phase-title">Phase 3 - Scale</div>
              <div class="phase-days">Hari 13–24 · Memperluas reach, memaksimalkan volume transaksi</div>
            </div>
          </div>
          <span class="pill pill-yellow">Volume & Reach</span>
        </div>
        <div class="phase-body">
          <h4 class="minor">Objectives</h4>
          <ul class="clean">
            <li>Memperluas jangkauan ke audiens yang belum terpapar di fase Launch - termasuk lewat kreator/affiliate.</li>
            <li>Memaksimalkan volume transaksi harian melalui ritme promo yang konsisten (tidak hanya mengandalkan momentum launch).</li>
            <li>Mendorong partisipasi komunitas - UGC, testimoni, dan engagement organik sebagai bukti sosial berkelanjutan.</li>
          </ul>
          <h4 class="minor">Key Messages</h4>
          <ul class="clean">
            <li>"Festival masih berlangsung - dan makin rame!"</li>
            <li>"Udah banyak yang upgrade ke original, kamu kapan?"</li>
            <li>"Brand spotlight minggu ini: [Sharge/Momax/Aulumu] - cek koleksi clearance-nya."</li>
          </ul>
          <h4 class="minor">Content Strategy</h4>
          <ul class="clean">
            <li>Rotasi brand spotlight mingguan (Sharge Power Week, Momax Mega Deals, Aulumu Days) sesuai Campaign Architecture.</li>
            <li>UGC campaign - repost konten pelanggan yang membeli, beri insentif kecil untuk yang posting dengan hashtag campaign.</li>
            <li>Kolaborasi nano/micro influencer dan tech reviewer untuk review jujur produk dengan harga clearance (detail di dokumen Influencer Strategy).</li>
            <li>Livestream rutin 2-3x seminggu di TikTok Shop/Shopee Live dengan tema brand spotlight berjalan.</li>
          </ul>
          <h4 class="minor">Promotions</h4>
          <ul class="clean">
            <li>Flash sale mingguan terjadwal (mengikuti tema "Flash Sale Friday" dari Campaign Architecture).</li>
            <li>Bundle baru diperkenalkan bertahap - tidak semua bundle dibuka sekaligus di awal, agar selalu ada "yang baru" tiap minggu.</li>
            <li>Program affiliate/komisi untuk kreator yang mendorong konversi langsung ke marketplace.</li>
          </ul>
          <h4 class="minor">Marketing Channels</h4>
          <p style="margin-bottom:6px;"><span class="pill pill-orange">Semua channel aktif penuh</span> <span class="pill pill-blue">Influencer/KOL</span> <span class="pill pill-blue">Affiliate marketplace</span> <span class="pill pill-green">Modern retail partner & pop-up event</span></p>
          <div class="kpi-strip">
            <div class="kpi-chip">Volume transaksi harian stabil <b>↑</b></div>
            <div class="kpi-chip">Jumlah UGC/mention <b>↑</b></div>
            <div class="kpi-chip">Reach dari konten kreator <b>↑</b></div>
            <div class="kpi-chip">Repeat purchase rate <b>↑</b></div>
          </div>
        </div>
      </div>

      <!-- PHASE 4 -->
      <div class="phase-block phase-4">
        <div class="phase-head">
          <div class="phase-head-left">
            <div class="phase-num">04</div>
            <div>
              <div class="phase-title">Phase 4 - Last Chance</div>
              <div class="phase-days">Hari 25–30 · Urgensi penutup dan konversi sisa keraguan</div>
            </div>
          </div>
          <span class="pill pill-red">Urgency & Closing</span>
        </div>
        <div class="phase-body">
          <h4 class="minor">Objectives</h4>
          <ul class="clean">
            <li>Mengkonversi pelanggan yang sudah tertarik tapi belum bertransaksi (warm audience dari retargeting 3 fase sebelumnya).</li>
            <li>Menghabiskan sisa stok prioritas yang belum terjual dengan mekanik penutup yang lebih agresif.</li>
            <li>Menutup festival dengan kesan positif dan jelas - bukan "ngilang diam-diam" - agar membangun ekspektasi sehat untuk festival berikutnya.</li>
          </ul>
          <h4 class="minor">Key Messages</h4>
          <ul class="clean">
            <li>"Tinggal beberapa hari sebelum harga normal kembali."</li>
            <li>"Last call - yang belum upgrade ke original, ini kesempatan terakhir."</li>
            <li>"Terima kasih sudah jadi bagian dari festival terbesar UniTAG tahun ini."</li>
          </ul>
          <h4 class="minor">Content Strategy</h4>
          <ul class="clean">
            <li>Countdown harian terbuka (H-5, H-4 ... H-Hari Terakhir) di semua channel - visual jam/clock yang konsisten.</li>
            <li>Retargeting konten khusus ke audiens yang sudah engage tapi belum beli ("Masih ada di keranjangmu, jangan sampai kehabisan").</li>
            <li>Konten "Clearance Hour" - jam spesifik di hari-hari terakhir dengan diskon tambahan singkat untuk mendorong keputusan instan.</li>
            <li>Recap/highlight video penutup festival - momen ramai toko, testimoni, angka pencapaian (tanpa membuka data sensitif internal).</li>
          </ul>
          <h4 class="minor">Promotions</h4>
          <ul class="clean">
            <li>Mekanik "Clearance Hour" dan "Last Call Bundle" - kombinasi sisa stok prioritas dengan harga paling agresif di seluruh festival.</li>
            <li>Lucky draw/mystery box penutup sebagai bonus tambahan untuk transaksi di periode ini (detail mekanik di dokumen Promotional Mechanics).</li>
            <li>Pengumuman tegas tanggal & jam terakhir - tidak ada perpanjangan, untuk menjaga kredibilitas urgency di festival berikutnya.</li>
          </ul>
          <h4 class="minor">Marketing Channels</h4>
          <p style="margin-bottom:6px;"><span class="pill pill-red">Retargeting Meta/Google Ads</span> <span class="pill pill-orange">WhatsApp Broadcast (last call)</span> <span class="pill pill-blue">In-store countdown POSM</span> <span class="pill pill-blue">Marketplace flash sale penutup</span></p>
          <div class="kpi-strip">
            <div class="kpi-chip">Konversi dari retargeting audience <b>↑</b></div>
            <div class="kpi-chip">Reduksi stok prioritas akhir <b>↑</b></div>
            <div class="kpi-chip">Transaksi di Clearance Hour <b>↑</b></div>
            <div class="kpi-chip">Sentimen penutup (komentar/review) <b>positif</b></div>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION 5: STORE LAYOUT -->
    <section id="sec-layout">
      <div class="sec-head">
        <div class="sec-eyebrow">Bagian 05</div>
        <h2>Layout Store</h2>
        <img class="img-store" style="width:100%" src="https://i.ibb.co.com/CpqVZcm3/Chat-GPT-Image-18-Jun-2026-10-07-35.png">
    </section>

    <!-- SECTION 6: ONLINE MARKETING -->
    <section id="sec-online">
      <div class="sec-head">
        <div class="sec-eyebrow">Bagian 06</div>
        <h2>Online Marketing Strategy</h2>
        <p class="lede">Strategi lengkap untuk Instagram, TikTok, Facebook, dan Website - masing-masing dengan peran berbeda dalam funnel namun tetap satu suara dengan Big Idea festival.</p>
      </div>

      <!-- INSTAGRAM -->
      <div class="platform-banner">
        <div class="platform-icon platform-ig">📸</div>
        <div><div class="platform-title">Instagram</div><div class="platform-sub">Peran: Brand storytelling, edukasi produk, dan community hub festival</div></div>
      </div>

      <h4 class="minor">Content Pillars</h4>
      <table>
        <thead><tr><th>Pillar</th><th>Porsi</th><th>Tujuan</th><th>Contoh Format</th></tr></thead>
        <tbody>
          <tr><td><b>Festival Hype</b></td><td>30%</td><td>Reveal harga, countdown, urgency</td><td>Reels reveal, Stories countdown sticker</td></tr>
          <tr><td><b>Product Education</b></td><td>25%</td><td>Edukasi kualitas original vs KW</td><td>Carousel perbandingan, tips memilih aksesoris</td></tr>
          <tr><td><b>Social Proof</b></td><td>20%</td><td>Bangun trust lewat testimoni nyata</td><td>Repost UGC, review tech reviewer</td></tr>
          <tr><td><b>Bundle Spotlight</b></td><td>15%</td><td>Dorong AOV lebih tinggi</td><td>Carousel bundle, Reels unboxing bundle</td></tr>
          <tr><td><b>Behind the Scenes</b></td><td>10%</td><td>Humanisasi brand, bangun kedekatan</td><td>Stories suasana toko ramai, tim sedang packing</td></tr>
        </tbody>
      </table>

      <h4 class="minor">Reels Strategy</h4>
      <ul class="clean">
        <li><strong>Hook 3 detik pertama wajib visual, bukan teks panjang</strong> - gunakan jump-cut harga ("KW: Rp X → Original UniTAG: Rp Y") atau reaksi orang kaget melihat harga.</li>
        <li>Setiap Reels festival diakhiri CTA konsisten: "Cek link di bio / DM 'FESTIVAL' untuk info bundle."</li>
        <li>Gunakan audio trending tapi tetap relevan dengan mood babak cerita (misterius untuk Teasing, energik untuk Launch/Scale, dramatis-mendesak untuk Last Chance).</li>
        <li>Frekuensi: minimal 1 Reels/hari selama Launch & Scale, 2x/hari saat hari-hari kunci (Launch Day, Last Chance Day terakhir).</li>
      </ul>

      <h4 class="minor">Carousel Strategy</h4>
      <ul class="clean">
        <li>Carousel "Before-After Harga" - slide 1 sebagai hook (harga normal dicoret), slide berikutnya reveal harga clearance per produk dalam satu kategori.</li>
        <li>Carousel edukatif "5 Tanda Aksesoris KW yang Bisa Merusak HP-mu" - soft-sell mengarah ke value original dengan harga festival.</li>
        <li>Carousel bundle "Paket Hemat untuk [Persona]" (mahasiswa, gamer, profesional) - menyasar segmentasi target audience secara spesifik.</li>
      </ul>

      <h4 class="minor">Stories Strategy</h4>
      <ul class="clean">
        <li>Countdown sticker di setiap fase - terutama krusial di Teasing (menuju launch) dan Last Chance (menuju penutupan).</li>
        <li>Polling & quiz interaktif untuk riset minat sekaligus meningkatkan engagement algoritma ("Mana yang lebih kamu butuh: case atau power bank?").</li>
        <li>Highlight permanen "FESTIVAL INFO" yang di-update tiap fase - jadi rujukan cepat pelanggan yang baru menemukan akun di tengah festival.</li>
        <li>Swipe-up/link sticker langsung ke landing page atau marketplace untuk produk yang sedang ditampilkan.</li>
      </ul>

      <h4 class="minor">Community Engagement Strategy</h4>
      <ul class="clean">
        <li>Respons DM dan komentar dengan SLA maksimal 1 jam selama jam operasional - kecepatan respons krusial saat urgency tinggi (Launch, Last Chance).</li>
        <li>Repost UGC pelanggan ke Stories dengan ucapan terima kasih personal - memperkuat rasa "dirayakan bersama".</li>
        <li>Buat saved-reply template untuk pertanyaan FAQ umum (stok, garansi, cara klaim bundle) agar respons cepat dan konsisten.</li>
      </ul>

      <div class="divider"></div>

      <!-- TIKTOK -->
      <div class="platform-banner">
        <div class="platform-icon platform-tt">🎵</div>
        <div><div class="platform-title">TikTok</div><div class="platform-sub">Peran: Viral reach, konten otentik, akselerasi konversi via TikTok Shop</div></div>
      </div>

      <h4 class="minor">Viral Content Strategy</h4>
      <ul class="clean">
        <li>Format "harga reveal shock" - talent kaget melihat harga clearance produk premium, terbukti performa tinggi di kategori gadget accessories.</li>
        <li>Format "POV beli KW vs Original" - storytelling singkat dramatis yang relate dengan insight konsumen (pernah kena masalah pakai KW).</li>
        <li>Manfaatkan tren audio/format yang sedang viral tapi tetap disesuaikan ritme festival - jangan ikut tren yang tidak related sama sekali dengan produk.</li>
        <li>Konsistensi posting jadi kunci algoritma TikTok - minimal 1x/hari, idealnya 2x di hari-hari kunci (Launch, Flash Sale Friday, Last Chance).</li>
      </ul>

      <h4 class="minor">Creator Strategy</h4>
      <ul class="clean">
        <li>Kombinasi nano (5K-20K followers) untuk volume dan keotentikan, dengan beberapa micro (20K-100K) untuk reach lebih luas - detail lengkap di Section 10.</li>
        <li>Brief creator dengan kebebasan kreatif dalam format, tapi wajib menyebut nama campaign dan harga clearance yang akurat.</li>
        <li>Prioritaskan creator yang sudah punya audiens relevan (tech, gadget review, lifestyle mahasiswa/profesional muda).</li>
      </ul>

      <h4 class="minor">Affiliate Strategy</h4>
      <ul class="clean">
        <li>Aktifkan TikTok Shop Affiliate Program dengan komisi kompetitif khusus produk overstock prioritas - affiliate akan natural memilih produk dengan komisi lebih tinggi.</li>
        <li>Sediakan sample produk gratis untuk affiliate aktif sebagai insentif tambahan membuat konten organik.</li>
        <li>Pantau leaderboard affiliate mingguan, beri shoutout/bonus untuk top performer agar termotivasi konsisten selama 30 hari.</li>
      </ul>

      <h4 class="minor">Live Strategy</h4>
      <ul class="clean">
        <li>Jadwal live minimal 3x/minggu selama Scale, dengan host yang energik dan paham produk (bukan sekadar baca script).</li>
        <li>Setiap live wajib ada flash deal eksklusif "khusus yang nonton live" - insentif menonton sampai akhir.</li>
        <li>Gunakan fitur pinned product dan countdown sticker dalam live untuk mendorong keputusan instan.</li>
      </ul>

      <div class="divider"></div>

      <!-- WEBSITE -->
      <div class="platform-banner">
        <div class="platform-icon platform-web">🌐</div>
        <div><div class="platform-title">Website</div><div class="platform-sub">Peran: Hub informasi resmi festival dan konversi langsung tanpa potongan marketplace</div></div>
      </div>

      <h4 class="minor">Landing Page Strategy</h4>
      <ul class="clean">
        <li>Satu landing page khusus festival (<code>/clearance-festival</code>) yang menjadi destinasi utama dari semua link bio dan iklan - bukan halaman kategori produk biasa.</li>
        <li>Struktur halaman: Hero dengan Big Idea & countdown → highlight bundle unggulan → kategori brand (Spigen/Aulumu/Sharge/Momax/) → social proof/testimoni → FAQ → CTA akhir.</li>
        <li>Update visual landing page mengikuti fase berjalan - versi Teasing (misterius, form signup), versi Launch/Scale (katalog penuh), versi Last Chance (banner urgency dominan di atas).</li>
      </ul>

      <h4 class="minor">CRO (Conversion Rate Optimization) Strategy</h4>
      <ul class="clean">
        <li>Pasang trust badge jelas (100% Original, Garansi Resmi) di dekat tombol beli - menjawab langsung kekhawatiran konsumen soal keaslian barang.</li>
        <li>Sediakan live chat/WhatsApp widget mengambang di seluruh halaman untuk pertanyaan cepat sebelum checkout.</li>
        <li>Tampilkan stok terbatas secara jujur ("Tersisa X unit") pada produk overstock prioritas - memperkuat urgency tanpa perlu klaim palsu.</li>
        <li>Sederhanakan proses checkout maksimal 3 langkah, dengan opsi pembayaran lokal yang familiar (transfer bank, e-wallet, COD jika tersedia).</li>
        <li>Pasang exit-intent popup ringan dengan insentif kecil (voucher tambahan) khusus untuk pengunjung yang akan meninggalkan halaman tanpa checkout.</li>
      </ul>
    </section>

    <!-- SECTION 7: MARKETPLACE STRATEGY -->
    <section id="sec-marketplace">
      <div class="sec-head">
        <div class="sec-eyebrow">Bagian 07</div>
        <h2>Marketplace Strategy</h2>
        <p class="lede">Shopee, Tokopedia, dan TikTok Shop adalah mesin konversi volume tertinggi selama festival — strategi di bawah berlaku untuk ketiga platform dengan penyesuaian fitur masing-masing.</p>
      </div>

      <div class="grid-3">
        <div class="platform-banner" style="margin-bottom:0;">
          <div class="platform-icon platform-shopee">🛍️</div>
          <div><div class="platform-title" style="font-size:15px;">Shopee</div><div class="platform-sub">Volume tertinggi, basis pengguna luas</div></div>
        </div>
        <div class="platform-banner" style="margin-bottom:0;">
          <div class="platform-icon platform-tokped">🛒</div>
          <div><div class="platform-title" style="font-size:15px;">Tokopedia</div><div class="platform-sub">Basis pengguna lebih matang/profesional</div></div>
        </div>
        <div class="platform-banner" style="margin-bottom:0;">
          <div class="platform-icon platform-ttshop">🎬</div>
          <div><div class="platform-title" style="font-size:15px;">TikTok Shop</div><div class="platform-sub">Konversi langsung dari konten video</div></div>
        </div>
      </div>

      <h3 class="sub" style="margin-top:30px;"><span class="dot"></span>Flash Sale Strategy</h3>
      <table>
        <thead><tr><th>Fase</th><th>Frekuensi Flash Sale</th><th>Mekanik</th></tr></thead>
        <tbody>
          <tr><td>Teasing</td><td>Tidak ada (jaga reveal untuk Launch)</td><td>Hanya signup early access di luar marketplace</td></tr>
          <tr><td>Launch</td><td>1x — 24 jam penuh hari pertama</td><td>Diskon clearance dibuka serentak di semua platform pada jam yang sama</td></tr>
          <tr><td>Scale</td><td>2-3x/minggu (mengikuti Flash Sale Friday)</td><td>Slot waktu spesifik (misal 12:00 & 20:00) dengan kuota terbatas per slot</td></tr>
          <tr><td>Last Chance</td><td>Setiap hari ("Clearance Hour")</td><td>Jam singkat 1-2 jam dengan diskon tambahan di atas harga clearance dasar</td></tr>
        </tbody>
      </table>

      <h3 class="sub"><span class="dot"></span>Voucher Strategy</h3>
      <ul class="clean">
        <li><strong>Voucher Toko (Shop Voucher):</strong> potongan langsung untuk minimum belanja tertentu, aktif sepanjang festival sebagai insentif dasar.</li>
        <li><strong>Voucher Cashback:</strong> dikombinasikan dengan program cashback platform untuk memaksimalkan visibilitas listing di halaman promo marketplace.</li>
        <li><strong>Voucher Eksklusif Followers:</strong> khusus untuk yang follow toko — mendorong pertumbuhan follower sekaligus basis retargeting di kemudian hari.</li>
        <li><strong>Voucher Last Chance:</strong> nominal lebih besar tapi berlaku sangat singkat (jam terakhir festival) untuk dorongan keputusan final.</li>
      </ul>

      <h3 class="sub"><span class="dot"></span>Bundle Strategy (Marketplace)</h3>
      <p>Bundle lengkap (20+ ide) akan disusun di dokumen Bundle & Promo Mechanics — namun untuk eksekusi marketplace, prinsip kuncinya:</p>
      <ul class="clean">
        <li>Setiap bundle dibuat sebagai <strong>listing tersendiri</strong> (bukan hanya catatan di deskripsi produk) agar muncul di pencarian dan bisa di-iklankan terpisah.</li>
        <li>Foto utama bundle harus menampilkan semua item dalam satu frame yang jelas — bundle dengan foto produk terpisah-pisah cenderung performa konversi lebih rendah.</li>
        <li>Bundle ditampilkan dengan perbandingan "harga total jika beli satuan" vs "harga bundle" secara eksplisit di gambar produk.</li>
      </ul>

      <h3 class="sub"><span class="dot"></span>Livestream Strategy</h3>
      <ul class="clean">
        <li>Jadwal tetap dan konsisten (misal setiap Sabtu jam 19:00) agar pelanggan setia tahu kapan harus menonton — konsistensi membangun audiens berulang.</li>
        <li>Setiap sesi live wajib menampilkan minimal satu flash deal eksklusif yang hanya berlaku selama live berlangsung.</li>
        <li>Host harus hafal detail produk (material, garansi, perbandingan dengan KW) untuk menjawab pertanyaan real-time di kolom chat dengan percaya diri.</li>
        <li>Gunakan fitur giveaway/lucky spin di tengah live untuk menahan penonton lebih lama (durasi tonton mempengaruhi distribusi algoritma platform).</li>
      </ul>

      <h3 class="sub"><span class="dot"></span>Affiliate Strategy (Marketplace)</h3>
      <ul class="clean">
        <li>Daftarkan seluruh katalog overstock prioritas ke program affiliate marketplace dengan komisi lebih tinggi dibanding produk reguler.</li>
        <li>Berikan komisi tambahan/bonus tier untuk affiliate yang mencapai target penjualan tertentu selama periode festival.</li>
        <li>Pantau performa affiliate per minggu, alihkan fokus promosi ke affiliate dengan konversi terbaik di sisa periode festival.</li>
      </ul>

      <h3 class="sub"><span class="dot"></span>Conversion Optimization Strategy</h3>
      <ul class="clean">
        <li><strong>Judul listing:</strong> sertakan nama brand, kata kunci pencarian umum (case iphone, power bank fast charging), dan penanda "Original/Resmi" — krusial untuk SEO marketplace.</li>
        <li><strong>Foto produk:</strong> minimal 1 foto perbandingan ukuran/skala, 1 foto detail material/tekstur, dan 1 foto lifestyle penggunaan — bukan hanya foto produk putih polos.</li>
        <li><strong>Respons chat cepat:</strong> performa toko (Shop Rating, Chat Response Rate) langsung mempengaruhi posisi di hasil pencarian — SLA respons maksimal 15 menit selama jam operasional festival.</li>
        <li><strong>Kelola review aktif:</strong> follow-up pelanggan pasca-transaksi untuk memberi rating & ulasan, terutama dari pembeli bundle yang puas — ulasan positif memperkuat kepercayaan calon pembeli lain.</li>
        <li><strong>Stok & variasi jelas:</strong> pastikan stok di listing selalu update real-time agar tidak ada pembeli kecewa karena stok kosong setelah checkout.</li>
      </ul>

      <div class="callout info">
        <div class="callout-icon">🔁</div>
        <div><strong>Koordinasi lintas-platform:</strong> Flash sale dan voucher di Shopee, Tokopedia, dan TikTok Shop harus dijalankan pada <strong>jam yang sama</strong> setiap kali memungkinkan. Ini menghindari kebingungan pelanggan ("kok di Shopee diskon, di Tokped belum?") dan memperkuat kesan festival yang terkoordinasi rapi, bukan promo acak per-channel.</div>
      </div>
    </section>

  </div>
</main>

<script>
  document.querySelectorAll('.nav-link, .footer-nav a').forEach(link => {
    link.addEventListener('click', (e) => {
      e.preventDefault();
      const target = document.getElementById(link.dataset.target);
      if(target){ target.scrollIntoView({behavior:'smooth', block:'start'}); }
    });
  });

  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-link');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if(entry.isIntersecting){
        navLinks.forEach(l => l.classList.remove('active'));
        const active = document.querySelector(`.nav-link[data-target="${entry.target.id}"]`);
        if(active) active.classList.add('active');
      }
    });
  }, { rootMargin: '-15% 0px -75% 0px' });
  sections.forEach(s => observer.observe(s));
</script>

</body>
</html>