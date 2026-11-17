Tabel saldo per rekening untuk dashboard dan daftar rekening.

## Kolom

Company, Bank, Rekening (masking, mono), Currency, Saldo, Jenis saldo, Tanggal saldo, Status.

## Aturan

- Saldo rata kanan dengan `tabular-nums` dan kode currency; tiap baris tetap dalam currency rekeningnya. Tidak ada baris total yang mencampur currency; total ada di CashPositionTotals.
- Status: **Reconciled** (badge teal dengan ikon) atau **Stale** (ikon jam, border putus-putus) dengan tanggal saldo terakhir.
- Baris stale tidak diredupkan atau diberi warna merah; informasinya ada di kolom tanggal dan status.
- Nomor rekening selalu masking; nomor lengkap hanya lewat aksi eksplisit bagi role yang diotorisasi.
- Baris dapat dibuka ke Account Detail dan riwayat saldo; klik pada baris dan Enter dari keyboard sama-sama membuka.

## Token

`surface-subtle` (header), `border`, `reconciled`, `stale`, gaya `body-sm`, `amount`, `reference`.
