Baris total cash position, satu kolom per currency.

## Aturan

- Satu kolom per currency (IDR, USD, SGD, dan lainnya). Tidak ada total gabungan lintas currency kecuali dengan kurs dan tanggal kurs yang jelas.
- Setiap kolom memuat: label "Total IDR", nominal (gaya `amount-xl`), jenis saldo (default **Reconciled**), tanggal saldo "per 17 Nov 2026", dan jumlah rekening.
- Jika sebagian rekening stale, kolom menampilkan penanda stale dengan jumlah rekening terdampak. Tanggal yang ditampilkan adalah tanggal terlama.
- Hanya statement Posted yang dihitung. Pending Approval atau Rejected tidak memengaruhi angka.
- Filter (tanggal, company, bank) berada dalam satu baris di atas dan berlaku untuk seluruh widget.
- Angka besar memakai angka proporsional, bukan `tabular-nums`; tabular hanya untuk kolom yang harus sejajar.

## Token

`surface`, `border`, `radius-lg`, `reconciled`, `reconciled-bg`, `stale`, `stale-bg`, gaya `amount-xl`, `caption`.
