# Pola layar

Pemetaan layar pada spesifikasi (SCR-001 sampai SCR-015) ke pola desain. Semua pola memakai token dari sistem ini.

## Agent workspace (SCR-002, SCR-003, SCR-004)

- Topbar: pencarian global, notifikasi, profil.
- Kolom kiri `layout-nav` 220px: Workspace, Bank Accounts, Bank Statements, Treasury Dashboard, Reports, Administration, serta saved views.
- Kolom tengah `layout-list` 380–440px: daftar tiket sebagai tabel (default) atau kartu. Baris `row-compact` 44px berisi subjek, requester, status, prioritas, indikator SLA.
- Kolom kanan: percakapan, private note, metadata (company, rekening terkait, assignee, group).
- Private note memakai latar `warning-subtle` dan label "Hanya internal" agar tidak tertukar dengan balasan publik.

## Buat tiket (SCR-005)

Form satu kolom. Field: company (hanya yang diotorisasi), category dan subcategory, subjek, deskripsi, prioritas, lampiran, rekening terkait (opsional). Error ditampilkan di bawah field dengan `danger-text` dan ikon.

## Daftar dan detail rekening (SCR-006, SCR-007)

Tabel: company, bank, nomor masking, currency, saldo, tanggal saldo, status. Kolom saldo memakai komponen BalanceCard atau Amount. Rekening tanpa statement terbaru menampilkan penanda stale.

## Upload statement (SCR-008, SCR-009)

Empat area berurutan:

1. Account selector: company, bank, rekening.
2. Upload zone: CSV atau XLSX, batas ukuran, periode.
3. Import preview: hasil parsing dan mapping kolom.
4. Validation summary: error, warning, duplikat, selisih saldo. Selisih ditampilkan sebagai tiga angka (Opening + Credit − Debit, hasil hitung, Closing di statement).

Statement dengan closing balance tidak cocok tidak dapat diajukan; tombol Submit for Approval nonaktif dengan alasan.

## Approval statement (SCR-010)

ApprovalBanner di atas, ringkasan saldo dan jumlah transaksi, tabel transaksi, lalu aksi Approve dan Reject (alasan wajib). Jika pengguna adalah maker, Approve nonaktif dengan alasan.

## Dashboard cash position (SCR-011)

Widget: Total Cash Position per currency, Bank Account Summary, Company Cash Position, Daily Cash Movement, Latest Statement, Pending Approval, Ticket Backlog, SLA at Risk. Setiap kartu nominal memuat tanggal saldo dan jenis saldo (Reconciled sebagai default).

## Reconciliation (SCR-012)

Dua kolom: saldo Bank reported dan Calculated. Selisih tampil di tengah dengan Amount. Item tidak cocok memakai `danger-subtle`; item cocok memakai badge Reconciled.

## Administrasi dan audit (SCR-014, SCR-015)

Tabel padat dengan filter. Audit Viewer hanya baca: tidak ada aksi ubah atau hapus, hanya ekspor.

## State umum

| State | Perilaku |
| --- | --- |
| Loading | Skeleton setinggi baris, tanpa spinner untuk tabel |
| Empty | Satu kalimat penjelas dan satu aksi utama |
| Error | Pesan spesifik, bukan "Terjadi kesalahan", plus aksi coba lagi |
| Stale | Penanda stale pada nominal, bukan banner halaman |
| Tidak berwenang | HTTP 403 ditampilkan sebagai halaman akses ditolak, bukan data kosong |
