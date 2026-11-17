Contoh halaman Reconciliation (SCR-012): memeriksa saldo dan integritas transaksi satu statement.

## Komposisi

- Tiga sel di atas: **Bank reported**, **Calculated**, dan **Selisih**. Selisih nol memakai `reconciled-bg` dengan ikon centang ganda; selisih tidak nol memakai `danger-subtle` dengan ikon silang dan angka selisihnya.
- Daftar pemeriksaan: kesinambungan opening dengan closing statement sebelumnya, total credit dan debit, closing balance, duplikat transaksi, transaksi tanpa sumber.
- Tabel item reconciliation dengan status per item: Matched atau Unmatched (disertai alasan).
- Aksi: Tandai Reconciled hanya aktif bila selisih nol dan tidak ada item Unmatched; pelaku dicatat di audit trail.

## Aturan

- MVP berfokus pada balance dan transaction integrity; pencocokan dengan Oracle EBS atau SAP masuk rilis berikutnya dan tidak ditampilkan.
- Tiga jenis saldo tidak dicampur; Reconciled hanya muncul setelah pemeriksaan selesai dan dinyatakan cocok.
- Item Unmatched tidak dikoreksi dari halaman ini; koreksi lewat Reverse atau Adjust dengan referensi transaksi asli.

Halaman ini memakai data ilustrasi.
