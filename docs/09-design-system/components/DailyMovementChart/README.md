Grafik batang berkelompok pergerakan kas harian: Credit dan Debit per tanggal, untuk satu currency.

## Aturan

- Satu currency per grafik. Currency berbeda berarti grafik terpisah (small multiples), tidak pernah dua sumbu.
- Dua seri: `chart-credit` (biru) dan `chart-debit` (jingga). Warna ini dipilih agar tetap terbedakan pada buta warna merah-hijau; identitas tidak bergantung warna karena legend selalu ada dan tooltip menyebut nama seri.
- Batang maksimal 24px, ujung data membulat 4px, dasar rata, celah 2px antar batang, mulai dari nol.
- Label nilai hanya pada puncak tertinggi; selebihnya lewat sumbu, tooltip, dan tampilan tabel.
- Tooltip menampilkan kedua seri pada tanggal itu (nilai tebal, nama seri sekunder), muncul juga saat fokus keyboard.
- Tombol "Lihat sebagai tabel" menampilkan data yang sama sebagai tabel, sehingga tidak ada nilai yang hanya tersedia lewat hover.
- Teks (sumbu, label, legend) memakai token teks, bukan warna seri.
- Satuan sumbu ditulis di judul grafik ("juta IDR").

## Token

`chart-credit`, `chart-debit`, `border` (grid), `text`, `text-muted`, `surface`, `elevation-2`.
