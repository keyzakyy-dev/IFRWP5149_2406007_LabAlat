# Praktikum Analisis Berobjek — IFRWP5149

**NIM:** 2406007 — Sayyid Dzaky Farhan
**Kakas:** draw.io

**Kasus:**
- **LAB** — Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus (studi kasus terbimbing)
- **SIA** — Sistem Informasi Akademik (tugas praktik)

## Daftar Isi

- [Struktur folder](#struktur-folder)
- [Peta artefak per pertemuan](#peta-artefak-per-pertemuan)
  - [Pertemuan 1](#pertemuan-1--pengenalan-lingkungan-praktikum-dan-kakas)
  - [Pertemuan 2](#pertemuan-2--notasi-use-case-dasar)
  - [Pertemuan 3](#pertemuan-3--use-case-diagram-includeextend-dan-asosiasi)
  - [Pertemuan 4](#pertemuan-4--use-case-lanjutan-generalization-dan-collaboration)
  - [Pertemuan 5](#pertemuan-5--tabel-skenario-use-case)
  - [Pertemuan 6](#pertemuan-6--activity-diagram)
- [Status / catatan tertunda](#status--catatan-tertunda)

Keterangan status: ✅ selesai / sudah diperiksa; ⬜ belum selesai.

## Struktur folder

| Folder | Isi |
|---|---|
| `00_administrasi/` | Logbook per pertemuan (`P0N_2406007_logbook_v01.md`) |
| `01_skenario/` | Orientasi kasus, skenario, dan kebutuhan per pertemuan per kasus |
| `02_template/` | Metadata artefak per pertemuan |
| `03_latihan_tools/P0N/{LAB,SIA}/` | Diagram latihan (drawio + PNG) dan deskripsi use case |
| `04_model_analisis/P0N/{LAB,SIA}/` | Model analisis: tabel hubungan, diagram kumulatif, tabel skenario, activity diagram |
| `06_laporan/` | Laporan singkat dan review jobsheet |

## Peta artefak per pertemuan

### Pertemuan 1 — Pengenalan lingkungan praktikum dan kakas

| Item | Berkas | Status |
|---|---|---|
| Latihan activity diagram | `03_latihan_tools/P01/P01_2406007_latihan_activity_v01.drawio` + `.png` | ✅ |
| Orientasi kasus | `01_skenario/S-ORI-01_orientasi_kasus_v01.md` | ✅ |
| Metadata | `02_template/P01_metadata_artefak_v01.md` | ✅ |
| Logbook | `00_administrasi/P01_2406007_logbook_v01.md` | ✅ (9/9) |
| Laporan singkat | `06_laporan/P01_2406007_laporan_singkat_v01.md` | ✅ |

### Pertemuan 2 — Notasi use case dasar

| Item | Berkas | Status |
|---|---|---|
| Skenario | `01_skenario/P02_LAB_skenario_v01.md`, `01_skenario/P02_SIA_skenario_v01.md` | ✅ |
| Notasi use case LAB | `03_latihan_tools/P02/LAB/P02_2406007_LAB_notasi_usecase_v01.drawio` | ⬜ (belum ada ekspor PNG) |
| Metadata | `02_template/P02_metadata_artefak_v01.md` | ✅ |
| Review jobsheet | `06_laporan/P02_2406007_jobsheet_review_v01.md` (4 temuan) | ✅ |
| Logbook | `00_administrasi/P02_2406007_logbook_v01.md` | ⬜ (ekspor PNG dan koreksi SIA) |

### Pertemuan 3 — Use case diagram: include/extend dan asosiasi

| Item | Berkas | Status |
|---|---|---|
| Skenario | `01_skenario/P03_LAB_skenario_v01.md`, `01_skenario/P03_SIA_skenario_v01.md` | ✅ |
| Diagram & deskripsi | `03_latihan_tools/P03/{LAB,SIA}/` | ✅ (deskripsi LAB & SIA terisi) |
| Model analisis | `04_model_analisis/P03/LAB/P03_2406007_LAB_model_analisis_v01.md`, `04_model_analisis/P03/SIA/P03_2406007_SIA-model_analisis_v01.md` | ⬜ (kolom tujuan SIA masih pakai ID kebutuhan) |
| Review jobsheet | `06_laporan/P03_2406007_jobsheet_review_v01.md` (4 temuan) | ✅ |
| Logbook | `00_administrasi/P03_2406007_logbook_v01.md` | ✅ (A13/B11 tuntas) |

### Pertemuan 4 — Use case lanjutan: generalization dan collaboration

| Item | Berkas | Status |
|---|---|---|
| Skenario & kebutuhan | `01_skenario/P04_{LAB,SIA}_skenario_v01.md`, `01_skenario/P04_{LAB,SIA}_kebutuhan_v01.md` | ✅ |
| Diagram kumulatif & deskripsi | LAB: `04_model_analisis/P04/LAB/P04_2406007_LAB_usecase_v01.drawio` + PNG. SIA: `03_latihan_tools/P04/SIA/P04_2406007_SIA_usecase_v01.drawio` + PNG | ✅ (folder `04_model_analisis/P04/SIA/` masih kosong) |
| Metadata | `02_template/P04_metadata_artefak_v01.md` | ✅ |
| Logbook | `00_administrasi/P04_2406007_logbook_v01.md` | ✅ (LAB 19/19, SIA 13/13) |

### Pertemuan 5 — Tabel skenario use case

| Item | Berkas | Status |
|---|---|---|
| Skenario LAB (indeks) | `01_skenario/P05_2406007_LAB_skenario_v01.md` | ⬜ (baru indeks, belum termuat tabel lengkap) |
| Skenario SIA | `01_skenario/P05_2406007_SIA_skenario_v01.md` | ✅ |
| Tabel skenario lengkap | `04_model_analisis/P05/LAB/P05_2406007_LAB_skenario_v01.drawio`, `04_model_analisis/P05/SIA/P05_2406007_SIA_skenario_v01.drawio` | ✅ |
| Metadata | `02_template/P05_metadata_artefak_v01.md` | ✅ |
| Logbook | `00_administrasi/P05_2406007_logbook_v01.md` | ⬜ (A11, A12) |

### Pertemuan 6 — Activity diagram

| Item | Berkas | Status |
|---|---|---|
| Activity LAB (7 diagram) | `04_model_analisis/P06/LAB/` — `lihat_ketersediaan`, `peminjaman`, `keputusan`, `cetak_bukti`, `kelola_data`, `laporan`, `pengembalian` | ⬜ (branch `[tidak tersedia]`; PNG sebagian perlu regen) |
| Activity SIA (7 diagram) | `04_model_analisis/P06/SIA/` — `lihat_kalender`, `input_nilai`, `lihat_khs`, `kelola_data`, `tambah_data`, `ubah_data`, `hapus_data` (satu diagram per berkas) | ✅ |
| Metadata | `02_template/P06_metadata_artefak_v01.md` | ✅ |
| Logbook | `00_administrasi/P06_2406007_logbook_v01.md` | ⬜ (A10, A11) |

## Status / catatan tertunda

- **Branch `[tidak tersedia]`** diagram lihat ketersediaan LAB masih menyalin teks aksi cabang `[tersedia]`.
- **Skenario alternatif/akhir LAB-UC04** di tabel P05 masih menyalin teks UC01.
- **Tabel skenario LAB** belum dimuat ke `01_skenario/P05_2406007_LAB_skenario_v01.md` (baru indeks; tabel lengkap ada di drawio).
- **PNG LAB** (keputusan, kelola data, peminjaman) perlu diekspor ulang dari sumber terkini setelah koreksi label.
- **Diagram P03 LAB** masih memakai label "Proses **Kebutuhan** Peminjaman" dan aktor "Petugas/Kepala **Laboran**" (sudah diperbaiki pada P04).
- **Kolom tujuan model analisis SIA P03** masih memakai ID kebutuhan (SIA-R01, …) alih-alih nama/ID use case.
- Setiap diagram LAB/SIA sudah memiliki padanan PNG; nama berkas keputusan sudah dinormalisasi.
