Mahasiswa mengajukan KRS dengan memilih mata kuliah. Setiap pengajuan menjalankan validasi KRS yang memeriksa kelengkapan, prasyarat mata kuliah, dan benturan jadwal. Jika validasi berhasil, sistem menyimpan pengajuan berstatus menunggu persetujuan dosen wali. Pada konfirmasi penyimpanan, mahasiswa dapat memilih mengunduh bukti pengajuan. Dosen wali menyetujui atau menolak KRS dan memberikan catatan keputusan.

## Langkah 1 — Catat kebutuhan dan batas

| ID | Kebutuhan tugas |
|---|---|
| SIA-R01 | Mahasiswa dapat melihat jadwal kuliah |
| SIA-R02 | Admin akademik dapat mengelola jadwal kuliah |
| SIA-R03 | Mahasiswa dapat mengajukan KRS |
| SIA-R04 | Sistem memvalidasi KRS sebagai bagian pengajuan |
| SIA-R05 | Mahasiswa dapat mengunduh bukti jika memilihnya pada konfirmasi pengajuan |
| SIA-R06 | Dosen wali dapat memproses persetujuan atau penolakan KRS |

Batas dan asumsi:
- Pengguna telah terautentikasi.
- Data mata kuliah, prasyarat, dan jadwal tersedia.
- Validasi gagal menyebabkan pengajuan belum berhasil tersimpan.
- Unduh bukti tidak menjadi syarat keberhasilan pengajuan.
- KRS tersimpan belum berarti disetujui.
- Pembayaran, pengisian nilai, dan implementasi basis data berada di luar
tugas.

## Langkah 2 — Identifikasi aktor dan use case

|   ID  | Nama UseCase            | Peran Dalam Model                  |
|-------|--------------           |-------------------                 |
|SIA-R01| Melihat Jadwal Kuliah   | Fungsi Utama Mahasiswa             |
|SIA-R02| Mengajukan KRS          | Fungsi Utama Mahasiswa             |
|SIA-R03| Mengunduh Bukti         | Fungsi Utama Mahasiswa             |
|SIA-R04| Mengelola Jadwal Kuliah | Fungsi Utama Akademik              |
|SIA-R05| Menyetujui/Menolak KRS  | Fungsi Utama Dosen Wali            |
|SIA-R06| Validasi KRS            | Perilaku yang disertakan pada R02  |

## Langkah 3 — Tentukan include
SIA-R02 <<"include">> SIA-R06
Alasan : Karena Validasi KRS termasuk dalam bagian Pengajuan KRS

## Langkah 4 — Tentukan extend
SIA-R03 <<"extend>> SIA-R02
Alasan : Karena Mengunduh bukti termasuk dalam Pengajuan KRS