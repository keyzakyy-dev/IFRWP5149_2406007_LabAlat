### a. SIA-UC08 - Input Nilai Mata Kuliah

| Elemen | Deskripsi |
|---|---|
| ID dan nama | SIA-UC08: Input Nilai Mata Kuliah |
| Sumber kebutuhan | SIA-R08, SIA-R12 |
| Tujuan | Nilai mata kuliah yang diampu oleh dosen terekam di sistem dan dapat ditampilkan pada KHS setelah dipublikasikan |
| Aktor utama | Dosen |
| Pemicu | Dosen memilih fungsi input nilai dan menentukan mata kuliah yang diampu |
| Prasyarat | Dosen telah terautentikasi; mata kuliah terpilih adalah mata kuliah yang diampu dosen tersebut; masa perkuliahan selesai; nilai sesuai rentang 0–100 (asumsi, lihat pertanyaan terbuka) |
| Pascakondisi berhasil | Nilai tersimpan dengan status "belum dipublikasikan"; tidak langsung tampil di KHS |
| Pascakondisi gagal | Tidak ada nilai yang tersimpan; sistem menampilkan alasan penolakan |
| Generalization | Tidak ada (SIA-UC08 bukan bentuk khusus dari use case lain) |
| Collaboration | SIA-CO01: Input Nilai Mata Kuliah |

**Alur utama**

| Langkah | Tindakan dosen | Respons sistem |
|---|---|---|
| 1 | Memilih mata kuliah yang diampu | Menampilkan daftar mata kuliah yang diampu; menampilkan data mahasiswa pendaftar |
| 2 | Mengisi nilai akhir per mahasiswa (0–100) | Memvalidasi rentang nilai |
| 3 | Tidak ada | Menolak nilai di luar rentang, menampilkan pesan kesalahan, nilai tidak tersimpan |
| 4 | Menyimpan | Menyimpan nilai dengan status "belum dipublikasikan" |
| 5 | Melihat konfirmasi | Menampilkan ringkasan nilai yang tersimpan |

**Alur alternatif atau pengecualian**

- A1: Nilai di luar rentang 0–100 (langkah 2): sistem menolak, nilai tidak tersimpan. Pascakondisi gagal berlaku.
- A2: Mata kuliah terpilih bukan yang diampu dosen (langkah 1): sistem menolak akses, pascakondisi gagal berlaku.

### b. SIA-UC09 - Lihat KHS (deskripsi ringkas)

| Elemen | Deskripsi |
|---|---|
| ID dan nama | SIA-UC09: Lihat KHS |
| Sumber kebutuhan | SIA-R09, SIA-R12 |
| Tujuan | Mahasiswa dapat melihat Kartu Hasil Studi untuk semester yang nilainya sudah dipublikasikan |
| Aktor utama | Mahasiswa |
| Pemicu | Mahasiswa memilih semester dan membuka KHS |
| Prasyarat | Mahasiswa telah terautentikasi; semester dipilih memiliki minimal satu nilai yang sudah dipublikasikan |
| Pascakondisi berhasil | KHS tampil berisi mata kuliah dan nilai yang sudah dipublikasikan |
| Pascakondisi gagal | Tidak ada nilai terpublikasi untuk semester tersebut, sistem menampilkan pesan bahwa KHS belum tersedia |
| Generalization | Tidak ada |
| Collaboration | SIA-CO02: Lihat KHS |