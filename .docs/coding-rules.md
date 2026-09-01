# Aturan Penulisan Kode

## Umum

Utamakan kode yang sederhana dibandingkan kode yang terlalu rumit atau "pintar".

Jangan membuat abstraksi tanpa adanya kasus penggunaan ulang yang nyata.

Jangan membuat berkas (file) kecuali jika memiliki tanggung jawab yang jelas.

Jangan menduplikasi utilitas yang sudah ada.

Periksa komponen yang sudah ada sebelum membuat komponen baru.

## TypeScript

Hindari penggunaan `any`.

Utamakan tipe data eksplisit untuk antarmuka publik (public interfaces).

Gunakan Zod untuk validasi *runtime* terhadap input eksternal.

Jangan hanya mengandalkan TypeScript untuk validasi input pengguna.

## React

Pastikan komponen tetap fokus pada satu tujuan.

Hindari penggunaan *client component* yang tidak perlu.

Utamakan *Server Component* jika interaktivitas tidak diperlukan.

Jangan menempatkan akses basis data di dalam komponen presentasi.

## Next.js

Ikuti arsitektur App Router yang sudah ada.

Jangan memperkenalkan pola *routing* lain.

Gunakan operasi sisi server untuk logika yang sensitif.

Simpan data rahasia di server.

## Basis Data

Jangan pernah memercayai data yang diberikan oleh klien, seperti:

- harga
- total
- peran (*role*)
- izin (*permissions*)
- status pesanan

Hitung ulang nilai-nilai sensitif di server.

## Performa

Hindari kueri basis data yang tidak perlu.

Hindari pengambilan data yang tidak diperlukan.

Utamakan paginasi untuk kumpulan data yang berpotensi besar.

Jangan melakukan optimasi terlalu dini (*premature optimization*).

Lakukan pengukuran sebelum menerapkan optimasi yang kompleks.

## Keamanan

Validasi setiap input eksternal.

Lakukan otorisasi untuk setiap operasi yang dilindungi.

Jangan mengandalkan otorisasi di tingkat UI.

Jangan pernah mengekspos data rahasia.

Jangan pernah menampilkan pesan kesalahan internal yang sensitif kepada klien.

## Kemudahan Pemeliharaan

Satu tanggung jawab per modul.

Penamaan yang jelas.

Fungsi yang ringkas.

Perilaku yang dapat diprediksi.

Dependensi minimal.