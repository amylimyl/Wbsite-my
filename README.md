# Wbsite-my
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Pengenalan Diri & Catatan Deskripsi</title>
  <style>
    :root {
      --bg: #0f172a;
      --card: #111827;
      --text: #e5e7eb;
      --muted: #9ca3af;
      --accent: #22c55e;
      --danger: #ef4444;
      --border: #1f2937;
    }
    .light {
      --bg: #f8fafc;
      --card: #ffffff;
      --text: #0f172a;
      --muted: #475569;
      --accent: #16a34a;
      --danger: #dc2626;
      --border: #e2e8f0;
    }
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Liberation Sans", sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
    }
    header {
      padding: 24px;
      border-bottom: 1px solid var(--border);
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: sticky;
      top: 0;
      backdrop-filter: blur(6px);
      background: color-mix(in oklab, var(--bg) 85%, transparent);
      z-index: 10;
    }
    header h1 {
      margin: 0;
      font-size: 1.25rem;
      letter-spacing: 0.2px;
    }
    .container {
      max-width: 980px;
      margin: 24px auto;
      padding: 0 16px;
    }
    .grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
    }
    @media (max-width: 860px) {
      .grid { grid-template-columns: 1fr; }
    }
    .card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 18px;
      box-shadow: 0 10px 24px rgba(0,0,0,0.15);
    }
    .card h2 {
      margin: 0 0 12px;
      font-size: 1.1rem;
    }
    .row { display: grid; grid-template-columns: 140px 1fr; gap: 12px; align-items: center; }
    .row + .row { margin-top: 10px; }
    label { color: var(--muted); font-size: 0.9rem; }
    input[type="text"], input[type="url"], textarea, select {
      width: 100%;
      padding: 10px 12px;
      border-radius: 10px;
      border: 1px solid var(--border);
      background: color-mix(in oklab, var(--card) 92%, black 8%);
      color: var(--text);
      outline: none;
    }
    textarea { min-height: 110px; resize: vertical; }
    .actions { display: flex; gap: 10px; margin-top: 12px; }
    button {
      padding: 10px 14px;
      border-radius: 10px;
      border: 1px solid var(--border);
      background: color-mix(in oklab, var(--card) 92%, black 8%);
      color: var(--text);
      cursor: pointer;
    }
    .btn-primary { background: var(--accent); border-color: color-mix(in oklab, var(--accent) 70%, black 30%); color: #062b16; }
    .btn-danger { background: var(--danger); border-color: color-mix(in oklab, var(--danger) 70%, black 30%); color: #fff; }
    .btn-ghost { background: transparent; }
    .profile {
      display: grid; grid-template-columns: 120px 1fr; gap: 16px; align-items: start;
    }
    .avatar {
      width: 120px; height: 120px; border-radius: 14px; border: 1px solid var(--border);
      background: linear-gradient(135deg, #1f2937, #0b1220);
      display: grid; place-items: center; color: var(--muted); font-size: 0.85rem; overflow: hidden;
    }
    .avatar img { width: 100%; height: 100%; object-fit: cover; display: block; }
    .muted { color: var(--muted); }
    .list { display: grid; gap: 12px; }
    .note {
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 12px;
      background: color-mix(in oklab, var(--card) 92%, black 8%);
    }
    .note h3 { margin: 0 0 6px; font-size: 1rem; }
    .note p { margin: 0; white-space: pre-wrap; }
    .note .meta { display: flex; justify-content: space-between; align-items: center; margin-top: 8px; color: var(--muted); font-size: 0.85rem; }
    .note .tools { display: flex; gap: 8px; }
    .toolbar { display: flex; gap: 10px; align-items: center; }
    .search { flex: 1; }
    .empty {
      border: 1px dashed var(--border);
      border-radius: 12px;
      padding: 16px;
      text-align: center;
      color: var(--muted);
    }
    .toggle {
      display: inline-flex; align-items: center; gap: 8px;
      padding: 8px 12px; border-radius: 999px; border: 1px solid var(--border);
      background: color-mix(in oklab, var(--card) 92%, black 8%);
      font-size: 0.9rem;
    }
    .footer { text-align: center; color: var(--muted); padding: 24px 0; }
    a { color: var(--accent); text-decoration: none; }
    a:hover { text-decoration: underline; }
  </style>
</head>
<body>
  <header>
    <h1>Pengenalan Diri & Catatan</h1>
    <button id="themeToggle" class="toggle" aria-label="Ubah tema">🌙 Tema</button>
  </header>

  <main class="container">
    <div class="grid">
      <!-- Profil -->
      <section class="card" aria-labelledby="profil-title">
        <h2 id="profil-title">Profil singkat</h2>
        <div class="profile">
          <div class="avatar" id="avatarPreview">Foto<br/>profil</div>
          <div>
            <div class="row">
              <label for="name">Nama</label>
              <input type="text" id="name" placeholder="Tulis nama kamu" />
            </div>
            <div class="row">
              <label for="role">Profesi</label>
              <input type="text" id="role" placeholder="Misal: Mahasiswa, Desainer, Developer" />
            </div>
            <div class="row">
              <label for="photo">URL Foto</label>
              <input type="url" id="photo" placeholder="https://..." />
            </div>
            <div class="row">
              <label for="bio">Bio</label>
              <textarea id="bio" placeholder="Ceritakan dirimu secara singkat..."></textarea>
            </div>
            <div class="actions">
              <button class="btn-primary" id="saveProfile">Simpan profil</button>
              <button class="btn-ghost" id="clearProfile">Reset</button>
            </div>
            <p class="muted" id="profileStatus"></p>
          </div>
        </div>
      </section>

      <!-- Tambah catatan -->
      <section class="card" aria-labelledby="catatan-title">
        <h2 id="catatan-title">Catatan deskripsi</h2>
        <div class="row">
          <label for="noteTitle">Judul</label>
          <input type="text" id="noteTitle" placeholder="Judul catatan" />
        </div>
        <div class="row">
          <label for="noteBody">Deskripsi</label>
          <textarea id="noteBody" placeholder="Tulis deskripsi, ide, atau refleksi..."></textarea>
        </div>
        <div class="actions">
          <button class="btn-primary" id="addNote">Tambah catatan</button>
          <button class="btn-ghost" id="resetNote">Bersihkan</button>
        </div>
        <p class="muted" id="noteStatus"></p>
      </section>
    </div>

    <!-- Daftar catatan -->
    <section class="card" style="margin-top:20px" aria-labelledby="daftar-title">
      <div class="toolbar">
        <h2 id="daftar-title" style="margin:0">Daftar catatan</h2>
        <input class="search" type="text" id="search" placeholder="Cari judul/deskripsi..." />
        <button id="exportNotes">Ekspor JSON</button>
        <button class="btn-danger" id="clearNotes">Hapus semua</button>
      </div>
      <div id="notesList" class="list" aria-live="polite"></div>
      <div id="emptyState" class="empty" hidden>Belum ada catatan. Tambahkan sesuatu yang berarti buat kamu.</div>
    </section>

    <section class="footer">
      Dibuat sederhana—semua data disimpan di perangkat kamu (localStorage).
    </section>
  </main>

  <script>
    // Tema
    const themeToggle = document.getElementById('themeToggle');
    const applyTheme = (t) => {
      document.documentElement.classList.toggle('light', t === 'light');
      themeToggle.textContent = t === 'light' ? '☀️ Tema' : '🌙 Tema';
      localStorage.setItem('theme', t);
    };
    const savedTheme = localStorage.getItem('theme') || 'dark';
    applyTheme(savedTheme);
    themeToggle.addEventListener('click', () => {
      const next = document.documentElement.classList.contains('light') ? 'dark' : 'light';
      applyTheme(next);
    });

    // Profil
    const nameEl = document.getElementById('name');
    const roleEl = document.getElementById('role');
    const photoEl = document.getElementById('photo');
    const bioEl = document.getElementById('bio');
    const avatarPreview = document.getElementById('avatarPreview');
    const saveProfileBtn = document.getElementById('saveProfile');
    const clearProfileBtn = document.getElementById('clearProfile');
    const profileStatus = document.getElementById('profileStatus');

    const loadProfile = () => {
      const p = JSON.parse(localStorage.getItem('profile') || '{}');
      nameEl.value = p.name || '';
      roleEl.value = p.role || '';
      photoEl.value = p.photo || '';
      bioEl.value = p.bio || '';
      renderAvatar(p.photo);
    };
    const renderAvatar = (url) => {
      if (url) {
        avatarPreview.innerHTML = '';
        const img = document.createElement('img');
        img.src = url;
        img.alt = 'Foto profil';
        img.onerror = () => { avatarPreview.textContent = 'URL foto tidak valid'; };
        avatarPreview.appendChild(img);
      } else {
        avatarPreview.innerHTML = 'Foto<br/>profil';
      }
    };
    photoEl.addEventListener('input', (e) => renderAvatar(e.target.value));

    saveProfileBtn.addEventListener('click', () => {
      const profile = {
        name: nameEl.value.trim(),
        role: roleEl.value.trim(),
        photo: photoEl.value.trim(),
        bio: bioEl.value.trim(),
        updatedAt: new Date().toISOString()
      };
      localStorage.setItem('profile', JSON.stringify(profile));
      profileStatus.textContent = 'Profil disimpan.';
      setTimeout(() => profileStatus.textContent = '', 1500);
    });
    clearProfileBtn.addEventListener('click', () => {
      localStorage.removeItem('profile');
      loadProfile();
      profileStatus.textContent = 'Profil direset.';
      setTimeout(() => profileStatus.textContent = '', 1500);
    });

    // Catatan
    const noteTitle = document.getElementById('noteTitle');
    const noteBody = document.getElementById('noteBody');
    const addNoteBtn = document.getElementById('addNote');
    const resetNoteBtn = document.getElementById('resetNote');
    const noteStatus = document.getElementById('noteStatus');
    const notesList = document.getElementById('notesList');
    const emptyState = document.getElementById('emptyState');
    const searchEl = document.getElementById('search');
    const exportBtn = document.getElementById('exportNotes');
    const clearNotesBtn = document.getElementById('clearNotes');

    const getNotes = () => JSON.parse(localStorage.getItem('notes') || '[]');
    const setNotes = (notes) => localStorage.setItem('notes', JSON.stringify(notes));

    const renderNotes = () => {
      const q = (searchEl.value || '').toLowerCase();
      const notes = getNotes().filter(n =>
        n.title.toLowerCase().includes(q) || n.body.toLowerCase().includes(q)
      );
      notesList.innerHTML = '';
      if (notes.length === 0) {
        emptyState.hidden = false;
        return;
      }
      emptyState.hidden = true;
      notes.forEach(n => {
        const el = document.createElement('div');
        el.className = 'note';
        el.innerHTML = `
          <h3>${escapeHTML(n.title)}</h3>
          <p>${escapeHTML(n.body)}</p>
          <div class="meta">
            <span>Dibuat: ${formatDate(n.createdAt)} • Diperbarui: ${formatDate(n.updatedAt)}</span>
            <div class="tools">
              <button data-id="${n.id}" class="edit">Edit</button>
              <button data-id="${n.id}" class="btn-danger delete">Hapus</button>
            </div>
          </div>
        `;
        notesList.appendChild(el);
      });
    };

    const escapeHTML = (s) => s.replace(/[&<>"']/g, (c) => ({
      '&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'
    }[c]));

    const formatDate = (iso) => {
      const d = new Date(iso);
      return d.toLocaleString('id-ID', { dateStyle: 'medium', timeStyle: 'short' });
    };

    addNoteBtn.addEventListener('click', () => {
      const title = noteTitle.value.trim();
      const body = noteBody.value.trim();
      if (!title || !body) {
        noteStatus.textContent = 'Judul dan deskripsi tidak boleh kosong.';
        setTimeout(() => noteStatus.textContent = '', 1500);
        return;
      }
      const now = new Date().toISOString();
      const note = { id: crypto.randomUUID(), title, body, createdAt: now, updatedAt: now };
      const notes = getNotes();
      notes.unshift(note);
      setNotes(notes);
      noteTitle.value = '';
      noteBody.value = '';
      noteStatus.textContent = 'Catatan ditambahkan.';
      setTimeout(() => noteStatus.textContent = '', 1500);
      renderNotes();
    });

    resetNoteBtn.addEventListener('click', () => {
      noteTitle.value = '';
      noteBody.value = '';
    });

    notesList.addEventListener('click', (e) => {
      const btn = e.target.closest('button');
      if (!btn) return;
      const id = btn.dataset.id;
      if (btn.classList.contains('delete')) {
        const notes = getNotes().filter(n => n.id !== id);
        setNotes(notes);
        renderNotes();
      } else if (btn.classList.contains('edit')) {
        const notes = getNotes();
        const idx = notes.findIndex(n => n.id === id);
        if (idx === -1) return;
        const current = notes[idx];
        const newTitle = prompt('Edit judul:', current.title);
        if (newTitle === null) return;
        const newBody = prompt('Edit deskripsi:', current.body);
        if (newBody === null) return;
        notes[idx] = { ...current, title: newTitle.trim(), body: newBody.trim(), updatedAt: new Date().toISOString() };
        setNotes(notes);
        renderNotes();
      }
    });

    searchEl.addEventListener('input', renderNotes);

    exportBtn.addEventListener('click', () => {
      const data = JSON.stringify(getNotes(), null, 2);
      const blob = new Blob([data], { type: 'application/json' });
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'catatan.json';
      a.click();
      URL.revokeObjectURL(url);
    });

    clearNotesBtn.addEventListener('click', () => {
      if (confirm('Hapus semua catatan?')) {
        localStorage.removeItem('notes');
        renderNotes();
      }
    });

    // Init
    loadProfile();
    renderNotes();
  </script>
</body>
</html>

