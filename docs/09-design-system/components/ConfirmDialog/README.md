Dialog konfirmasi untuk aksi yang tidak dapat dibatalkan atau berdampak finansial: Post, Reverse, Reject.

## Isi

Judul berupa kata kerja dan objek ("Post statement?"), ringkasan yang dapat diperiksa (rekening, periode, jumlah transaksi, closing balance), kalimat dampak ("Setelah diposting, statement tidak dapat diubah atau dihapus. Koreksi hanya lewat Reverse atau Adjust."), dan dua tombol.

## Aturan

- Tombol aksi memakai label yang sama dengan judul ("Post Statement"), bukan "Ya" atau "OK". Reject dan Reverse memakai varian danger dan meminta alasan (wajib, minimal satu kalimat).
- Fokus awal pada tombol Batal untuk aksi destruktif; Escape menutup dialog dan fokus kembali ke pemicu.
- Dialog memakai `role="dialog"`, `aria-modal="true"`, `aria-labelledby` ke judul, dan perangkap fokus.
- Setelah aksi, hasilnya tidak hanya muncul sebagai toast: status baru tampil di halaman (ApprovalBanner atau StatementStatus) dan tercatat di audit trail.
- Tombol aksi dinonaktifkan selama permintaan berjalan dan mengirim idempotency key, sehingga klik ganda tidak menghasilkan posting ganda.

## Token

`surface`, `border`, `elevation-2`, `radius-lg`, `danger-solid`, `primary`, `space-6`.
