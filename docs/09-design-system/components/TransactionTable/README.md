Tabel transaksi statement dengan kolom debit dan credit terpisah.

## Kolom

Tanggal transaksi, Value date, Deskripsi, Reference (mono), Debit, Credit, Running balance.

## Aturan

- Debit dan credit di dua kolom, rata kanan, `tabular-nums`, tanpa angka negatif. Sel kosong ditulis "—".
- Debit memakai `fin-debit` dan credit `fin-credit`, namun posisi kolom sudah cukup menjelaskan arah; warna hanya penguat.
- Header memakai `surface-subtle`, tinggi baris `row-compact` (44px) atau `row-comfortable` (56px).
- Baris dengan masalah validasi diberi ikon dan teks di kolom paling kiri, bukan hanya latar merah.
- Footer menampilkan total debit, total credit, dan rumus Opening + Credit − Debit = Closing.
- Statement Posted: tabel hanya baca. Koreksi lewat Reverse atau Adjust dari menu baris, dengan referensi transaksi asli.

## Aksesibilitas

`<table>` dengan `<th scope="col">`. Kolom angka diberi `text-align: right`. Urutan kolom dapat diubah dengan keyboard.
