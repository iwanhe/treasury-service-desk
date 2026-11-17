Contoh halaman Import Mapping (Administrasi): template parser per bank, dengan versi.

## Komposisi

- Header: nama template, bank, versi aktif, status (Aktif, Draft).
- Aturan format: format tanggal, pemisah desimal, pemisah ribuan, mode debit/credit (dua kolom atau satu kolom dengan indikator), jumlah baris header yang dilewati.
- Tabel mapping: kolom di file sumber ke field kanonik (tanggal transaksi, value date, deskripsi, reference, debit, credit, running balance). Field wajib ditandai dengan teks "wajib".
- Pratinjau hasil parsing atas contoh baris, sehingga kesalahan format terlihat sebelum template diaktifkan.

## Aturan

- Mengubah template selalu membuat versi baru; import lama tetap merujuk versi yang dipakainya, sehingga histori tidak rusak.
- Template Draft tidak dapat dipakai untuk upload; mengaktifkan memerlukan pengguna dengan izin konfigurasi.
- Angka diproses dengan decimal arithmetic; pratinjau menampilkan hasil sebagai teks desimal, bukan float.
- Nilai negatif ditangani eksplisit lewat mode debit/credit yang dipilih.

Halaman ini memakai data ilustrasi.
