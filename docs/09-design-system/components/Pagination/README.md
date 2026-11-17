Pagination untuk tabel panjang: daftar tiket, riwayat import, transaksi statement.

## Aturan

- Tampilkan rentang dan total: "Menampilkan 1–50 dari 214". Selalu ada total agar pengguna tahu ukuran data.
- Halaman aktif memakai `aria-current="page"` dengan border dan latar `primary-subtle`. Tombol Sebelumnya dan Berikutnya nonaktif di ujung.
- Ukuran halaman dapat dipilih (25, 50, 100); pilihan diingat per tabel.
- Mengubah filter mengembalikan ke halaman 1.
- Untuk tabel transaksi statement, pagination tidak memengaruhi total di footer: total selalu atas seluruh transaksi.

## Token

`primary`, `primary-subtle`, `primary-text`, `text-muted`, `surface-subtle`, `focus-ring`.
