# Wbsite-my
Website
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Daftar Lapangan Futsal — Keren & Mantap</title>
    <style>
        :root{
          --bg:#0a0f1a;
          --card:#11182a;
          --glass:rgba(255,255,255,.06);
          --text:#e8f0ff;
          --muted:#a8b3cf;
          --primary:#3b82f6;
          --accent:#22d3ee;
          --good:#10b981;
          --warn:#f59e0b;
          --danger:#ef4444;
          --border:rgba(255,255,255,.12);
          --shadow:0 12px 30px rgba(0,0,0,.35);
        }
        *{box-sizing:border-box}
        html,body{height:100%}
        body{
          margin:0;
          font-family: ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
          background:
            radial-gradient(1200px 600px at 10% 0%, #0d1b2a 0%, var(--bg) 60%),
            radial-gradient(900px 500px at 90% 100%, #041024 0%, var(--bg) 60%);
          color:var(--text);
        }
        header{
          position:relative;
          padding:48px 20px 24px;
          text-align:center;
          overflow:hidden;
        }
        .shine{
          position:absolute; inset:0;
          background:
            radial-gradient(400px 140px at 20% 10%, rgba(59,130,246,.25), transparent 60%),
            radial-gradient(500px 160px at 80% 20%, rgba(34,211,238,.25), transparent 60%);
          filter: blur(40px);
          pointer-events:none;
        }
        h1{
          margin:0 0 10px;
          font-size: clamp(28px, 4vw, 44px);
          letter-spacing:.5px;
          background: linear-gradient(90deg, #fff 0%, #cde1ff 40%, #a6fffb 100%);
          -webkit-background-clip:text; background-clip:text; color:transparent;
        }
        .subtitle{
          margin:0 auto 22px;
          max-width:700px;
          color:var(--muted);
          font-size: clamp(14px, 2.4vw, 18px);
        }
        .toolbar{
          display:grid; gap:12px;
          grid-template-columns: 1.2fr .9fr .9fr .6fr .6fr;
          max-width:1100px; margin:0 auto; padding:10px;
          background: linear-gradient(180deg, rgba(255,255,255,.08), rgba(255,255,255,.04));
          border:1px solid var(--border); border-radius:16px;
          backdrop-filter: saturate(160%) blur(8px);
          box-shadow: var(--shadow);
        }
        .field{position:relative}
        .field input,.field select{
          width:100%; padding:12px 14px; border-radius:12px;
          border:1px solid var(--border); background:var(--card); color:var(--text);
          outline:none; transition: border .2s, box-shadow .2s;
        }
        .field input:focus,.field select:focus{
          border-color: rgba(59,130,246,.5);
          box-shadow: 0 0 0 4px rgba(59,130,246,.15);
        }
        .btn{
          display:flex; align-items:center; justify-content:center; gap:8px;
          border:none; border-radius:12px; cursor:pointer; padding:12px 14px;
          background: linear-gradient(90deg, var(--primary), #6366f1);
          color:#fff; font-weight:600; letter-spacing:.2px;
          transition: transform .08s ease, filter .2s ease;
        }
        .btn:hover{filter: brightness(1.1)}
        .btn:active{transform: translateY(1px)}
        .toggle{
          background: linear-gradient(90deg, #0ea5e9, var(--accent));
        }

        main{max-width:1200px; margin:24px auto; padding:0 20px 60px}

        .grid{
          display:grid; gap:18px;
          grid-template-columns: repeat(12, 1fr);
        }
        @media (max-width: 1080px){
          .grid{grid-template-columns: repeat(8, 1fr)}
        }
        @media (max-width: 760px){
          .toolbar{grid-template-columns: 1fr 1fr; }
          .btn.toggle{grid-column: 1 / -1}
          .grid{grid-template-columns: repeat(2, 1fr)}
        }
        @media (max-width: 520px){
          .grid{grid-template-columns: 1fr}
        }

        .card{
          grid-column: span 3;
          background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
          border:1px solid var(--border); border-radius:16px; overflow:hidden;
          box-shadow: var(--shadow); transition: transform .15s ease, box-shadow .2s ease, border .2s ease;
          position:relative;
        }
        .card:hover{transform: translateY(-2px); box-shadow: 0 16px 40px rgba(0,0,0,.45); border-color: rgba(255,255,255,.18)}
        .thumb{
          aspect-ratio: 16/9; width:100%;
          background:
            radial-gradient(160px 80px at 20% 30%, rgba(34,211,238,.4), transparent 70%),
            radial-gradient(200px 100px at 80% 20%, rgba(99,102,241,.35), transparent 70%),
            linear-gradient(135deg, #0b1222, #0e1a2f 60%, #0a1326);
          position:relative;
        }
        .thumb::after{
          content:""; position:absolute; inset:auto 12px 12px auto;
          width:100px; height:36px; border-radius:8px;
          background: repeating-linear-gradient(90deg, rgba(255,255,255,.22) 0 6px, transparent 6px 12px);
          opacity:.35; filter: blur(.6px);
          transform: skewX(-12deg);
        }
        .badge{
          position:absolute; top:12px; left:12px;
          padding:6px 10px; border-radius:10px; font-size:12px; font-weight:700;
          background: rgba(16,185,129,.16); color: var(--good); backdrop-filter: blur(6px);
          border:1px solid rgba(16,185,129,.35);
        }
        .content{padding:14px 14px 12px}
        .title{
          display:flex; align-items:center; gap:8px; margin-bottom:6px;
          font-weight:700; font-size:16px;
        }
        .meta{
          display:flex; flex-wrap:wrap; gap:10px;
          color:var(--muted); font-size:13px; margin-bottom:10px;
        }
        .pill{
          padding:6px 9px; border:1px dashed rgba(255,255,255,.18);
          border-radius:10px; background: rgba(255,255,255,.03);
        }
        .price{
          margin-left:auto; font-weight:700; color:#fff;
          background: linear-gradient(90deg, #93c5fd, #a7f3d0);
          -webkit-background-clip:text; background-clip:text; color:transparent;
        }
        .actions{
          display:flex; gap:8px; margin-top:8px;
        }
        .ghost{
          border:1px solid var(--border);
          background: rgba(255,255,255,.02);
          color:#dbeafe;
        }
        .ghost:hover{border-color: rgba(34,211,238,.6); color:#fff}

        .hidden{display:none}

        /* Modal */
        .modal.backdrop{
          position:fixed; inset:0; background: rgba(0,0,0,.5);
          display:flex; align-items:center; justify-content:center; z-index:90;
        }
        .modal.card{
          width: min(560px, 92vw);
          grid-column: auto;
        }
        .modal .content{padding:18px}
        .modal h3{margin:0 0 8px}
        .modal .slots{display:flex; flex-wrap:wrap; gap:8px; margin:8px 0 14px}
        .slot{
          padding:8px 10px; border-radius:10px; border:1px solid var(--border);
          background: rgba(255,255,255,.03); cursor:pointer; color:#fff; font-weight:600; font-size:13px;
        }
        .slot.active{border-color: rgba(59,130,246,.6); background: rgba(59,130,246,.18)}

        /* Light mode toggle (class: light) */
        body.light{
          --bg:#f6f8ff;
          --card:#ffffff;
          --glass:rgba(0,0,0,.04);
          --text:#0b1220;
          --muted:#4b5565;
          --border:rgba(0,0,0,.12);
          background:
            radial-gradient(1200px 600px at 10% 0%, #eef3ff 0%, var(--bg) 60%),
            radial-gradient(900px 500px at 90% 100%, #f2f6ff 0%, var(--bg) 60%);
        }
        body.light .subtitle{color:#5b6475}
        body.light .badge{color:#0f766e; background: rgba(16,185,129,.12); border-color: rgba(16,185,129,.28)}
        body.light .pill{background:#f9fafb; border-color:#e5e7eb}
        body.light .ghost{color:#0b1220}
    </style>
</head>
<body>
<header>
    <div class="shine"></div>
    <h1>Daftar Lapangan Futsal</h1>
    <p class="subtitle">Cari, bandingkan, dan booking lapangan futsal favoritmu. Desain neon yang halus, responsif, dan mantap untuk dipakai di website klub atau venue.</p>

    <div class="toolbar" id="filters">
        <div class="field">
            <input type="text" id="q" placeholder="Cari nama lapangan atau fasilitas (contoh: rumput sintetis, AC)" />
        </div>
        <div class="field">
            <select id="lokasi">
                <option value="">Semua lokasi</option>
                <option>Jakarta Pusat</option>
                <option>Jakarta Barat</option>
                <option>Jakarta Timur</option>
                <option>Jakarta Selatan</option>
                <option>Jakarta Utara</option>
                <option>Depok</option>
                <option>Tangerang</option>
                <option>Bekasi</option>
            </select>
        </div>
        <div class="field">
            <select id="lantai">
                <option value="">Jenis lantai</option>
                <option>Rumput sintetis</option>
                <option>Vinyl</option>
                <option>Interlock</option>
                <option>Parquet</option>
            </select>
        </div>
        <div class="field">
            <select id="harga">
                <option value="">Harga per jam</option>
                <option value="150">≤ 150k</option>
                <option value="250">≤ 250k</option>
                <option value="350">≤ 350k</option>
                <option value="500">≤ 500k</option>
            </select>
        </div>
        <button class="btn toggle" id="toggleTheme" aria-label="Toggle tema">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M12 3v2m0 14v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M3 12h2m14 0h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42" stroke="white" stroke-width="2" stroke-linecap="round"/></svg>
            Tema
        </button>
    </div>
</header>

<main>
    <section class="grid" id="list">
        <!-- Cards will be rendered here -->
    </section>
</main>

<!-- Modal Booking -->
<div id="modal" class="hidden">
    <div class="modal backdrop" role="dialog" aria-modal="true">
        <div class="card modal">
            <div class="thumb"></div>
            <div class="content">
                <h3 id="modalTitle">Booking Lapangan</h3>
                <p class="meta" id="modalMeta"></p>
                <div class="slots" id="slotList"></div>
                <div class="actions">
                    <button class="btn" id="confirmBooking">
                        <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M5 13l4 4L19 7" stroke="white" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
                        Konfirmasi
                    </button>
                    <button class="btn ghost" id="closeModal">Batal</button>
                </div>
            </div>
        </div>
    </div>
</div>

<script>
    // Data contoh lapangan (silakan ganti sesuai kebutuhan)
    const DATA = [
      {
        id:"LPG-01",
        nama:"Neon Arena Futsal",
        lokasi:"Jakarta Selatan",
        lantai:"Rumput sintetis",
        harga:250,
        rating:4.7,
        fasilitas:["AC","Locker","Shower","Café"],
        status:"Available",
        ukuran:"25 x 15 m",
        jam:["08:00","10:00","12:00","14:00","16:00","20:00"]
      },
      {
        id:"LPG-02",
        nama:"Metro Court 1",
        lokasi:"Jakarta Timur",
        lantai:"Vinyl",
        harga:180,
        rating:4.5,
        fasilitas:["Tribun mini","Toilet","Parkir luas"],
        status:"Available",
        ukuran:"28 x 16 m",
        jam:["09:00","11:00","13:00","15:00","19:00"]
      },
      {
        id:"LPG-03",
        nama:"Prime Futsal Bekasi",
        lokasi:"Bekasi",
        lantai:"Interlock",
        harga:220,
        rating:4.3,
        fasilitas:["Toilet","Mushola","Kantin"],
        status:"Available",
        ukuran:"26 x 15 m",
        jam:["08:00","12:00","14:00","18:00","21:00"]
      },
      {
        id:"LPG-04",
        nama:"Tangerang Sport Hub",
        lokasi:"Tangerang",
        lantai:"Vinyl",
        harga:320,
        rating:4.8,
        fasilitas:["AC","Scoreboard","Shower","Parkir luas"],
        status:"Limited",
        ukuran:"27 x 17 m",
        jam:["10:00","12:00","16:00","20:00","22:00"]
      },
      {
        id:"LPG-05",
        nama:"Central Futsal",
        lokasi:"Jakarta Pusat",
        lantai:"Parquet",
        harga:350,
        rating:4.6,
        fasilitas:["Locker","Shower","Café","Wifi"],
        status:"Limited",
        ukuran:"25 x 14 m",
        jam:["09:00","11:00","15:00","18:00"]
      },
      {
        id:"LPG-06",
        nama:"Utara Arena",
        lokasi:"Jakarta Utara",
        lantai:"Rumput sintetis",
        harga:160,
        rating:4.1,
        fasilitas:["Toilet","Parkir luas"],
        status:"Available",
        ukuran:"24 x 14 m",
        jam:["08:00","10:00","12:00","14:00","16:00"]
      },
      {
        id:"LPG-07",
        nama:"Barat Futsal Center",
        lokasi:"Jakarta Barat",
        lantai:"Interlock",
        harga:210,
        rating:4.4,
        fasilitas:["Café","Wifi","Scoreboard"],
        status:"Available",
        ukuran:"26 x 16 m",
        jam:["10:00","12:00","14:00","18:00","20:00"]
      },
      {
        id:"LPG-08",
        nama:"Depok Kickoff",
        lokasi:"Depok",
        lantai:"Vinyl",
        harga:190,
        rating:4.2,
        fasilitas:["Toilet","Kantin","Mushola"],
        status:"Available",
        ukuran:"25 x 15 m",
        jam:["08:00","10:00","13:00","17:00","19:00"]
      }
    ];

    const $ = (sel, root=document) => root.querySelector(sel);
    const $$ = (sel, root=document) => Array.from(root.querySelectorAll(sel));

    const listEl = $("#list");
    const qEl = $("#q");
    const lokasiEl = $("#lokasi");
    const lantaiEl = $("#lantai");
    const hargaEl = $("#harga");
    const toggleThemeBtn = $("#toggleTheme");

    let STATE = {
      q:"",
      lokasi:"",
      lantai:"",
      harga:""
    };

    function iconStar(){
      return '<svg width="16" height="16" viewBox="0 0 24 24" fill="#facc15"><path d="M12 .587l3.668 7.431 8.2 1.193-5.934 5.787 1.402 8.162L12 18.896l-7.336 3.964 1.402-8.162L.132 9.211l8.2-1.193L12 .587z"/></svg>';
    }
    function iconMap(){
      return '<svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M12 2l7 4v12l-7 4-7-4V6l7-4z" stroke="#93c5fd" stroke-width="1.6"/><circle cx="12" cy="12" r="2.8" fill="#22d3ee"/></svg>';
    }
    function iconFloor(){
      return '<svg width="16" height="16" viewBox="0 0 24 24" fill="none"><rect x="3" y="5" width="18" height="14" rx="2" stroke="#a3e635" stroke-width="1.6"/><path d="M3 12h18M9 5v14" stroke="#a3e635" stroke-width="1.2" opacity=".8"/></svg>';
    }
    function formatHarga(k){ return k >= 1000 ? (k/1000).toFixed(1) + "jt" : k + "k"; }

    function cardTemplate(d){
      return `
        <article class="card" data-id="${d.id}" data-lokasi="${d.lokasi}" data-lantai="${d.lantai}" data-harga="${d.harga}" data-fasilitas="${d.fasilitas.join(', ').toLowerCase()}">
          <div class="thumb">
            <span class="badge">${d.status}</span>
          </div>
          <div class="content">
            <div class="title">
              <span>${d.nama}</span>
              <span class="price">Rp ${formatHarga(d.harga)}</span>
            </div>
            <div class="meta">
              <span class="pill" title="Lokasi">${iconMap()} ${d.lokasi}</span>
              <span class="pill" title="Lantai">${iconFloor()} ${d.lantai}</span>
              <span class="pill" title="Ukuran">Ukuran: ${d.ukuran}</span>
              <span class="pill" title="Rating">${iconStar()} ${d.rating.toFixed(1)}</span>
            </div>
            <div class="meta">
              <span>Fasilitas:</span>
              ${d.fasilitas.map(f => `<span class="pill">${f}</span>`).join('')}
            </div>
            <div class="actions">
              <button class="btn" data-action="book">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M5 4h14v16H5z" stroke="white" stroke-width="2"/><path d="M8 2v4M16 2v4" stroke="white" stroke-width="2"/><path d="M5 9h14" stroke="white" stroke-width="2"/></svg>
                Booking
              </button>
              <button class="btn ghost" data-action="detail">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M12 5c-7 0-10 7-10 7s3 7 10 7 10-7 10-7-3-7-10-7zm0 10a3 3 0 1 1 0-6 3 3 0 0 1 0 6z" stroke="#a8b3cf" stroke-width="1.6"/></svg>
                Detail
              </button>
            </div>
          </div>
        </article>
      `;
    }

    function renderList(items){
      const html = items.map(cardTemplate).join("");
      listEl.innerHTML = html || `<div style="grid-column:1/-1; text-align:center; color:var(--muted); padding:40px">Tidak ada lapangan yang cocok dengan filter.</div>`;
    }

    function applyFilters(){
      const q = STATE.q.trim().toLowerCase();
      const hasil = DATA.filter(d => {
        const matchQ =
          !q ||
          d.nama.toLowerCase().includes(q) ||
          d.fasilitas.join(' ').toLowerCase().includes(q) ||
          d.lantai.toLowerCase().includes(q) ||
          d.lokasi.toLowerCase().includes(q);
        const matchLokasi = !STATE.lokasi || d.lokasi === STATE.lokasi;
        const matchLantai = !STATE.lantai || d.lantai === STATE.lantai;
        const matchHarga = !STATE.harga || d.harga <= Number(STATE.harga);
        return matchQ && matchLokasi && matchLantai && matchHarga;
      });
      renderList(hasil);
    }

    // Events
    qEl.addEventListener("input", e => { STATE.q = e.target.value; applyFilters(); });
    lokasiEl.addEventListener("change", e => { STATE.lokasi = e.target.value; applyFilters(); });
    lantaiEl.addEventListener("change", e => { STATE.lantai = e.target.value; applyFilters(); });
    hargaEl.addEventListener("change", e => { STATE.harga = e.target.value; applyFilters(); });

    // Theme toggle
    toggleThemeBtn.addEventListener("click", () => {
      document.body.classList.toggle("light");
    });

    // Delegate card actions
    listEl.addEventListener("click", (e) => {
      const btn = e.target.closest("button");
      if(!btn) return;
      const card = e.target.closest(".card");
      const id = card?.dataset.id;
      const item = DATA.find(x => x.id === id);
      const action = btn.dataset.action;
      if(action === "book"){
        openModal(item);
      } else if(action === "detail"){
        alert(`${item.nama}\nLokasi: ${item.lokasi}\nLantai: ${item.lantai}\nUkuran: ${item.ukuran}\nHarga: Rp ${formatHarga(item.harga)}/jam\nFasilitas: ${item.fasilitas.join(", ")}`);
      }
    });

    // Modal booking
    const modalRoot = $("#modal");
    const modalMeta = $("#modalMeta");
    const modalTitle = $("#modalTitle");
    const slotList = $("#slotList");
    const closeModalBtn = $("#closeModal");
    const confirmBookingBtn = $("#confirmBooking");

    let selectedSlot = null;
    let currentItem = null;

    function openModal(item){
      currentItem = item;
      selectedSlot = null;
      modalTitle.textContent = `Booking: ${item.nama}`;
      modalMeta.textContent = `${item.lokasi} • ${item.lantai} • Ukuran ${item.ukuran} • Rp ${formatHarga(item.harga)}/jam`;
      slotList.innerHTML = item.jam.map(j => `<button class="slot" data-time="${j}">${j}</button>`).join("");
      modalRoot.classList.remove("hidden");
    }
    function closeModal(){
      modalRoot.classList.add("hidden");
    }

    slotList.addEventListener("click", (e) => {
      const btn = e.target.closest(".slot");
      if(!btn) return;
      selectedSlot = btn.dataset.time;
      $$(".slot", slotList).forEach(b => b.classList.toggle("active", b === btn));
    });

    closeModalBtn.addEventListener("click", closeModal);
    modalRoot.addEventListener("click", (e) => {
      if(e.target.classList.contains("backdrop")) closeModal();
    });
    confirmBookingBtn.addEventListener("click", () => {
      if(!selectedSlot){
        alert("Pilih jam terlebih dahulu.");
        return;
      }
      closeModal();
      // Demo: kirim notifikasi sederhana
      const msg = `Booking berhasil!\n\nLapangan: ${currentItem.nama}\nJam: ${selectedSlot}\nLokasi: ${currentItem.lokasi}\nHarga: Rp ${formatHarga(currentItem.harga)}/jam`;
      setTimeout(() => alert(msg), 200);
    });

    // Initial
    renderList(DATA);
</script>
</body>
</html>
