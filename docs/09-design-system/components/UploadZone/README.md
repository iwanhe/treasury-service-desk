Area unggah file statement (CSV atau XLSX) dan daftar file yang dipilih.

## Keadaan

| Keadaan | Tampilan |
| --- | --- |
| Default | Border putus-putus, instruksi, tipe dan batas ukuran file |
| Drag aktif | Border solid `primary` dan latar `primary-subtle`, teks "Lepas file untuk mengunggah" |
| File dipilih | Baris file: nama, ukuran, checksum singkat, aksi Hapus dan Ganti |
| Ditolak | Pesan error spesifik: tipe tidak didukung, ukuran melebihi batas, duplikat |

## Aturan

- Tombol "Pilih File" selalu tersedia; drag-and-drop adalah tambahan, bukan satu-satunya cara.
- Zona ini baru aktif setelah company dan rekening dipilih; jika belum, tampilkan alasan.
- Pesan duplikat menyebut statement yang sudah ada dan statusnya.
- Hasil validasi keamanan file (tipe, ukuran, malware scan) tampil sebagai langkah terpisah sebelum parsing.

## Aksesibilitas

Zona dapat difokus dan dibuka dengan Enter atau Spasi. Status unggah diumumkan lewat `aria-live="polite"`.
