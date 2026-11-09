## Langkah 5 — Susun deskripsi

### a. LAB-UC01 — Lihat Ketersediaan Peralatan

| Elemen | Deskripsi |
|---|---|
| Tujuan | Menampilkan informasi ketersediaan peralatan laboratorium |
| Aktor utama | Mahasiswa |
| Sumber kebutuhan | LAB-R01 |
| Pemicu | Mahasiswa membuka fungsi lihat ketersediaan peralatan |
| Prasyarat | Mahasiswa telah terautentikasi dan data peralatan tersedia |
| Pascakondisi berhasil | Sistem menampilkan daftar peralatan beserta status ketersediaannya |
| Pascakondisi gagal | Tidak ada data peralatan yang dapat ditampilkan dan sistem menampilkan informasi kegagalan |
| Include | Tidak ada |
| Extension point | — |
| Extend | Tidak ada |

### b. LAB-UC02 — Kelola Data Peralatan

| Elemen | Deskripsi |
|---|---|
| Tujuan | Mengelola data peralatan laboratorium |
| Aktor utama | Petugas laboratorium |
| Sumber kebutuhan | LAB-R02 |
| Pemicu | Petugas memilih fungsi pengelolaan data peralatan |
| Prasyarat | Petugas telah terautentikasi |
| Pascakondisi berhasil | Data peralatan tersimpan atau terubah sesuai tindakan petugas |
| Pascakondisi gagal | Perubahan data tidak tersimpan dan sistem menampilkan informasi kegagalan |
| Include | Tidak ada |
| Extension point | — |
| Extend | Tidak ada |

### c. LAB-UC03 — Ajukan Peminjaman

| Elemen | Deskripsi |
|---|---|
| Tujuan | Menghasilkan pengajuan peminjaman peralatan yang tersimpan di dalam sistem |
| Aktor utama | Mahasiswa |
| Sumber kebutuhan | LAB-R03 |
| Pemicu | Mahasiswa memilih fungsi pengajuan peminjaman |
| Prasyarat | Mahasiswa telah terautentikasi dan data peralatan tersedia untuk diajukan |
| Pascakondisi berhasil | Pengajuan peminjaman tersimpan dengan status menunggu keputusan |
| Pascakondisi gagal | Pengajuan tidak berhasil disimpan dan sistem menampilkan informasi kegagalan |
| Include | LAB-UC04 — Periksa Ketersediaan |
| Extension point | Pencetakan bukti pengajuan tersedia setelah pengajuan berhasil disimpan |
| Extend | LAB-UC05 — Cetak Bukti Pengajuan, jika mahasiswa memilih pencetakan |

### d. LAB-UC04 — Periksa Ketersediaan

| Elemen | Deskripsi |
|---|---|
| Tujuan | Memastikan peralatan yang diajukan tersedia sebelum pengajuan disimpan |
| Aktor utama | Sistem, dipicu oleh pengajuan mahasiswa |
| Sumber kebutuhan | LAB-R03 |
| Pemicu | Mahasiswa mengajukan peminjaman dan sistem menjalankan pemeriksaan ketersediaan |
| Prasyarat | Mahasiswa telah terautentikasi dan data pengajuan telah diisi |
| Pascakondisi berhasil | Peralatan dinyatakan tersedia dan proses pengajuan dapat dilanjutkan |
| Pascakondisi gagal | Peralatan tidak tersedia, sistem menampilkan alasan kegagalan, dan pengajuan tidak disimpan |
| Include | Tidak ada |
| Extension point | Pemeriksaan ketersediaan peralatan yang diajukan |
| Extend | Tidak ada |

### e. LAB-UC05 — Cetak Bukti Pengajuan

| Elemen | Deskripsi |
|---|---|
| Tujuan | Menghasilkan bukti pengajuan peminjaman yang dapat dicetak mahasiswa |
| Aktor utama | Mahasiswa |
| Sumber kebutuhan | LAB-R04 |
| Pemicu | Mahasiswa memilih opsi cetak bukti saat konfirmasi pengajuan peminjaman |
| Prasyarat | Pengajuan peminjaman berhasil disimpan dan bukti tersedia |
| Pascakondisi berhasil | Bukti pengajuan berhasil dicetak oleh mahasiswa |
| Pascakondisi gagal | Bukti tidak berhasil dicetak dan sistem menampilkan informasi kegagalan |
| Include | Tidak ada |
| Extension point | Pilihan cetak bukti pada tahap konfirmasi pengajuan peminjaman |
| Extend | LAB-UC03 — Ajukan Peminjaman, jika mahasiswa memilih opsi cetak bukti |

### f. LAB-UC06 — Proses Keputusan Peminjaman

| Elemen | Deskripsi |
|---|---|
| Tujuan | Menghasilkan keputusan persetujuan atau penolakan terhadap pengajuan peminjaman |
| Aktor utama | Petugas laboratorium |
| Sumber kebutuhan | LAB-R05 |
| Pemicu | Petugas memilih pengajuan peminjaman yang berstatus menunggu keputusan |
| Prasyarat | Petugas telah terautentikasi dan pengajuan peminjaman tersedia untuk diproses |
| Pascakondisi berhasil — disetujui | Status pengajuan berubah menjadi disetujui dan hasil keputusan tersimpan |
| Pascakondisi berhasil — ditolak | Status pengajuan berubah menjadi ditolak dan hasil keputusan tersimpan |
| Pascakondisi gagal | Keputusan tidak berhasil disimpan dan status tetap menunggu keputusan |
| Include | Tidak ada, kecuali terdapat proses wajib lain yang ditetapkan dalam skenario |
| Extension point | Penentuan hasil keputusan terhadap pengajuan peminjaman |
| Extend | Tidak ada |

### g. LAB-UC07 — Lihat Laporan Peminjaman

| Elemen | Deskripsi |
|---|---|
| Tujuan | Menampilkan laporan peminjaman peralatan |
| Aktor utama | Kepala laboratorium |
| Sumber kebutuhan | LAB-R06 |
| Pemicu | Kepala laboratorium membuka fungsi lihat laporan peminjaman |
| Prasyarat | Kepala laboratorium telah terautentikasi dan data peminjaman tersedia |
| Pascakondisi berhasil | Sistem menampilkan laporan peminjaman |
| Pascakondisi gagal | Laporan tidak dapat ditampilkan dan sistem menampilkan informasi kegagalan |
| Include | Tidak ada |
| Extension point | — |
| Extend | Tidak ada |
