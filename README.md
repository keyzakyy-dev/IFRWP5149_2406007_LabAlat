# Praktikum Analisis Berobjek — IFRWP5149

**NIM:** 2406007 — Sayyid Dzaky Farhan
**Kakas:** draw.io
**Kasus:**
- **LAB** — Sistem Informasi Peminjaman dan Pengembalian Peralatan Laboratorium Kampus (studi kasus terbimbing)
- **SIA** — Sistem Informasi Akademik (tugas praktik)

## Struktur folder

| Folder | Isi |
|---|---|
| `00_administrasi/` | Logbook per pertemuan (`P0N_2406007_logbook_v01.md`). P01–P06 terisi; P02, P03, P05, dan P06 masih memiliki butir tunda (⬜) |
| `01_skenario/` | Orientasi kasus, skenario, dan kebutuhan per pertemuan per kasus |
| `02_template/` | Template metadata artefak (P01, P02, P04, P05, P06) |
| `03_latihan_tools/P0N/{LAB,SIA}/` | Diagram latihan (drawio + PNG) dan deskripsi use case per kasus |
| `04_model_analisis/P0N/{LAB,SIA}/` | Model analisis: tabel hubungan, diagram kumulatif, tabel skenario, activity diagram |
| `06_laporan/` | Laporan singkat dan review jobsheet |

## Peta artefak per pertemuan

### Pertemuan 1 — Pengenalan lingkungan praktikum dan kakas
| Item | Berkas |
|---|---|
| Latihan activity diagram | `03_latihan_tools/P01/P01_2406007_latihan_activity_v01.drawio` + `.png` (orientasi kasus: `01_skenario/S-ORI-01_orientasi_kasus_v01.md`) |
| Metadata | `02_template/P01_metadata_artefak_v01.md` |
| Logbook | `00_administrasi/P01_2406007_logbook_v01.md` (9/9 ✅) |
| Laporan singkat | `06_laporan/P01_2406007_laporan_singkat_v01.md` (**kosong**) |

### Pertemuan 2 — Notasi use case dasar
| Item | Berkas |
|---|---|
| Skenario | `01_skenario/P02_LAB_skenario_v01.md` (R01–R02), `01_skenario/P02_SIA_skenario_v01.md` |
| Notasi use case LAB | `03_latihan_tools/P02/LAB/P02_2406007_LAB_notasi_usecase_v01.drawio` (tanpa ekspor PNG) |
| Metadata | `02_template/P02_metadata_artefak_v01.md` |
| Review jobsheet | `06_laporan/P02_2406007_jobsheet_review_v01.md` (4 temuan) |
| Logbook | `00_administrasi/P02_2406007_logbook_v01.md` (ekspor PNG dan diagram koreksi SIA masih tunda ⬜) |

### Pertemuan 3 — Use case diagram: include/extend dan asosiasi
| Item | Berkas |
|---|---|
| Skenario | `01_skenario/P03_LAB_skenario_v01.md`, `01_skenario/P03_SIA_skenario_v01.md` |
| Diagram & deskripsi | `03_latihan_tools/P03/{LAB,SIA}/` — notasi use case (drawio + PNG) dan deskripsi use case (LAB **kosong**, SIA terisi) |
| Model analisis (tabel hubungan) | `04_model_analisis/P03/LAB/P03_2406007_LAB_model_analisis_v01.md`, `04_model_analisis/P03/SIA/P03_2406007_SIA-model_analisis_v01.md` |
| Review jobsheet | `06_laporan/P03_2406007_jobsheet_review_v01.md` (**kosong**) |
| Logbook | `00_administrasi/P03_2406007_logbook_v01.md` (deskripsi LAB, metadata, dan review jobsheet masih tunda ⬜) |

### Pertemuan 4 — Use case lanjutan: generalization dan collaboration
| Item | Berkas |
|---|---|
| Skenario & kebutuhan | `01_skenario/P04_{LAB,SIA}_skenario_v01.md`, `01_skenario/P04_{LAB,SIA}_kebutuhan_v01.md` (LAB-R07–R11, SIA-R07–R12) |
| Katalog & deskripsi use case | `03_latihan_tools/P04/{LAB,SIA}/` — use case diagram kumulatif (drawio + PNG) dan deskripsi use case |
| Diagram kumulatif | LAB: `04_model_analisis/P04/LAB/P04_2406007_LAB_usecase_v01.drawio` + PNG. SIA: `03_latihan_tools/P04/SIA/P04_2406007_SIA_usecase_v01.drawio` + PNG (folder `04_model_analisis/P04/SIA/` masih kosong) |
| Metadata | `02_template/P04_metadata_artefak_v01.md` |
| Logbook | `00_administrasi/P04_2406007_logbook_v01.md` (LAB 19/19 ✅, SIA 13/13 ✅) |

### Pertemuan 5 — Tabel skenario use case
| Item | Berkas |
|---|---|
| Skenario (indeks & telaah) | `01_skenario/P05_2406007_LAB_skenario_v01.md` (indeks 12 tabel studi kasus; SIA **kosong**) |
| Tabel skenario lengkap | `04_model_analisis/P05/LAB/P05_2406007_LAB_skenario_v01.drawio` (tabel skenario LAB), `04_model_analisis/P05/SIA/P05_2406007_SIA_skenario_v01.drawio` (tabel skenario SIA) |
| Logbook | `00_administrasi/P05_2406007_logbook_v01.md` |
| Metadata | `02_template/P05_metadata_artefak_v01.md` (**kosong**) |

### Pertemuan 6 — Activity diagram
| Item | Berkas (di `04_model_analisis/P06/`) |
|---|---|
| Activity LAB (7 diagram, drawio + PNG) | `LAB/P06_2406007_LAB_activity_…` — `lihat_ketersediaan`, `peminjaman`, `keputusan`, `cetak_bukti`, `kelola_data`, `laporan`, `pengembalian` |
| Activity SIA | `SIA/P06_2406007_SIA_activity_v01.drawio` (satu berkas, beberapa tahapan/L1–L4; ekspor `P06_2406007_SIA_activity_v01-L4.png`) |
| Metadata | `02_template/P06_metadata_artefak_v01.md` (SIA: swimlane 4 aktor, decision, fork/join) |
| Logbook | `00_administrasi/P06_2406007_logbook_v01.md` |

## Status / catatan tertunda

- Salah ketik label LAB dan SIA sudah dikoreksi di sumber drawio; PNG koreksi (3 diagram LAB + SIA L4) perlu diekspor ulang.
- Laporan singkat P01 dan review jobsheet P03 masih kosong.
- Skenario P05 SIA dan metadata P05 belum diisi.
- Tabel skenario LAB belum dimuat ke `01_skenario/P05_2406007_LAB_skenario_v01.md` (baru indeks; tabel lengkap ada di drawio).
- Skenario alternatif/akhir LAB-UC04 di tabel P05 masih menyalin teks UC01.
- Diagram P03 LAB memakai label "Proses **Kebutuhan** Peminjaman" (seharusnya *Keputusan*) — diperbaiki pada diagram P04.
- Nama aktor di diagram ("Petugas/Kepala **Laboran**") belum seragam dengan dokumen ("Petugas/Kepala **Laboratorium**").
- Setiap diagram LAB sudah memiliki padanan PNG; nama berkas keputusan sudah dinormalisasi.
