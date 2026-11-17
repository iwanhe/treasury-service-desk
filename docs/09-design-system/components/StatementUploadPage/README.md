Contoh halaman Upload Statement (SCR-008 dan SCR-009) untuk Maker.

## Empat area berurutan

1. **Account selector**: company, bank, rekening (hanya yang diotorisasi). Rekening nonaktif tidak dapat dipilih.
2. **Upload zone**: CSV atau XLSX, batas ukuran, periode; daftar file terpilih dengan checksum.
3. **Import preview**: hasil parsing dan mapping kolom berdasarkan template bank (dengan versi template), beberapa baris pertama.
4. **Validation summary**: pemeriksaan file, duplikat, format, debit dan credit, opening dan closing balance, plus rumus saldo.

## Aturan

- Langkah berikutnya terbuka bertahap; langkah yang belum dapat dipakai tetap tampil dengan alasan.
- Submit for Approval nonaktif selama ada error, terutama closing balance tidak cocok. Peringatan tidak menghalangi.
- Upload tidak mengubah saldo. Teks bantu di bawah tombol menyebut bahwa saldo baru berubah setelah posting.
- Maker dapat memperbaiki dan memproses ulang; baris bermasalah dibuka di Validation Queue.

Halaman ini memakai data ilustrasi.
