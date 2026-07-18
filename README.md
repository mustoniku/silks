# Panduan Penutupan Sementara Aplikasi SILIKS

## Tujuan

Pengunjung `https://kemenagkabtegal.id/siliks/` melihat halaman pengumuman, sedangkan deployment Google Apps Script tetap aktif dan dapat dibuka oleh Tim Pengembang menggunakan URL Apps Script asli.

## Persiapan wajib

1. Catat dan simpan URL deployment Apps Script asli.
2. Masuk ke panel hosting/WordPress/cPanel yang mengelola `kemenagkabtegal.id`.
3. Cari folder atau halaman yang melayani alamat `/siliks/`.
4. Unduh/cadangkan berkas `index.html` yang sekarang aktif. Beri nama, misalnya:
   `index-aplikasi-siliks-backup-2026-07-18.html`.
5. Jangan menghapus, menonaktifkan, atau membuat deployment baru di Google Apps Script.
6. Jangan membagikan URL Apps Script asli kepada madrasah selama masa penutupan.

## Cara memasang halaman pengumuman

### Jika `/siliks/` dikelola melalui cPanel/File Manager

1. Buka **File Manager**.
2. Masuk ke folder situs, biasanya salah satu dari:
   - `public_html/siliks/`
   - folder lain yang diarahkan ke URL `/siliks/`
3. Cadangkan berkas `index.html` lama.
4. Unggah `index-penutupan-siliks.html` dan `logo-siliks.webp` ke folder yang sama.
5. Ubah nama `index-penutupan-siliks.html` menjadi `index.html`. Jangan mengubah nama `logo-siliks.webp`.
6. Buka `https://kemenagkabtegal.id/siliks/?cek=20260718` menggunakan mode incognito.
7. Pastikan logo Kemenag di kiri, logo SILIKS di kanan, kartu pengumuman, hitung mundur, dan running text tampil baik di komputer dan ponsel.

### Jika `/siliks/` berupa halaman WordPress

1. Edit halaman SILIKS dengan editor yang dipakai.
2. Simpan isi/konfigurasi halaman lama sebagai cadangan.
3. Gunakan blok **Custom HTML** dan tempel isi halaman pengumuman.
4. Jika WordPress menghapus bagian `<head>`, `<style>`, atau `<script>`, gunakan pengelola file hosting atau minta admin web mengganti berkas pada route `/siliks/`. Cara ini lebih stabil untuk desain dan hitung mundur.

### Jika `/siliks/` saat ini hanya redirect ke Apps Script

1. Nonaktifkan sementara aturan redirect khusus `/siliks/`.
2. Arahkan `/siliks/` ke halaman pengumuman lokal.
3. Biarkan deployment Apps Script dan URL aslinya tetap aktif.
4. Simpan salinan aturan redirect lama agar mudah dikembalikan.

## Pemeriksaan setelah ditutup

1. Domain publik `/siliks/` menampilkan pengumuman.
2. URL Apps Script asli masih membuka aplikasi bagi Tim Pengembang.
3. Tombol login aplikasi tidak tersedia pada halaman publik.
4. Tanggal pembukaan tertulis **Senin, 20 Juli 2026 pukul 13.00 WIB**.
5. Pengujian dilakukan pada mode incognito dan minimal satu ponsel.
6. Bila masih muncul aplikasi lama, bersihkan cache situs/CDN dan cache browser.

## Cara membuka kembali Senin, 20 Juli 2026 pukul 13.00 WIB

Lakukan sekitar pukul 12.50–13.00 WIB:

1. Pastikan deployment Apps Script sudah diuji dan siap digunakan.
2. Masuk ke pengelola hosting/domain.
3. Simpan halaman pengumuman sebagai arsip, misalnya:
   `index-penutupan-siliks-2026-07.html`.
4. Kembalikan berkas `index.html` lama atau aktifkan kembali aturan redirect `/siliks/` menuju URL Apps Script.
5. Bersihkan cache hosting/CDN bila digunakan.
6. Buka `https://kemenagkabtegal.id/siliks/?aktif=20260720` melalui mode incognito.
7. Uji login menggunakan satu akun uji.
8. Pastikan halaman pengumuman tidak lagi muncul.
9. Setelah verifikasi berhasil, sampaikan informasi pembukaan kepada madrasah.

## Rencana pemulihan bila ada masalah

Jika aplikasi belum siap pada pukul 13.00 WIB, jangan menghapus halaman pengumuman. Ubah jadwal pembukaan pada halaman pengumuman terlebih dahulu, lalu publikasikan informasi terbaru melalui kanal resmi.

Jika halaman publik bermasalah setelah dibuka kembali, pasang kembali halaman pengumuman, periksa URL Apps Script, lalu aktifkan aplikasi setelah pengujian berhasil.
