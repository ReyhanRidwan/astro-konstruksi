# Website Kontraktor Indonesia — Pure Astro Framework

Website profil perusahaan dan penawaran tender untuk kontraktor konstruksi Indonesia (**PT Mahakarya Bangun Nusantara**), dibangun sepenuhnya menggunakan framework **Astro** (Astro component `.astro`, zero-JS by default, MPA berkecepatan tinggi) tanpa framework React SPA.

> [!IMPORTANT]
> **Keputusan Kunci Sesuai Preferensi Pengguna**:
> - **Framework**: Pure **Astro** (`.astro` native components, Astro asset pipeline, Tailwind CSS) menggantikan setup awal React/Vite SPA.
> - **Kategori Bisnis**: Kontraktor Umum & Spesialis Konstruksi Indonesia (Gedung Komersial, Sipil/Infrastruktur, Pabrik/Gudang, dan Desain-Bangun).
> - **Portabilitas & Standar AI Studio**: Menjalankan dev server Astro pada port 3000 (`astro dev --port 3000 --host 0.0.0.0`) dan build pipeline `astro build` yang terverifikasi.

---

### User Review & Critical Decisions

- **Framework Terpilih**: Pure Astro. Tidak menggunakan React runtime; seluruh halaman dan komponen (Header, Hero, Services, Portfolio, RAB Calculator, Contact) dirancang menggunakan komponen native Astro dengan skrip interaktif ringan untuk kalkulator RAB dan filter proyek.
- **Identitas Perusahaan**: PT Mahakarya Bangun Nusantara — Kontraktor Umum Terdaftar (Kualifikasi B2/Besar, ISO 9001:2015, Sertifikat SMK3).
- **Fitur Interaktif Utama**: 
  1. Filter Portofolio Proyek (Komersial, Infrastruktur, Industrial, Residensial).
  2. Kalkulator Estimasi Awal RAB (Rencana Anggaran Biaya) interaktif berdasarkan tipe proyek, luas m², dan spesifikasi material.
  3. Form Pengajuan Konsultasi & Permintaan Penawaran Tender (RFP) lengkap dengan validasi.

---

## 1. Overview & Core Concept

- **What It Does**: Memberikan platform kredibilitas tinggi bagi pemilik proyek, developer properti, BUMN, dan korporasi swasta untuk meninjau kapabilitas, rekam jejak, legalitas konstruksi (SBU & K3), serta menghitung estimasi anggaran awal pembangunan proyek mereka.
- **Target Audience / Persona**: 
  - Project Director / Pengembang Properti komersial dan residensial.
  - Manajer Operasional & Pengadaan (Procurement) industri yang membutuhkan pembangunan pabrik/gudang.
  - Pemilik bangunan komersial yang membutuhkan renovasi struktural dan arsitektural.
- **Key Value**: Skor performa 100/100 (Core Web Vitals) khas arsitektur Astro, navigasi ultra-responsif, tata visual arsitektural-industrial yang otoritatif, dan kemudahan mendapatkan estimasi biaya dalam hitungan detik.

---

## 2. User Experience & Visual Design

### A. Section Flow & Visual Storytelling
1. **Top Navigation Bar**: Memenuhi kontrak 3-zona (Wordmark brand teks tunggal, 4 tautan navigasi single-line tanpa bungkus pil, 1 tombol aksi utama: *"Konsultasi Proyek"*).
2. **Hero Section (Proposition & Trust)**:
   - Headline otoritatif: *"Membangun Fondasi Masa Depan Konstruksi Indonesia"*
   - Deskripsi komitmen kualitas, ketepatan waktu, dan standar keselamatan kerja K3.
   - 3 Metrik Terverifikasi: 140+ Proyek Selesai, 99.4% On-Time Delivery, 0 Fatal Accidents (Zero Accident Award).
3. **Layanan Unggulan (Core Capabilities)**:
   - `01. Konstruksi Gedung Bertingkat & Komersial` (Perkantoran, Mall, Hotel)
   - `02. Fasilitas Industri & Pergudangan` (Pabrik, Cold Storage, Steel Structure)
   - `03. Pekerjaan Sipil & Infrastruktur` (Jalan kawasan, jembatan, drainase makro)
   - `04. Design & Build / Manajemen Konstruksi` (Turnkey solution dari desain izin PBG hingga handover)
4. **Portofolio & Rekam Jejak (Proof of Impact)**:
   - Galeri proyek dengan filter kategori interaktif (Semua, Komersial, Industri, Sipil).
   - Setiap kartu menampilkan nilai proyek terukur, durasi pelaksanaan, luas lahan/bangunan, dan status serah terima.
5. **Kalkulator Estimasi RAB Mandiri (Interactive Feature)**:
   - Input: Kategori bangunan, perkiraan luas total ($m^2$), spesifikasi material (Standar SNI, Premium Korporat, Heavy Industrial).
   - Output: Estimasi rentang biaya (Rp/m² dan total estimasi) serta opsi ekspor ringkasan ke form konsultasi / WhatsApp tender.
6. **Sertifikasi, Legalitas & K3**:
   - Sertifikat Badan Usaha (SBU), ISO 9001:2015, ISO 14001, ISO 45001 (SMK3).
