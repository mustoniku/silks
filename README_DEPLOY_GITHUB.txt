PANDUAN REDIRECT GITHUB PAGES KE APLIKASI SILIKS

File yang perlu diupload ke repository GitHub Pages:
- index.html
- 404.html

Target redirect saat ini:
https://script.google.com/macros/s/AKfycbzq0X6FiYJT6O8GjXNHFnhVdti9IiklSFqYxFtXy3fkv11zZ2E3Lf7uoB_jm4gj-qyT/exec

LANGKAH DI GITHUB

1. Buka repository GitHub yang dipakai untuk alamat SILIKS.

2. Upload/replace file index.html dari folder ini ke root repository atau folder yang dipakai GitHub Pages.

3. Upload/replace file 404.html di tempat yang sama.

4. Buka Settings > Pages.

5. Pastikan Source mengarah ke branch dan folder yang benar, biasanya:
   Branch: main
   Folder: /root

6. Tunggu 1-3 menit, lalu buka alamat GitHub Pages SILIKS.

JIKA TARGET WEB APP BERUBAH

Buka index.html, lalu ganti URL pada bagian:

const TARGET_URL = '...';

Gunakan URL Web App Apps Script yang berakhiran /exec.

CATATAN

- Jangan pakai URL editor Apps Script.
- Jangan pakai URL yang berakhiran /dev.
- Pastikan akses Web App: Anyone / Siapa saja yang memiliki link.
- Redirect ini memakai JavaScript agar langsung berpindah ke Apps Script.
