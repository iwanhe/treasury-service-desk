Placeholder saat data dimuat.

## Aturan

- Dipakai untuk muatan pertama sebuah daftar atau kartu; bentuknya mengikuti baris atau kartu aslinya (tinggi `row-compact`), agar layout tidak melompat.
- Untuk muat ulang akibat filter, pertahankan tampilan sebelumnya dengan opasitas lebih rendah, bukan skeleton.
- Tabel tidak memakai spinner. Angka finansial tidak boleh ditampilkan sebagai nol selama memuat.
- Animasi denyut pelan; dimatikan bila pengguna memilih `prefers-reduced-motion`.
- Wadah memakai `aria-busy="true"` dan teks tersembunyi "Memuat".

## Token

`border` (warna blok), `radius-sm`, `row-compact`.
