## Langkah 5 — Susun deskripsi
### a. SIA-UC02 — Ajukan KRS
| Elemen | Deskripsi |
|---|---|
| Tujuan | Menghasilkan pengajuan KRS yang tersimpan di dalam sistem |
| Aktor utama | Mahasiswa |
| Sumber kebutuhan | SIA-R03 |
| Pemicu | Mahasiswa memilih fungsi pengajuan KRS |
| Prasyarat | Mahasiswa telah terautentikasi dan data KRS tersedia untuk diajukan |
| Pascakondisi berhasil | Pengajuan KRS tersimpan dengan nomor pengajuan dan status menunggu keputusan Dosen Wali |
| Pascakondisi gagal | Pengajuan KRS tidak berhasil disimpan dan sistem menampilkan informasi kegagalan |
| Include | SIA-UC06 — Validasi KRS |
| Extension point | Pengunduhan bukti pengajuan tersedia setelah pengajuan berhasil disimpan |
| Extend | SIA-UC03 — Unduh Bukti Pengajuan KRS, jika mahasiswa memilih opsi unduh |

### b. SIA-UC06 — Validasi KRS
| Elemen | Deskripsi |
|---|---|
| Tujuan | Memastikan pengajuan KRS memenuhi ketentuan sistem sebelum disimpan |
| Aktor utama | Sistem, dipicu oleh pengajuan mahasiswa |
| Sumber kebutuhan | SIA-R04 |
| Pemicu | Mahasiswa mengajukan KRS dan sistem menjalankan validasi |
| Prasyarat | Mahasiswa telah terautentikasi dan data pengajuan KRS telah diisi |
| Pascakondisi berhasil | Pengajuan dinyatakan valid dan proses pengajuan dapat dilanjutkan |
| Pascakondisi gagal | Pengajuan tidak lolos validasi, sistem menampilkan alasan kegagalan, dan mahasiswa dapat memperbaiki data |
| Include | Tidak ada |
| Extension point | Pemeriksaan kelengkapan dan kesesuaian data KRS |
| Extend | Tidak ada |

### c. SIA-UC03 — Unduh Bukti Pengajuan KRS
| Elemen | Deskripsi |
|---|---|
| Tujuan | Menghasilkan bukti pengajuan KRS yang dapat diunduh mahasiswa |
| Aktor utama | Mahasiswa |
| Sumber kebutuhan | SIA-R05 |
| Pemicu | Mahasiswa memilih opsi unduh bukti saat konfirmasi pengajuan KRS |
| Prasyarat | Pengajuan KRS berhasil disimpan dan bukti pengajuan tersedia |
| Pascakondisi berhasil | Bukti pengajuan KRS berhasil diunduh oleh mahasiswa |
| Pascakondisi gagal | Bukti tidak berhasil diunduh dan sistem menampilkan informasi kegagalan |
| Include | Tidak ada |
| Extension point | Pilihan unduh bukti pada tahap konfirmasi pengajuan KRS |
| Extend | SIA-UC02 — Ajukan KRS, jika mahasiswa memilih opsi unduh bukti |

### d. SIA-UC05 — Proses Keputusan KRS
| Elemen | Deskripsi |
|---|---|
| Tujuan | Menghasilkan keputusan persetujuan atau penolakan terhadap pengajuan KRS mahasiswa |
| Aktor utama | Dosen Wali |
| Sumber kebutuhan | SIA-R06 |
| Pemicu | Dosen Wali memilih pengajuan KRS yang berstatus menunggu keputusan |
| Prasyarat | Dosen Wali telah terautentikasi dan pengajuan KRS mahasiswa tersedia untuk diproses |
| Pascakondisi berhasil — disetujui | Status pengajuan berubah menjadi disetujui dan hasil keputusan tersimpan di sistem |
| Pascakondisi berhasil — ditolak | Status pengajuan berubah menjadi ditolak dan hasil keputusan tersimpan di sistem |
| Pascakondisi gagal | Keputusan tidak berhasil disimpan dan status pengajuan tetap menunggu keputusan |
| Include | Tidak ada, kecuali terdapat proses wajib lain yang ditetapkan dalam skenario |
| Extension point | Penentuan hasil keputusan terhadap pengajuan KRS |
| Extend | Tidak ada |