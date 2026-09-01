# Instruksi Agen PesananKu

## Sebelum Coding

1. Baca file ini terlebih dahulu.
2. Pahami tugas yang diminta pengguna.
3. Periksa implementasi yang ada sebelum memodifikasi file.
4. Baca hanya dokumentasi yang relevan dari `.docs/`.
5. Jangan membuat fungsionalitas duplikat.
6. Jangan menulis ulang kode yang sudah berjalan dengan baik tanpa alasan yang jelas.

## Dokumentasi

Gunakan `.docs/README.md` untuk menemukan dokumentasi yang relevan.

Dokumentasi yang relevan wajib dibaca sebelum menerapkan perubahan yang memengaruhi:

- arsitektur
- basis data
- autentikasi
- otorisasi
- aturan bisnis
- keamanan
- pembayaran
- siklus hidup pesanan

## Prinsip Coding

- Utamakan solusi yang sederhana dan mudah dipelihara.
- Hindari abstraksi yang tidak perlu.
- Hindari optimasi dini (*premature optimization*).
- Gunakan kembali komponen dan utilitas yang sudah ada.
- Pisahkan logika bisnis dari komponen presentasi.
- Validasi input eksternal.
- Jangan pernah memercayai input dari sisi klien (*client-side*).
- Gunakan TypeScript dengan mode ketat (*strict*).
- Tangani error secara eksplisit.
- Hindari duplikasi logika.
- Pastikan fungsi memiliki fokus yang jelas dan perilakunya dapat diprediksi.

## Keamanan

- Jangan pernah mengekspos informasi rahasia (*secrets*).
- Jangan pernah melakukan *commit* pada file `.env`.
- Jangan pernah memercayai harga yang diberikan oleh klien.
- Jangan pernah memercayai peran (*role*) yang diberikan oleh klien.
- Validasi otorisasi di sisi server.
- Validasi semua input eksternal.
- Jangan tampilkan error basis data yang sensitif kepada pengguna.
- Gunakan kueri basis data yang aman melalui Prisma.
- Jangan melewati pemeriksaan autentikasi atau otorisasi.

## Basis Data

- Jangan pernah mengubah skema basis data tanpa memeriksa relasi yang ada.
- Pertahankan data historis pesanan.
- Harga pesanan harus menggunakan *snapshot* pada saat transaksi terjadi.
- Jangan sembarangan melakukan migrasi yang bersifat destruktif.
- Utamakan perubahan yang kompatibel ke belakang (*backward-compatible*).

## Pengujian

Setiap fitur yang signifikan harus disertai dengan pengujian yang memadai.

Sebelum menganggap tugas selesai:

1. Jalankan *linting*.
2. Jalankan pemeriksaan tipe (*type checking*) atau *build*.
3. Jalankan pengujian yang relevan.
4. Verifikasi fungsionalitas yang telah diubah.
5. Tinjau perubahan kode (*diff*).

## Git

Pastikan *commit* memiliki fokus yang jelas.

Gunakan format pesan *commit* konvensional jika sesuai.

Jangan melakukan *commit* pada:

- `.env`
- informasi rahasia (*secrets*)
- kredensial
- *output build* yang dihasilkan secara otomatis
- `node_modules`

## Penting

Jangan membuat asumsi.

Periksa basis kode yang ada sebelum melakukan perubahan arsitektur. Jika perubahan yang diminta bertentangan dengan aturan bisnis atau arsitektur yang terdokumentasi, jelaskan pertentangan tersebut sebelum mengubah desain.