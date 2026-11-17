Kartu saldo rekening atau company yang menampilkan jenis saldo, tanggal saldo, dan penanda stale.

## Isi kartu

- Judul: company, bank, nomor rekening masking, currency.
- Nominal utama: saldo **Reconciled** (default dashboard) memakai Amount `xl`.
- Baris pendukung: **Bank reported** dan **Calculated** dengan nominalnya.
- Tanggal saldo: "per 17 Nov 2026". Jika statement hari berjalan belum ada, tampilkan penanda stale beserta tanggal saldo terakhir.

## Aturan

- Jangan menjumlahkan currency berbeda dalam satu kartu.
- Jangan menyebut saldo sebagai real-time.
- Selisih Bank reported dan Calculated ditampilkan sebagai teks dan ikon, bukan hanya warna.
- Hanya statement berstatus Posted yang memengaruhi angka; statement Pending Approval atau Rejected tidak.

## Token

`surface`, `border`, `radius-lg`, `elevation-1`, `reconciled`, `reconciled-bg`, `stale`, `stale-bg`, `text-muted`, gaya `amount-xl`, `caption`, `label`.
