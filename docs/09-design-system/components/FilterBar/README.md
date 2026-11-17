Satu baris filter di atas halaman: rentang tanggal, company, bank, currency.

## Aturan

- Satu baris, rata kiri, di atas konten yang dicakupnya; tidak di dalam kartu dan tidak per widget. Seluruh widget di bawahnya memakai irisan data yang sama.
- Rentang tanggal lebih dulu, dengan preset (Hari ini, 7 hari, 30 hari, 90 hari) sebelum rentang kustom.
- Preset terpilih memakai `aria-pressed="true"` dan latar `primary-subtle`; hover tidak menyaingi seleksi.
- Filter company hanya menampilkan company yang diotorisasi bagi pengguna. Memilih satu currency membatasi total ke currency itu.
- Saat data dimuat ulang, tampilan sebelumnya dipertahankan dengan opasitas lebih rendah, tanpa skeleton dan tanpa lonjakan layout.
- Filter aktif dapat dihapus satu per satu, dan tombol "Reset" mengembalikan ke default.

## Token

`border-strong`, `surface`, `surface-subtle`, `primary-subtle`, `primary-text`, `focus-ring`, `radius-md`.
