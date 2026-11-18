# Pemuda Code

<p align="center">
  <img src="assets/pemuda-mark.png" alt="Pemuda Code Logo" width="128" height="128" />
</p>

<p align="center">
  <strong>Desktop AI Coding Agent dengan Otonomi Lokal, Dukungan Multi-Model, dan Isolasi Kerja Terverifikasi.</strong>
</p>

<p align="center">
  <a href="https://github.com/ramonhd/pemuda-code-releases/releases/latest">
    <img src="https://img.shields.io/github/v/release/ramonhd/pemuda-code-releases?color=6366f1&label=Release" alt="Latest Release" />
  </a>
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-blue" alt="Platform Support" />
  <img src="https://img.shields.io/badge/Architecture-Full%20Electron-success" alt="Full Electron" />
  <img src="https://img.shields.io/badge/Tests-593%20passed-green" alt="Tests Passed" />
  <img src="https://img.shields.io/badge/Security-OS%20SafeStorage-red" alt="Security" />
</p>

---

## ðŸŒŸ Apa itu Pemuda Code?

**Pemuda Code** adalah aplikasi desktop *coding agent* berbasis **Full Electron** yang bekerja langsung di dalam repositori kode lokal Anda. Pemuda Code menghubungkan model penalaran AI mutakhir (Claude 3.7 / 3.5 Sonnet, DeepSeek V4, Qwen 2.5 Coder, GPT-4o, Gemini 2.0 Flash, Kimi K2, dll.) dengan alat kerja nyata di lingkungan lokal pengguna (pembacaan file, modifikasi presisi, pencarian AST, terminal shell PTY terisolasi, dan diagnosa kode).

---

## ðŸš€ Fitur Unggulan

### 1. ðŸ§­ Interactive Agent Steering
- **`ask_questions`**: Agen dapat menanyakan keputusan ambigu atau pilihan arsitektur secara terstruktur dengan pilihan opsi dan input kustom sebelum melanjutkan pekerjaan.
- **`exit_plan`**: Mode Perencanaan (*Plan Mode*) menyajikan rencana kerja lengkap dalam format markdown, dengan tombol **ðŸš€ Setujui & Bangun** yang otomatis beralih ke Mode Pengerjaan (*Build Mode*).

### 2. ðŸ” Context Management & Diagnostics
- **`fetch_web_content`**: Mengambil dokumentasi resmi, referensi API, atau changelog dari web publik dengan proteksi ketat dari SSRF (Private IP blocking).
- **`git_diff`**: Agen dan pengguna dapat memeriksa perubahan kode (*working tree* vs *staged*) secara langsung.
- **`code_diagnostics`**: Memeriksa sintaks dan mendeteksi kesalahan *parse* kode secara instan dan *offline* menggunakan Tree-sitter WASM.

### 3. â¬¡ Multi-Agent Orchestration & Observability
- Mendekomposisi satu permintaan kompleks menjadi graf tugas (*Task DAG*).
- Menugaskan peran spesialis (*Architect*, *Coder*, *QA*, *Reviewer*).
- Eksekusi paralel di dalam **Git Worktree terisolasi**, lengkap dengan deteksi konflik dan *Pre-Merge Review Gate*.
- Panel visual interaktif dengan status live animasi dan *dual view* (Visual Graph vs Raw Logs).

### 4. âª Session Forking & File Checkpoints (Safety Net)
- **Automatic Turn Checkpoints**: Setiap modifikasi file oleh agen dicatat snapshot kondisinya. Pengguna dapat me-rewind file ke kondisi awal kapan saja.
- **Session Forking**: Mencabangkan percakapan dari pesan mana pun menjadi sesi baru tanpa kehilangan riwayat lama.

### 5. ðŸ“Œ Pinned Working Set (Compaction Immunity)
- Sematkan file-file inti proyek ke bar konteks di atas composer.
- File yang disematkan **kebal dari pemadatan konteks** (*Compaction Immunity*) saat percakapan melebihi 40.000 token.
- Daftar file otomatis disuntikkan ke dalam *system prompt* agen sebagai referensi prioritas utama.

### 6. âš¡ Custom Multi-Format Project Rules
- Mendukung pemuatan otomatis aturan proyek: `.pemudarules`, `.cursorrules`, `.windsurfrules`, `AGENTS.md`, `CLAUDE.md`, dan `SKILL.md`.
- Dilengkapi editor `.pemudarules` bawaan langsung di dalam modal pengaturan.

### 7. ðŸ›¡ï¸ Keamanan Lokal & Fail-Closed
- Kredensial disimpan terenkripsi melalui **OS Keychain / SafeStorage** (Windows DPAPI, macOS Keychain, Linux Secret Service).
- Tidak ada token yang dicetak di log.
- Loopback bridge server dilindungi dengan `X-Pemuda-Secret` injection dan penolakan origin asing.

---

## ðŸ“¥ Unduh & Instalasi

Unduh rilis installer terbaru dari [Halaman Rilis Resmi](https://github.com/ramonhd/pemuda-code-releases/releases/latest):

| Sistem Operasi | Paket Installer | Deskripsi |
|---|---|---|
| **Windows 10 / 11** | `Pemuda-Code-Setup.exe` | Standalone NSIS x64 Installer (Mendukung OTA auto-update) |
| **Windows Store** | `Pemuda Code.appx` | Paket aplikasi Microsoft Store / Partner Center |
| **Linux (Ubuntu/Debian)** | `pemuda-code_amd64.deb` | Paket Debian/Ubuntu x64 |
| **Linux (Universal)** | `Pemuda-Code.AppImage` | Standalone AppImage portable |

---

## ðŸ”‘ Mulai Menggunakan

1. Jalankan **Pemuda Code**.
2. Masuk ke menu **Account** di Settings, klik **ðŸŒ Masuk dengan Akun Pemuda AI**.
3. Selesaikan login di portal web, browser akan otomatis kembali ke aplikasi desktop.
4. Masukkan **API Key** Pemuda AI Anda di prompt atau tab Account.
5. Pilih folder proyek lokal Anda dan mulai berkolaborasi dengan agen koding!

---

## ðŸŒ Portal & Komunitas
- **Situs Resmi:** [https://pemuda.ai](https://pemuda.ai)
- **Portal & API Key:** [https://portal.pemuda.ai](https://portal.pemuda.ai)
- **Repositori Rilis:** [https://github.com/ramonhd/pemuda-code-releases](https://github.com/ramonhd/pemuda-code-releases)

---

*Hak Cipta Â© 2026 Pemuda AI. Seluruh hak cipta dilindungi undang-undang.*

