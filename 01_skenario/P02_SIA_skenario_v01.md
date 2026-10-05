Mahasiswa melihat jadwal kuliah melalui Sistem Informasi Akademik.
Admin akademik mengelola jadwal kuliah. Dalam latihan ini, mahasiswa
tidak mengelola jadwal dan admin tidak dihubungkan dengan fungsi
melihat jadwal sebagai pengguna mahasiswa.

### Koreksi Yang Dilakukan :
1. memindahkan aktor mahasiswa ke luar sistem, karena Aktor adalah pihak eksternal yang berinteraksi dengan sistem.
2. mengubah lihat jadwal kuliah menjadi elips, karena usecase pada UML digambar bentuk elips
3. menghubungkan aktor mahasiswa dengan lihat jadwal kuliah, karena aktor mahasiswa dan dosen dihubungkan ke perannya (mahasiswa ke lihat jadwal kuliah) , (dosen ke kelola jadwal kuliah)
4. mengganti judul menjadi Sistem Informasi Akademik, karena Judul harus sesuai dengan sistem yang direpresentasikan oleh diagram

Garis asosiasi bukan alur proses karena garis tersebut hanya menunjukkan hubungan atau interaksi antara aktor dan use case; garis itu tidak menunjukkan urutan langkah, arah proses, atau perpindahan data.

Hasil uji buka ulang sumber: berkas sumber berhasil dibuka kembali dan diagram tampil lengkap. Aktor, batas sistem, use case, serta garis asosiasi tetap tersedia dan dapat diperiksa.