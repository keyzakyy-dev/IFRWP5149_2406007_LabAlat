Mahasiswa mengajukan peminjaman peralatan dengan memilih alat, jumlah, dan rentang waktu. Sistem memeriksa ketersediaan. Jika tersedia dan data lengkap, sistem menyimpan pengajuan berstatus menunggu keputusan. Pada tampilan konfirmasi, mahasiswa dapat memilih mencetak bukti pengajuan. Petugas mengelola data peralatan serta menyetujui atau menolak pengajuan. Kepala laboratorium melihat laporan peminjaman.

Batas sistem dan aturan:
- Sistem mencatat dan menyediakan informasi; perpindahan fisik alat tidak terjadi di dalam perangkat lunak.
- Pengguna telah terautentikasi dan memiliki hak akses sesuai peran.
- Pengajuan yang diterima sistem berstatus Menunggu keputusan, bukan otomatis Disetujui.
- Pengajuan dengan peralatan tidak tersedia tidak disimpan sebagai pengajuan berhasil.
- Pencetakan bukti tidak menjadi syarat keberhasilan pengajuan.
- Persetujuan petugas belum dimodelkan sebagai reservasi teknis stok.
- Pengambilan, pengembalian, kondisi alat, dan denda belum dianalisis pada potongan model ini.

| Aktor | Tujuan terhadap sistem |
|---|---|
| Mahasiswa | Melihat ketersediaan, mengajukan peminjaman, dan mencetak bukti |
| Petugas laboratorium | Mengelola peralatan dan memproses keputusan |
| Kepala laboratorium | Melihat laporan peminjaman |