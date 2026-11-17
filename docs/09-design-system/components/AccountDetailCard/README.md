Kartu detail rekening bank: identitas, tiga jenis saldo, mode statement, dan status data.

## Komposisi
- Header: nama rekening, bank, company, nomor tersamar (`•••• 4417`), mata uang.
- Tiga saldo berlabel: Bank reported, Calculated, Reconciled, masing-masing dengan tanggal "per".
- Mode statement (Controlled atau Automatic) dan template import aktif beserta versinya.
- Status data: Reconciled, atau Stale dengan tanggal terakhir.
- Aksi: Upload statement, Lihat transaksi, Konfigurasi (hanya untuk izin yang sesuai).

## Aturan
- Nomor rekening penuh hanya dapat dilihat lewat aksi khusus yang tercatat di audit trail.
- Tidak ada angka gabungan lintas mata uang di kartu ini.
- Selisih ditampilkan sebagai angka dan teks, bukan hanya warna.
- Rekening Automatic menampilkan catatan bahwa disetujui Treasury Manager.
