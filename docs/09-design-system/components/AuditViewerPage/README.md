Contoh halaman Audit Viewer (SCR-015) untuk Auditor: histori perubahan hanya baca.

## Komposisi

- FilterBar: rentang tanggal, pelaku, jenis aksi, jenis entitas.
- Tabel kejadian: waktu (UTC dengan tampilan zona pengguna), pelaku, aksi, entitas, ID entitas (mono), ringkasan.
- Baris dapat dibuka untuk melihat sebelum dan sesudah per field; tampilan memakai font mono.
- Aksi halaman hanya Export; tidak ada Edit atau Delete.

## Aturan

- Log tidak dapat diubah dari aplikasi; halaman memuat keterangan itu di atas tabel.
- Posting statement, approval, reject, reversal, perubahan konfigurasi rekening, dan perubahan role semuanya tercatat dengan pelaku.
- Data finansial pada detail audit hanya field yang diperlukan; nomor rekening tetap masking.
- Hasil filter ditampilkan lengkap dengan jumlah total; ekspor membawa filter yang sama.

Halaman ini memakai data ilustrasi.