7. **Formulir Pengajuan Tender & Hubungi Kami**:
   - Field nama, perusahaan, nomor kontak/WhatsApp, jenis pekerjaan, perkiraan lokasi & luas.
8. **Footer**:
   - Alamat kantor pusat (Jakarta) & kantor operasional cabang (Surabaya/IKN), jam kerja, nomor legalitas NIB/SBU.

### B. Visual Identity & Theme
- **Aesthetic Direction**: *Industrial Architectural Authority* — tegas, kokoh, berbobot, terstruktur rapi dengan hairline borders (`border-neutral-200` / `border-neutral-800`), tanpa ornamen buatan atau gradien ungu generik.
- **Palet Warna (Aturan 60-30-10)**:
  - *60% Neutral Canvas*: Slate gelap pekat (`#0B132B`, `#0F172A`) atau off-white arsitektural seimbang.
  - *30% Structural Surfaces*: Deep steel slate (`#1E293B`, `#334155`) dengan border bergaris halus.
  - *10% Accent Intent*: Safety Amber & Construction Gold (`#F59E0B` / `#D97706`) untuk penanda aksi utama dan highlight metrik.
- **Tipografi**:
  - Headings: `Plus Jakarta Sans` / `Outfit` (bersih, proporsional, berwibawa).
  - Body: `Plus Jakarta Sans` (16px, 1.6 line height).
  - Angka & Metrik: `font-mono tabular-nums` untuk akurasi nominal rupiah dan dimensi teknis.

---

## 3. Key Product Decisions & Trade-Offs

- **Pure Astro Architecture vs React SPA**:
  - *Keputusan*: Menghapus dependensi React runtime di sisi browser dan beralih ke Astro MPA murni (`astro dev` dan `astro build`).
  - *Alasan*: Permintaan langsung pengguna ("Pure menggunakan framework astro, tanpa menggunakna react vite"). Website kontraktor berorientasi konten, kecepatan muat halaman instan, SEO terunggul untuk pencarian tender/kontraktor di Indonesia, dan zero JavaScript hydration bloat.
- **Interaktivitas Tanpa React Framework**:
  - *Keputusan*: Kalkulator RAB dan filter galeri proyek dijalankan menggunakan skrip vanilla ES module bawaan Astro `<script>` yang terisolasi dan super cepat.
  - *Alasan*: Menjamin website 100% pure Astro tanpa menyuntikkan React adapter atau virtual DOM berlebih.

---

## 4. Technical Architecture & Data Strategy

```
┌──────────────────────────────────────────────────────────┐
│                   Astro Application                      │
│                                                          │
│  src/pages/index.astro                                   │
│  ├── BaseLayout.astro (SEO Meta, Google Fonts, Tailwind) │
│  ├── Navbar.astro (Top Bar Contract 3-Zone)              │
│  ├── Hero.astro (Lead Value Prop & KPI Strip)            │
│  ├── ServicesBento.astro (4 Layanan Konstruksi)          │
│  ├── ProjectsGallery.astro (Filterable Case Studies)     │
│  ├── RabCalculator.astro (Client-Side Estimator Script)  │
│  ├── Certifications.astro (Legalitas, K3 & ISO)          │
│  ├── ContactSection.astro (Validated RFP Form)           │
│  └── Footer.astro (Legal, Alamat Kantor, Disclaimer)     │
└──────────────────────────────────────────────────────────┘
                            │
               ┌────────────┴────────────┐
               ▼                         ▼
      astro.config.mjs           package.json
   (Port 3000, Host 0.0.0.0)  ("dev": "astro dev --port 3000",
                               "build": "astro build")
```

### Data Model & State
1. **Layanan (`servicesData`)**: Daftar layanan lengkap dengan lingkup kerja, standar material, dan sertifikasi terkait.
2. **Portofolio Proyek (`projectsData`)**: Daftar proyek referensi nyata (Komersial, Industri, Infrastruktur) lengkap dengan lokasi, luas m², nilai pengerjaan, dan tahun penyelesaian.
3. **Kalkulator State**: Perhitungan rumus real-time:
   $$\text{Estimasi Total} = \text{Luas (m²)} \times \text{Tarif Dasar Kategori} \times \text{Koefisien Material}$$
   dengan output rentang anggaran (Min – Max) dan format mata uang Rupiah (`IDR`).

---

## 5. Rencana Langkah Eksekusi Setelah Persetujuan

1. **Instalasi Paket Astro**:
   - Menginstal `astro` dan plugin terkait via package manager.
2. **Konfigurasi Project Astro**:
   - Menyiapkan `astro.config.mjs` dengan konfigurasi server host `0.0.0.0` dan port `3000`.
   - Menyesuaikan `package.json` (`"dev": "astro dev --port 3000 --host 0.0.0.0"`, `"build": "astro build"`).
3. **Pembuatan Komponen & Struktur Halaman**:
   - `src/layouts/BaseLayout.astro`
   - `src/components/Navbar.astro`
   - `src/components/Hero.astro`
   - `src/components/Services.astro`
   - `src/components/Projects.astro`
   - `src/components/RabCalculator.astro`
   - `src/components/TrustCertifications.astro`
   - `src/components/ContactForm.astro`
   - `src/components/Footer.astro`
   - `src/pages/index.astro`
4. **Verifikasi & Build**:
   - Restart dev server dan jalankan verifikasi build menggunakan `compile_applet`.
