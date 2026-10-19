## 1. Aktor dan Kedudukannya

| Aktor | Kedudukan | Tujuan terhadap sistem | Status |
|---|---|---|---|
| Civitas Akademika | Umum (general) | Melihat kalender akademik; mewariskan fungsi itu kepada Mahasiswa dan Dosen | Baru P4 |
| Mahasiswa | Khusus dari Civitas Akademika | Melihat kalender akademik (warisan); melihat jadwal kuliah, mengajukan KRS, mengunduh bukti, melihat KHS | Tetap P2/P3 |
| Dosen | Khusus dari Civitas Akademika | Melihat kalender akademik (warisan); menginput nilai mata kuliah yang diampu | Baru P4 |
| Admin Akademik | Tetap, di luar hierarki | Mengelola jadwal kuliah dan data mahasiswa | Tetap P2 |
| Dosen Wali | Tetap, di luar hierarki | Memproses keputusan KRS | Tetap P3 |

Catatan: Dosen Wali tidak dijadikan aktor khusus dari Dosen. Fungsinya berbeda
(memproses keputusan KRS, bukan menginput nilai), sehingga jika dijadikan anak Dosen
ia akan salah mewarisi SIA-UC08 Input Nilai Mata Kuliah.

## 2. Katalog Use Case Gabungan

| ID | Nama use case | Aktor terkait | Sumber kebutuhan | Status |
|---|---|---|---|---|
| SIA-UC01 | Lihat Jadwal Kuliah | Mahasiswa | SIA-R01 | Tetap (P2) |
| SIA-UC02 | Kelola Jadwal Kuliah | Admin Akademik | SIA-R02 | Tetap (P2) |
| SIA-UC03 | Ajukan KRS | Mahasiswa | SIA-R03 | Tetap (P3) |
| SIA-UC04 | Validasi KRS | — (disertakan SIA-UC03) | SIA-R04 | Tetap (P3) |
| SIA-UC05 | Unduh Bukti Pengajuan KRS | Mahasiswa | SIA-R05 | Tetap (P3) |
| SIA-UC06 | Proses Keputusan KRS | Dosen Wali | SIA-R06 | Tetap (P3) |
| SIA-UC07 | Lihat Kalender Akademik | Civitas Akademika (diwarisi Mahasiswa dan Dosen) | SIA-R07 | Baru (P4) |
| SIA-UC08 | Input Nilai Mata Kuliah | Dosen | SIA-R08 | Baru (P4) |
| SIA-UC09 | Lihat KHS | Mahasiswa | SIA-R09 | Baru (P4) |
| SIA-UC10 | Kelola Data Mahasiswa | Admin Akademik | SIA-R10, SIA-R11 | Baru (P4) — UC umum |
| SIA-UC11 | Tambah Data Mahasiswa | warisan SIA-UC10 | SIA-R11 | Baru (P4) — UC khusus |
| SIA-UC12 | Ubah Data Mahasiswa | warisan SIA-UC10 | SIA-R11 | Baru (P4) — UC khusus |
| SIA-UC13 | Hapus Data Mahasiswa | warisan SIA-UC10 | SIA-R11 | Baru (P4) — UC khusus |

## 3. Relasi yang Digunakan

### 3.1 Generalization aktor
- Mahasiswa → Civitas Akademika
- Dosen → Civitas Akademika

Fungsi yang diwarisi kedua aktor khusus: SIA-UC07 Lihat Kalender Akademik.

Asosiasi khusus (tidak diwarisi):
- Civitas Akademika: SIA-UC07
- Mahasiswa: SIA-UC01, SIA-UC03, SIA-UC05, SIA-UC09
- Dosen: SIA-UC08
- Admin Akademik: SIA-UC02, SIA-UC10
- Dosen Wali: SIA-UC06

Alasan: Mahasiswa dan Dosen sama-sama melihat kalender akademik, sehingga
asosiasi ke SIA-UC07 cukup digambar satu kali dari Civitas Akademika. Asosiasi
warisan tidak digambar ulang dari Mahasiswa maupun Dosen.

### 3.2 Generalization use case
- SIA-UC11 Tambah Data Mahasiswa → SIA-UC10 Kelola Data Mahasiswa
- SIA-UC12 Ubah Data Mahasiswa → SIA-UC10 Kelola Data Mahasiswa
- SIA-UC13 Hapus Data Mahasiswa → SIA-UC10 Kelola Data Mahasiswa

