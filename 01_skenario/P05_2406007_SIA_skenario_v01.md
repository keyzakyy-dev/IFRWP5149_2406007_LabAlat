Studi kasus ini memakai diagram kumulatif Pertemuan 4 sebagai acuan. Kebutuhan SIA-R07 sampai SIA-R12 dan relasi pada diagram kumulatif P04 dirujuk dari Jobsheet Pertemuan 4; tidak ada kebutuhan baru dan tidak ada use case baru pada pertemuan ini. Tabel skenario SIA disusun untuk SIA-UC07 sampai SIA-UC13.

## SIA-UC07 — Lihat Kalender Akademik

| Elemen | Deskripsi |
|---|---|
| Aktor | Civitas Akademika (berlaku untuk Mahasiswa dan Dosen) |
| Tujuan | Civitas akademika dapat mengetahui jadwal kegiatan akademik pada periode tertentu |
| Deskripsi | Civitas Akademika membuka fungsi kalender akademik, memilih periode, dan melihat kalender akademik periode tersebut |

**Skenario normal**

| Langkah | Kegiatan | Respons sistem |
|---|---|---|
| 1 | Civitas Akademika membuka fungsi Lihat Kalender Akademik | Sistem menampilkan daftar periode akademik |
| 2 | Civitas Akademika memilih periode akademik | Sistem menampilkan kalender akademik periode tersebut beserta nama kegiatan dan tanggalnya |

**Skenario alternatif**

- A1 (cabang dari langkah 2): Kalender akademik periode yang dipilih belum tersedia → sistem menampilkan pesan kalender akademik periode tersebut belum tersedia.

**Skenario akhir**

Use case selesai jika kalender akademik periode yang dipilih ditampilkan; jika kalender belum tersedia, use case selesai dengan pesan tersebut.

## SIA-UC08 — Input Nilai Mata Kuliah

| Elemen | Deskripsi |
|---|---|
| Aktor | Dosen (dosen pengampu mata kuliah) |
| Tujuan | Nilai mahasiswa pada mata kuliah yang diampu tercatat dalam sistem |
| Deskripsi | Dosen memilih mata kuliah yang diampunya, mengisi nilai mahasiswa peserta, dan menyimpan nilai. Hanya dosen pengampu mata kuliah yang dapat menginput nilai |

**Skenario normal**

| Langkah | Kegiatan | Respons sistem |
|---|---|---|
| 1 | Dosen membuka fungsi Input Nilai Mata Kuliah | Sistem menampilkan daftar mata kuliah yang diampu dosen tersebut |
| 2 | Dosen memilih mata kuliah | Sistem menampilkan daftar mahasiswa peserta mata kuliah beserta isian nilai |
| 3 | Dosen mengisi nilai setiap mahasiswa | Sistem memeriksa nilai berada dalam rentang yang sah |
| 4 | Dosen menyimpan nilai | Sistem menyimpan nilai mahasiswa dan menampilkan konfirmasi |

**Skenario alternatif**

- A1 (cabang dari langkah 3): Nilai yang diisi di luar rentang yang sah → sistem menolak penyimpanan, menampilkan pesan nilai di luar rentang, dan meminta dosen memperbaiki nilai.
- A2 (cabang dari langkah 1): Dosen tidak mengampu mata kuliah apa pun pada periode berjalan → sistem menampilkan pesan tidak ada mata kuliah yang diampu dan input nilai tidak dilanjutkan.

**Skenario akhir**

Use case selesai jika nilai mahasiswa tersimpan; jika nilai di luar rentang yang sah atau dosen tidak mengampu mata kuliah, nilai tidak tersimpan.

## SIA-UC09 — Lihat KHS

| Elemen | Deskripsi |
|---|---|
| Aktor | Mahasiswa |
| Tujuan | Mahasiswa dapat mengetahui hasil studinya pada periode tertentu |
| Deskripsi | Mahasiswa membuka fungsi KHS, memilih periode, dan melihat KHS yang hanya memuat nilai yang sudah dipublikasikan |

**Skenario normal**

| Langkah | Kegiatan | Respons sistem |
|---|---|---|
| 1 | Mahasiswa membuka fungsi Lihat KHS | Sistem menampilkan daftar periode akademik mahasiswa tersebut |
| 2 | Mahasiswa memilih periode akademik | Sistem menampilkan KHS periode tersebut berisi mata kuliah beserta nilai yang sudah dipublikasikan |

**Skenario alternatif**

- A1 (cabang dari langkah 2): Belum ada nilai yang dipublikasikan pada periode yang dipilih → sistem menampilkan pesan belum ada nilai yang dipublikasikan pada periode tersebut.

**Skenario akhir**

Use case selesai jika KHS dengan nilai yang sudah dipublikasikan ditampilkan; jika belum ada nilai yang dipublikasikan, use case selesai dengan pesan tersebut.

## SIA-UC10 — Kelola Data Mahasiswa

