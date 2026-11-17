Tile angka tunggal untuk widget operasional: Pending Approval, Ticket Backlog, SLA at Risk.

## Isi

Label (kalimat biasa, tanpa titik dua), nilai (gaya 28px semibold, angka proporsional), dan tautan ke antrean terkait. Ikon kecil di samping label membawa warna semantik; teks tetap memakai token teks.

## Aturan

- Satu tile, satu angka. Tidak ada tile yang menjumlahkan uang lintas currency.
- Tile bukan grafik: tidak perlu tooltip, tetapi tautan "Lihat antrean" wajib agar angka dapat ditelusuri.
- Perubahan (delta) hanya jika disebut periode pembandingnya, misalnya "+2 dibanding kemarin", dan tidak bergantung warna.
- Pending Approval memakai `approval`, SLA at Risk memakai `sla-warning`, Ticket Backlog netral (`text-muted`).

## Token

`surface`, `border`, `approval`, `sla-warning`, `text`, `text-muted`, `primary-text`, `radius-lg`.
