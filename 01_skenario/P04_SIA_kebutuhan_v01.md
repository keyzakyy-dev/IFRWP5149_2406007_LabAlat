## Skenario
Mahasiswa dan dosen sama-sama merupakan Civitas Akademika yang dapat melihat kalender akademik. Dosen menginput nilai mata kuliah yang diampunya setelah masa perkuliahan berakhir. Mahasiswa melihat Kartu Hasil Studi (KHS) untuk semester yang nilainya sudah dipublikasikan. Admin Akademik mengelola data mahasiswa: menambah data mahasiswa baru, mengubah data mahasiswa, dan menghapus data mahasiswa. Dua use case utama, Input Nilai Mata Kuliah dan Lihat KHS, ditunjukkan realisasinya oleh collaboration yang bersesuaian.

## Tabel Kebutuhan
| ID | Kebutuhan |
|---|---|
| SIA-R01, SIA-R02 | Kebutuhan Pertemuan 2 tetap berlaku dan tidak berubah arti (lihat Jobsheet Pertemuan 2). |
| SIA-R03 s.d. SIA-R06 | Kebutuhan Pertemuan 3 tetap berlaku dan tidak berubah arti (lihat Jobsheet Pertemuan 3). |
| SIA-R07 | Mahasiswa dan Dosen, sebagai Civitas Akademika, dapat melihat kalender akademik. |
| SIA-R08 | Dosen dapat menginput nilai mata kuliah yang diampunya. |
| SIA-R09 | Mahasiswa dapat melihat KHS untuk semester yang nilainya sudah dipublikasikan. |
| SIA-R10 | Admin Akademik dapat mengelola data mahasiswa. |
| SIA-R11 | Pengelolaan data mahasiswa terdiri dari tiga bentuk khusus: tambah, ubah, dan hapus data mahasiswa. |
| SIA-R12 | Model menunjukkan collaboration yang merealisasikan Input Nilai Mata Kuliah dan Lihat KHS. |

## Batas dan Asumsi
- Kode kebutuhan dimulai dari SIA-R07 agar SIA-R01 dan SIA-R02 (Pertemuan 2) serta SIA-R03 sampai SIA-R06 (Pertemuan 3) tetap mempunyai identitas berbeda.
- Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
- Kalender akademik adalah agenda resmi institusi (awal semester, batas KRS, masa ujian, dan sejenisnya); bukan jadwal kuliah Pertemuan 2.
- Nilai hanya dapat diinput oleh dosen pengampu mata kuliah tersebut.
- Nilai yang diinput belum terpublikasi sampai dinyatakan resmi; KHS hanya menampilkan nilai yang sudah dipublikasikan.
- Hapus Data Mahasiswa hanya untuk mahasiswa yang tidak memiliki data akademik aktif (ketentuan fiktif untuk latihan).
- Pengajuan KRS tetap digambar sebagai bagian diagram kumulatif Pertemuan 3.
- Pembayaran dan perancangan basis data berada di luar tugas ini.

## Pertanyaan Terbuka

| No | Pertanyaan | Alasan belum dimodelkan |
|---|---|---|
| 1 | Berapa rentang nilai yang sah (misalnya 0–100 atau A–E)? | Jobsheet tidak menetapkan skala nilai. Pada deskripsi dipakai asumsi rentang 0–100. |
| 2 | Siapa yang berwenang mempublikasikan nilai dan kapan? | Jobsheet hanya menyatakan KHS menampilkan nilai yang sudah dipublikasikan, tanpa menjelaskan mekanismenya. |
| 3 | Apakah Dosen Wali termasuk Civitas Akademika? | Jobsheet hanya menetapkan Mahasiswa dan Dosen sebagai aktor khusus Civitas Akademika. |
| 4 | Apakah Admin Akademik juga dapat melihat kalender akademik? | Tidak disebut pada skenario maupun Tabel 4.6. |

## Uji Konsistensi

### Situasi A — Mahasiswa melihat kalender akademik tanpa garis asosiasi langsung

Tetap benar. Mahasiswa adalah aktor khusus dari Civitas Akademika, sehingga mewarisi
asosiasi Civitas Akademika ke SIA-UC07 Lihat Kalender Akademik. Menggambar garis
langsung dari Mahasiswa justru melanggar aturan generalization aktor.

### Situasi B — Dosen yang bukan pengampu mencoba menginput nilai

Ditolak. Prasyarat "dosen adalah pengampu mata kuliah" tidak terpenuhi, sehingga use
case Input Nilai Mata Kuliah tidak berjalan. Sistem menampilkan penolakan, pascakondisi
gagal berlaku, dan tidak ada nilai yang tersimpan.

### Situasi C — Admin Akademik menghapus mahasiswa yang masih memiliki data akademik aktif

Ditolak. Aturan Hapus Data Mahasiswa hanya berlaku untuk mahasiswa tanpa data akademik
aktif. Data tidak terhapus dan sistem menampilkan alasan penolakan.