Perilaku pembeda:
- Tambah menghasilkan satu data mahasiswa baru.
- Ubah menghasilkan perubahan atribut data mahasiswa yang sudah ada.
- Hapus menghasilkan terhapusnya data mahasiswa yang tidak memiliki data akademik aktif.

### 3.3 Include dan extend (tetap dari Pertemuan 3)
- SIA-UC03 Ajukan KRS «include» SIA-UC04 Validasi KRS
- SIA-UC05 Unduh Bukti Pengajuan KRS «extend» SIA-UC03 Ajukan KRS
  - condition: [mahasiswa memilih unduh bukti]
  - extension point: Bukti pengajuan tersedia

### 3.4 Collaboration dan realization
| ID | Nama collaboration | Use case yang direalisasikan |
|---|---|---|
| SIA-CO01 | Input Nilai Mata Kuliah | SIA-UC08 Input Nilai Mata Kuliah |
| SIA-CO02 | Lihat KHS | SIA-UC09 Lihat KHS |

Alasan: kedua use case itu ditetapkan jobsheet sebagai use case utama yang
realisasinya ditunjukkan secara eksplisit.

## 4. Perbandingan Diagram Pertemuan 3 dan Pertemuan 4

| Kelompok | Isi |
|---|---|
| Tetap dari P2/P3 | Aktor Mahasiswa, Admin Akademik, Dosen Wali; SIA-UC01 sampai SIA-UC06; «include» SIA-UC03 ke SIA-UC04; «extend» SIA-UC05 ke SIA-UC03 beserta condition dan extension point; asosiasi Mahasiswa ke SIA-UC01, SIA-UC03, SIA-UC05; Admin Akademik ke SIA-UC02; Dosen Wali ke SIA-UC06 |
| Berubah | Tidak ada asosiasi yang dipindahkan. Perubahan hanya pada kerapian notasi: Mahasiswa dipastikan berada di luar batas sistem (tidak lagi menjadi anak elemen frame), garis «extend» yang menggantung disambungkan ke sumbernya, dan nama elips diseragamkan dengan katalog P4 |
| Ditambah P4 | Aktor Civitas Akademika dan Dosen; dua generalization aktor; SIA-UC07, SIA-UC08, SIA-UC09; SIA-UC10 beserta SIA-UC11, SIA-UC12, SIA-UC13 dan tiga generalization use case; collaboration SIA-CO01 dan SIA-CO02 beserta dua realization |

## 5. Pemetaan Nomor Use Case Lama ke Katalog P4

| Nama use case | Nomor pada tabel/deskripsi P3 | Nomor katalog P4 |
|---|---|---|
| Lihat Jadwal Kuliah | SIA-UC01 | SIA-UC01 |
| Kelola Jadwal Kuliah | SIA-UC04 | SIA-UC02 |
| Ajukan KRS | SIA-UC02 | SIA-UC03 |
| Validasi KRS | SIA-UC06 | SIA-UC04 |
| Unduh Bukti Pengajuan KRS | SIA-UC03 | SIA-UC05 |
| Proses Keputusan KRS | SIA-UC05 | SIA-UC06 |

Catatan: berkas P3 tidak mencantumkan ID use case secara eksplisit. Nomor UC02, UC03,
UC05, dan UC06 tercatat pada berkas deskripsi P3; nomor UC01 dan UC04 disimpulkan dari
urutan tabel Langkah 2 P3. Berkas P3 tidak diubah.

## 6. Daftar Hubungan Diagram

| Sumber | Hubungan | Tujuan |
|---|---|---|
| Civitas Akademika | Association | SIA-UC07 |
| Mahasiswa | Association | SIA-UC01 |
| Mahasiswa | Association | SIA-UC03 |
| Mahasiswa | Association | SIA-UC05 |
| Admin Akademik | Association | SIA-UC02 |
| Dosen Wali | Association | SIA-UC06 |
| Dosen | Association | SIA-UC08 |
| Mahasiswa | Association | SIA-UC09 |
| Admin Akademik | Association | SIA-UC10 |
| Mahasiswa | Generalization → | Civitas Akademika |
| Dosen | Generalization → | Civitas Akademika |
| SIA-UC03 | «include» | SIA-UC04 |
| SIA-UC05 | «extend» | SIA-UC03 |
| SIA-UC11 | Generalization → | SIA-UC10 |
| SIA-UC12 | Generalization → | SIA-UC10 |
| SIA-UC13 | Generalization → | SIA-UC10 |
| SIA-CO01 | Realization → | SIA-UC08 |
| SIA-CO02 | Realization → | SIA-UC09 |