| Elemen | Deskripsi |
|---|---|
| Aktor | Admin Akademik |
| Tujuan | Data mahasiswa terkelola melalui satu fungsi pengelolaan bersama |
| Deskripsi | Admin Akademik membuka fungsi pengelolaan data mahasiswa, memilih bentuk pengelolaan, dan menyimpan perubahan. Bentuk tambah, ubah, dan hapus dijabarkan pada tabel khususnya masing-masing |

**Skenario normal**

| Langkah | Kegiatan | Respons sistem |
|---|---|---|
| 1 | Admin Akademik membuka fungsi Kelola Data Mahasiswa | Sistem menampilkan daftar data mahasiswa |
| 2 | Admin Akademik memilih bentuk pengelolaan, yaitu tambah, ubah, atau hapus | Sistem menampilkan formulir sesuai bentuk pengelolaan yang dipilih |
| 3 | Admin Akademik mengisi atau mengonfirmasi data | Sistem memeriksa kelengkapan dan keabsahan data |
| 4 | Admin Akademik menyimpan perubahan | Sistem menyimpan perubahan dan menampilkan konfirmasi |

**Skenario alternatif**

- A1 (cabang dari langkah 3): Data tidak lengkap atau tidak sah → sistem menolak penyimpanan dan menampilkan pesan kesalahan data.

**Skenario akhir**

Use case selesai jika perubahan data mahasiswa tersimpan; jika data tidak lengkap atau tidak sah, perubahan tidak tersimpan.

## SIA-UC11 — Tambah Data Mahasiswa

| Elemen | Deskripsi |
|---|---|
| Aktor | Admin Akademik |
| Tujuan | Data mahasiswa baru tersimpan sebagai bentuk khusus dari pengelolaan data mahasiswa |
| Deskripsi | Admin Akademik mengisi data mahasiswa baru dan menyimpan data tersebut; langkah bersama mengikuti Tabel skenario SIA-UC10 |

**Skenario normal**

| Langkah | Kegiatan | Respons sistem |
|---|---|---|
| 1 | Admin Akademik membuka fungsi Tambah Data Mahasiswa | Sistem menampilkan formulir data mahasiswa baru |
| 2 | Admin Akademik mengisi data mahasiswa baru | Sistem memeriksa kelengkapan data |
| 3 | Admin Akademik menyimpan data | Sistem menyimpan data mahasiswa baru dan menampilkan konfirmasi |

**Skenario alternatif**

- A1 (cabang dari langkah 2): Data tidak lengkap → sistem menolak penyimpanan dan meminta Admin Akademik melengkapi data.

**Skenario akhir**

Use case selesai jika data mahasiswa baru tersimpan; jika data tidak lengkap, data tidak tersimpan.

## SIA-UC12 — Ubah Data Mahasiswa

| Elemen | Deskripsi |
|---|---|
| Aktor | Admin Akademik |
| Tujuan | Data mahasiswa berubah sebagai bentuk khusus dari pengelolaan data mahasiswa |
| Deskripsi | Admin Akademik memilih data mahasiswa, mengubah datanya, dan menyimpan perubahan; langkah bersama mengikuti Tabel skenario SIA-UC10 |

**Skenario normal**

| Langkah | Kegiatan | Respons sistem |
|---|---|---|
| 1 | Admin Akademik memilih data mahasiswa yang akan diubah | Sistem menampilkan data mahasiswa saat ini |
| 2 | Admin Akademik mengubah data mahasiswa | Sistem memeriksa perubahan data |
| 3 | Admin Akademik menyimpan perubahan | Sistem menyimpan data yang diubah dan menampilkan konfirmasi |

**Skenario alternatif**

- A1 (cabang dari langkah 1): Data mahasiswa tidak ditemukan → sistem menampilkan pesan data mahasiswa tidak ditemukan.

**Skenario akhir**

Use case selesai jika perubahan data mahasiswa tersimpan; jika data tidak ditemukan, perubahan tidak tersimpan.

## SIA-UC13 — Hapus Data Mahasiswa

| Elemen | Deskripsi |
|---|---|
| Aktor | Admin Akademik |
| Tujuan | Data mahasiswa terhapus sebagai bentuk khusus dari pengelolaan data mahasiswa |
| Deskripsi | Admin Akademik memilih data mahasiswa, mengonfirmasi penghapusan, dan sistem menghapus data tersebut; langkah bersama mengikuti Tabel skenario SIA-UC10 |

**Skenario normal**

| Langkah | Kegiatan | Respons sistem |
|---|---|---|
| 1 | Admin Akademik memilih data mahasiswa yang akan dihapus | Sistem memeriksa mahasiswa tidak memiliki data akademik aktif |
| 2 | Admin Akademik mengonfirmasi penghapusan | Sistem menghapus data mahasiswa dan menampilkan konfirmasi penghapusan |

**Skenario alternatif**

- A1 (cabang dari langkah 1): Mahasiswa memiliki data akademik aktif → sistem menolak penghapusan dan menampilkan pesan mahasiswa masih memiliki data akademik aktif.

**Skenario akhir**

Use case selesai jika data mahasiswa terhapus; jika mahasiswa memiliki data akademik aktif, data tidak terhapus.
