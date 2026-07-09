PANDUAN REDIRECT GITHUB PAGES KE APLIKASI CAPKIN

File yang perlu diupload ke repository GitHub Pages:
- index.html
- 404.html

Target redirect saat ini:
Belum diisi. Ganti teks GANTI_DENGAN_URL_WEB_APP_EXEC di index.html dengan URL Web App terbaru.

LANGKAH DI GITHUB

1. Buka repository GitHub yang dipakai untuk alamat:
   https://mustoniku.github.io/capkin/

2. Buka Apps Script > Terapkan/Deploy > Kelola deployment.

3. Copy URL Web App terbaru. URL yang benar harus berbentuk:
   https://script.google.com/macros/s/.../exec

   Catatan:
   - Jangan pakai URL editor Apps Script.
   - Jangan pakai URL yang berakhiran /dev.
   - Pastikan akses Web App: Anyone / Siapa saja yang memiliki link.

4. Buka file index.html dari folder ini.

5. Ganti:
   GANTI_DENGAN_URL_WEB_APP_EXEC

   dengan URL Web App terbaru yang berakhiran /exec.

6. Upload/replace file index.html ke repository GitHub Pages.

7. Upload/replace file 404.html di tempat yang sama.

8. Buka Settings > Pages.

9. Pastikan Source mengarah ke branch dan folder yang benar, biasanya:
   Branch: main
   Folder: /root

10. Tunggu 1-3 menit, lalu buka:
   https://mustoniku.github.io/capkin/

JIKA TARGET WEB APP BERUBAH

Buka index.html, ganti URL pada bagian:
const TARGET_URL = '...';

Sekarang cukup ganti bagian TARGET_URL saja. Tombol "Buka Aplikasi" otomatis mengikuti TARGET_URL.

CATATAN

- Redirect ini memakai JavaScript dan meta refresh.
- File index.html sekarang hanya memakai satu target URL agar tidak mudah salah tempel.
- Jangan membuka Apps Script di iframe GitHub Pages karena Web App Google sering memblokir iframe.
- Cara paling aman adalah redirect langsung seperti file ini.
