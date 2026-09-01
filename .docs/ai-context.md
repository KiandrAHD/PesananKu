# PesananKu — Konteks AI

## Identitas Proyek

PesananKu adalah platform pemesanan digital untuk kafe dan restoran.

## Konsep Utama

PesananKu mendukung dua metode pemesanan utama:

1. Pemesanan via Kios
2. Pemesanan via QR di Meja

Kedua metode pemesanan ini menggunakan sistem pemesanan terpusat yang sama.

## Alur Utama

Pelanggan
→ Menu
→ Keranjang
→ Checkout
→ Pembayaran
→ Pesanan Dibuat
→ Dapur
→ Pemrosesan Pesanan
→ Siap
→ Pelanggan Menerima Pesanan

## Saluran Pemesanan

### Kios

Pelanggan → Kios → Menu → Checkout → Pembayaran → Nomor Pesanan

### QR Meja

Pelanggan → Pindai QR → Identifikasi Meja → Menu → Checkout → Pembayaran → Dapur

## Dapur

Dapur menerima semua pesanan dari kedua saluran tersebut.

Siklus hidup pesanan:

PENDING (Menunggu)
→ CONFIRMED (Dikonfirmasi)
→ ​​PREPARING (Sedang Disiapkan)
→ READY (Siap)
→ COMPLETED (Selesai)

## Prinsip Penting

Kios dan QR Meja adalah antarmuka pemesanan yang berbeda,
namun keduanya harus menggunakan domain pemesanan dasar yang sama.

Jangan membuat sistem pemesanan terpisah untuk pemesanan via kios dan QR.

## Teknologi

Frontend:
Next.js
React
TypeScript
Tailwind CSS
shadcn/ui

Backend:
Kemampuan sisi server Next.js
Prisma ORM
PostgreSQL

Validasi:
Zod

State:
Zustand (jika diperlukan state sisi klien)

Autentikasi:
Auth.js

Pengujian:
Vitest
Playwright

## Prinsip Arsitektur

Utamakan organisasi berbasis fitur.

Logika bisnis tidak boleh ditempatkan langsung di dalam komponen UI.

Akses basis data harus dipisahkan dari komponen presentasi.

Validasi harus dilakukan pada batas sistem.
