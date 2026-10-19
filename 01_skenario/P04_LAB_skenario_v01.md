<!-- Deskripsi Skenario -->

## Deskripsi Skenario

| Aktor | Kedudukan | Tujuan terhadap sistem |
|---|---|---|
| Peminjam | Umum (general), baru pada Pertemuan 4. Mewariskan fungsinya kepada Mahasiswa dan Dosen. | Peran umum bagi peminjam peralatan. |
| Mahasiswa | Khusus dari Peminjam, tetap dari Pertemuan 3. | Melihat ketersediaan dan mengajukan peminjaman (diwarisi dari Peminjam), ditambah mencetak bukti pengajuan sebagai asosiasi khususnya sendiri. |
| Dosen | Khusus dari Peminjam, baru pada Pertemuan 4. | Melihat ketersediaan dan mengajukan peminjaman (diwarisi dari Peminjam). |
| Petugas Laboratorium | Tetap dari Pertemuan 3. | Mengelola data peralatan, memproses keputusan peminjaman, dan mencatat pengembalian peralatan. |
| Kepala Laboratorium | Tetap dari Pertemuan 3. | Melihat laporan peminjaman. |

## Tabel Katalog UseCase
| ID | Nama use case | Peran dalam model | Sumber kebutuhan |
|---|---|---|---|
| LAB-UC01 | Lihat Ketersediaan Peralatan | Tetap dari Pertemuan 3; fungsi aktor umum Peminjam | LAB-R01, LAB-R07 |
| LAB-UC02 | Kelola Data Peralatan | Tetap dari Pertemuan 3; use case UMUM bagi LAB-UC08, LAB-UC09, LAB-UC10 | LAB-R02, LAB-R08 |
| LAB-UC03 | Ajukan Peminjaman | Tetap dari Pertemuan 3; fungsi aktor umum Peminjam; menyertakan LAB-UC04; direalisasikan LAB-CO01 | LAB-R03, LAB-R07 |
| LAB-UC04 | Periksa Ketersediaan | Tetap dari Pertemuan 3; perilaku yang disertakan LAB-UC03 | LAB-R03 |
| LAB-UC05 | Cetak Bukti Pengajuan | Tetap dari Pertemuan 3; tambahan bersyarat pada LAB-UC03 melalui «extend» | LAB-R04 |
| LAB-UC06 | Proses Keputusan Peminjaman | Tetap dari Pertemuan 3; fungsi utama petugas | LAB-R05 |
| LAB-UC07 | Lihat Laporan Peminjaman | Tetap dari Pertemuan 3; fungsi utama kepala laboratorium | LAB-R06 |
| LAB-UC08 | Tambah Data Peralatan | Baru pada Pertemuan 4; use case KHUSUS dari LAB-UC02 | LAB-R08 |
| LAB-UC09 | Ubah Data Peralatan | Baru pada Pertemuan 4; use case KHUSUS dari LAB-UC02 | LAB-R08 |
| LAB-UC10 | Hapus Data Peralatan | Baru pada Pertemuan 4; use case KHUSUS dari LAB-UC02 | LAB-R08 |
| LAB-UC11 | Catat Pengembalian Peralatan | Baru pada Pertemuan 4; fungsi utama petugas; direalisasikan LAB-CO02 | LAB-R09 |
| LAB-UC12 | Periksa Kondisi Peralatan | Baru pada Pertemuan 4; perilaku yang disertakan LAB-UC11 | LAB-R10 |

## Tetapkan Generalization Aktor
- Mahasiswa adalah bentuk khusus dari Peminjam, dan Dosen adalah bentuk khusus dari Peminjam. Alasan: keduanya berbagi fungsi yang sama, yaitu melihat ketersediaan peralatan dan mengajukan peminjaman.
- Asosiasi ke LAB-UC01 dan LAB-UC03 digambar satu kali, yaitu dari Peminjam. Jangan menggambar garis yang sama dari Mahasiswa dan dari Dosen.
- Asosiasi Mahasiswa ke LAB-UC05 Cetak Bukti Pengajuan tidak ikut dipindahkan dan tidak dihapus, karena fungsi itu khusus mahasiswa. Asosiasi ini menjadi contoh asosiasi tambahan milik aktor khusus.
- Periksa arah panah pada gambar: ujung segitiga kosong harus menempel pada Peminjam, bukan pada Mahasiswa dan bukan pada Dosen. Karena Peminjam digambar di tengah, panah Mahasiswa mengarah ke bawah dan panah Dosen mengarah ke atas; keduanya berakhir pada Peminjam.

## Perbandingan Diagram
| Kelompok | Isi |
|---|---|
| Tetap sama dari Pertemuan 3 | Aktor Mahasiswa, Petugas Laboratorium, dan Kepala Laboratorium; use case LAB-UC01 sampai LAB-UC07; relasi «include» LAB-UC03 ke LAB-UC04; relasi «extend» LAB-UC05 ke LAB-UC03 lengkap dengan condition [mahasiswa memilih cetak] dan extension point Bukti pengajuan tersedia; asosiasi Petugas Laboratorium ke LAB-UC02 dan LAB-UC06; asosiasi Kepala Laboratorium ke LAB-UC07; asosiasi Mahasiswa ke LAB-UC05. |
| Berubah karena generalization aktor | Asosiasi ke LAB-UC01 dan LAB-UC03 yang pada Pertemuan 3 digambar dari Mahasiswa kini digambar satu kali dari Peminjam. Fungsi mahasiswa tidak hilang: mahasiswa mewarisinya dari Peminjam. Inilah satu-satunya perubahan garis pada diagram lama, dan alasannya adalah aturan generalization, bukan penghapusan fungsi. |
| Ditambah pada Pertemuan 4 | Aktor Peminjam dan Dosen; dua generalization aktor; use case LAB-UC08, LAB-UC09, LAB-UC10 beserta tiga generalization use case ke LAB-UC02; use case LAB-UC11 dan LAB-UC12 beserta relasi «include» antara keduanya dan asosiasi Petugas Laboratorium ke LAB-UC11; collaboration LAB-CO001 dan LAB-CO002 beserta dua relasi realization. |

## Tetapkan Generalization
- LAB-UC08, LAB-UC09, dan LAB-UC10 adalah bentuk khusus dari LAB-UC02 Kelola Data Peralatan. Alasan: ketiganya adalah bentuk khusus pengelolaan data peralatan.
- Tuliskan untuk setiap use case khusus satu kalimat perilaku pembedanya. Tambah menghasilkan data peralatan baru. Ubah menghasilkan data peralatan yang berubah. Hapus menghasilkan data peralatan yang terhapus dengan syarat pada aturan studi kasus.

## Tetapkan Collaboration dan realization
| ID | Nama collaboration (sama dengan nama use case) | Use case yang direalisasikan |
|---|---|---|
| LAB-CO01 | Ajukan Peminjaman | LAB-UC03: Ajukan Peminjaman |
| LAB-CO02 | Catat Pengembalian Peralatan | LAB-UC11: Catat Pengembalian Peralatan |

