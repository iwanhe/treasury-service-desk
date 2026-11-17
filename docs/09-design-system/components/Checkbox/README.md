Checkbox dan radio untuk seleksi baris, opsi form, dan pilihan tunggal.

## Aturan

- Ukuran 18px, border `border-strong` (3:1), terpilih memakai fill `primary` dengan tanda centang atau titik putih. Tanda di dalam kotak membuat keadaan terpilih terbaca tanpa warna.
- Keadaan indeterminate (garis) untuk "pilih semua" saat sebagian baris terpilih.
- Label selalu di sampingnya dan ikut dapat diklik. Area klik minimal 24px.
- Seleksi baris tabel: kotak di kolom pertama; saat ada baris terpilih, bar aksi massal muncul di atas daftar dan menyebut jumlah terpilih.
- Nonaktif memakai `disabled` dan menyebut alasannya di teks bantu bila terkait kebijakan.
- Radio untuk pilihan tunggal dengan 2–5 opsi; lebih dari itu pakai select.

## Token

`border-strong`, `primary`, `text-on-solid`, `surface`, `surface-subtle`, `focus-ring`, `radius-sm`, `radius-full`.
