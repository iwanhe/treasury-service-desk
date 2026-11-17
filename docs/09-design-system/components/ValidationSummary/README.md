Ringkasan hasil validasi import statement: daftar pemeriksaan dan rumus saldo.

## Pemeriksaan

File (tipe, ukuran, malware scan), duplikat import, format tanggal dan angka, debit dan credit, opening balance, closing balance.

## Aturan

- Setiap pemeriksaan: ikon, nama, hasil dalam teks, dan jumlah baris terdampak. Hijau, kuning, merah selalu disertai ikon berbeda (centang, segitiga, silang).
- Selisih closing balance tampil sebagai tiga angka: hasil hitung (Opening + Credit − Debit), closing di statement, dan selisih. Toleransi pembulatan per currency ditulis jika dipakai.
- Closing balance tidak cocok: tombol Submit for Approval nonaktif dengan alasan di bawah ringkasan.
- Baris bermasalah dapat dibuka ke Validation Queue dengan tautan "Lihat N baris".

## Token

`success-text`, `warning-text`, `danger-text`, `border`, `text-muted`, gaya `amount`.
