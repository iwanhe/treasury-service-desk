Tampilan nominal uang dengan currency, tanda debit atau credit, dan angka tabular.

## Aturan

- Format id-ID dengan kode currency: `IDR 15.000.000,00`. Desimal sesuai currency.
- Credit: tanda `+`, ikon panah masuk, token `fin-credit`. Debit: tanda `−`, ikon panah keluar, token `fin-debit`. Tanda dan ikon wajib, warna saja tidak cukup.
- Di tabel transaksi, debit dan credit berada di dua kolom terpisah; komponen ini dipakai di ringkasan dan daftar.
- Rata kanan, `tabular-nums`. Nominal tidak pernah dibulatkan secara visual; pembulatan hanya di KPI ringkas dan harus diberi label.
- Jangan menjumlahkan currency berbeda dalam satu angka.
- Ukuran `xl` (28px) hanya untuk total cash position per currency.

## Token

`fin-credit`, `fin-debit`, `text`, gaya tipografi `amount` dan `amount-xl`.

## Aksesibilitas

Teks aksesibel menyebut arah: "Credit IDR 25.000.000,00". Tanda minus memakai karakter minus (U+2212), bukan tanda hubung.
