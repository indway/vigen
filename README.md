# VIGEN (Video Generator Engine) Pro Edition

**Dari JSON ke video Shorts siap upload — otomatis, di HP kamu**

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Termux%20%7C%20Linux-green?style=flat-square)
![Formats](https://img.shields.io/badge/Format%20Konten-26-orange?style=flat-square)
![License](https://img.shields.io/badge/License-Commercial-red?style=flat-square)

```text
██╗   ██╗██╗ ██████╗ ███████╗███╗   ██╗
██║   ██║██║██╔════╝ ██╔════╝████╗  ██║
██║   ██║██║██║  ███╗█████╗  ██╔██╗ ██║
╚██╗ ██╔╝██║██║   ██║██╔══╝  ██║╚██╗██║
 ╚████╔╝ ██║╚██████╔╝███████╗██║ ╚████║
  ╚═══╝  ╚═╝ ╚═════╝ ╚══════╝╚═╝  ╚═══╝
```

---

> [!NOTE] 
> **THIS IS A PUBLIC SHOWCASE REPOSITORY**  
> Repository ini adalah bentuk showcase / demo dari kemampuan VIGEN.  
> *Source code engine utama bersifat private dan komersial.*

## Apa itu VIGEN?

**VIGEN** (Video Generator Engine) adalah sistem produksi konten video otomatis yang berjalan langsung di perangkat Android (via Termux) atau server Linux — tanpa langganan cloud, tanpa batas upload, dan sepenuhnya dikendalikan via command line.

Hanya dengan menyusun teks ke dalam file `JSON`, VIGEN akan memprosesnya otomatis menjadi puluhan video pendek (Shorts/Reels/TikTok) yang siap rilis ke semua platform.

```text
JSON konten  →  VIGEN Engine  →  MP4 video  →  Auto-upload
```

---

## 🔥 Fitur Utama

- **Zero Cloud Costs:** Jalan sepenuhnya secara lokal di Android/Termux atau PC yang sangat hemat biaya.
- **Bulk Rendering:** Hasilkan 10+ konten dalam hitungan menit secara otomatis di malam hari.
- **26 Format Konten Cerdas:** Bukan cuma sekadar teks ganti warna, VIGEN memiliki 26 layout dinamis sesuai topik (seperti *quotes*, *berita*, *highlight*, *fakta*, dll).
- **Gemini AI Integration:** Template otomatis terisi dari hasil pipeline AI, memastikan stok konten harian aman tanpa Anda harus mengetik semua caption sendiri.
- **Auto-Upload:** Terintegrasi langsung dengan API Facebook, Instagram Reels, dan YouTube Shorts.
- **Theme/Layout Switch:** Dukungan 4 custom layout (Classic, Minimal, Premium, Spacious) untuk beragam klien/niche channel.

---

## 🎨 26 Format Visual yang Didukung

VIGEN Pro dirancang dengan visual styling yang beragam untuk niche apa pun:
- **Konten Psikologi / Refleksi:** `quotes`, `punch`, `surat`, `dialog`, `skenario`
- **Data & Edukasi:** `fakta`, `statistik`, `definisi`, `ranking`
- **Komparasi:** `versus`, `sebelum_sesudah`, `kontra`
- **Interaktif:** `poll`, `meme`, `tips`, `peringatan`
- **Video Islami / Dakwah:** `quran`, `quote1`
- **Berita & Aktual:** `berita`, `highlight`

---

## 💻 Workflow / Cara Kerja (Contoh)

Walaupun repositori ini tidak menyertakan kode inti engine `render.py`, cara kerja sistemnya sangat sederhana:

### 1. Fetching Background Video otomatis
Sebelum merender, VIGEN dapat mengambil sumber video background secara otomatis.
```bash
python3 bg_fetcher.py --niche="nature, waterfall" --count=10
```
Script ini akan langsung mencari video kualitas HD, mengunduh, dan melakukan kompresi secara otomatis agar siap digunakan oleh engine.

### 2. Auto-Generate Konten via Gemini AI
Alih-alih menulis JSON manual, Anda bisa menggunakan modul AI.
```bash
python3 ai_generate.py "fakta psikologi overthinking" --count=5
```
Engine `ai_generate.py` akan menghubungi *Gemini AI API*, membuat ide konten, lalu menyusunnya secara otomatis ke dalam format JSON yang valid (contoh: antrian `data/pending.json`).

### 3. Memulai Rendering Video Secara Massal
Setelah data JSON dan aset background siap, developer hanya menjalankan perintah:
```bash
python3 render.py --all
```
Dalam hitungan detik, script secara *batch* otomatis me-render grafis kartu dan menggabungkannya dengan backgound menggunakan library FFmpeg. File output MP4 final akan tersimpan di direktori hasil.

### 4. Otomatisasi Upload & Scheduling
Script `upload.py` memastikan video MP4 langsung mengudara:
```bash
python3 upload.py --platform=yt --schedule=auto
```

---

## 📸 Demo Hasil VIGEN
Di repositori demo ini, kamu bisa melihat folder `demo/` untuk contoh hasil JSON vs MP4, dan `assets/` melihat layout rendering statis yang ada. *(Segera ditambahkan)*

---

<br>

<div align="center">

*Dimasak dari IndwayLabs*  
**Tertarik dengan lisensi VIGEN? Hubungi via <a href="mailto:indway@duck.com">indway@duck.com</a>    
atau via DM instagram <a href="https://instagram.com/indthatway">@indthatway</a> untuk informasi lebih lanjut!**

</div>
