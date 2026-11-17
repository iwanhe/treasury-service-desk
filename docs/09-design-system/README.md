# Treasury Service Desk Design System

Satu platform untuk permintaan Treasury, visibilitas bank, dan kontrol operasional.

Design system untuk **Treasury Service Desk & Cash Position Management Platform**: agent workspace bergaya Freshdesk untuk ticketing, ditambah modul rekening bank, bank statement, dan dashboard cash position. Stack target: Next.js, Tailwind, shadcn/ui, Radix, Lucide, TanStack Table. Draft ini dibangun dari Product Blueprint v1.0 dan dokumen Lanjutan Design & Implementation. Nama produk dan logo belum ditetapkan, jadi sistem ini memakai teks biasa sebagai identitas.

## Prinsip

1. **Produktivitas agent lebih dulu.** Tiga kolom (navigasi, daftar tiket, detail), baris compact 44px, aksi massal, dan pintasan keyboard.
2. **Angka finansial harus bisa dipercaya.** Setiap nilai uang menampilkan currency, tanggal saldo, dan sumbernya.
3. **Status tidak hanya warna.** Setiap status memakai ikon dan teks, sehingga tetap terbaca oleh pengguna buta warna dan pada tampilan cetak.
4. **Satu makna, satu token.** Status tiket, approval, reconciliation, SLA, dan stale masing-masing punya token semantik sendiri.
5. **Kontrol terlihat.** Maker-checker, status posting, dan audit trail muncul di antarmuka, bukan hanya di backend.

## Content fundamentals

**Bahasa.** Antarmuka berbahasa Indonesia. Istilah baku Treasury dan perbankan tetap dalam bahasa Inggris: Maker, Checker, Posted, Closing Balance, Opening Balance, Reconciled, SLA.

**Nada.** Lugas dan netral. Kalimat pendek, tanpa tanda seru, tanpa bahasa promosi.

**Tombol memakai kata kerja:** Buat Tiket, Assign, Kirim Balasan, Upload Statement, Submit for Approval, Approve, Reject, Post, Reverse.

**Format angka dan tanggal (locale id-ID):**

| Hal | Format | Contoh |
| --- | --- | --- |
| Nominal | Kode currency, titik ribuan, koma desimal | IDR 485.000.000,00 |
| Ringkasan KPI | Singkatan hanya di kartu ringkasan | Rp 180 M |
| Debit dan credit | Tanda eksplisit, tidak memakai angka negatif | + 25.000.000,00 dan − 15.000.000,00 |
| Tanggal | Tanggal singkat | 17 Nov 2026 |
| Tanggal saldo | Selalu "per" | per 17 Nov 2026 |
| Nomor rekening | Dimasking, empat digit terakhir | •••• 4417 |

**Contoh microcopy:**

- Error validasi: "Closing balance tidak cocok. Hitungan sistem IDR 110.000.000,00, tercantum di statement IDR 109.000.000,00."
- Maker mencoba approve: tombol nonaktif dengan alasan "Anda yang meng-upload statement ini. Checker lain harus menyetujui."
- Data stale: "Saldo terakhir per 14 Nov 2026. Statement 15–17 Nov belum diunggah."
- Empty state: "Belum ada statement untuk rekening ini. Upload statement CSV atau XLSX untuk memulai."

## Visual foundations

**Warna.** Primary biru `#2F6FED` untuk aksi utama. Latar `#F5F7FA`, panel putih, border `#E4E7EC`. Status memakai pasangan `-text` untuk teks dan `-subtle` untuk latar. Warna dasar success, warning, danger hanya untuk fill, ikon, dan border karena kontras sebagai teks di bawah 4.5:1. Tema dark tersedia lewat `data-theme="dark"` dan tidak membutuhkan perubahan per komponen.

**Tipografi.** Inter. Dasar 14px, tabel 13px, label 12px. Semua nominal memakai `font-variant-numeric: tabular-nums` dan rata kanan. Nomor referensi memakai font mono.

**Layout.** Agent workspace: navigasi `layout-nav` 220px, daftar tiket `layout-list` 380–440px, detail fleksibel. Tablet dan mobile berpindah ke navigasi bertahap. Tinggi baris `row-compact` 44px (default) atau `row-comfortable` 56px.

**Bentuk.** Radius 6 / 8 / 10px. Utamakan border satu piksel daripada shadow; shadow hanya untuk elemen yang melayang (dropdown, modal, toast).

**Gerak.** Minim: transisi 120–150ms untuk hover dan fokus. Tidak ada animasi pada angka finansial.

## Aturan tampilan finansial (wajib)

| Aturan | Implementasi UI |
| --- | --- |
| Tiga jenis saldo tidak dicampur | Label eksplisit: **Bank reported** (angka resmi statement), **Calculated** (hasil hitung transaksi), **Reconciled** (sudah dicocokkan). Dashboard utama menampilkan Reconciled dan menunjukkan dua lainnya. |
| Currency tidak dijumlahkan | Total selalu per currency (IDR, USD, SGD). Total gabungan hanya dengan kurs dan tanggal kurs yang jelas. |
| Saldo bukan real-time | Setiap saldo menampilkan "per [tanggal]". Jika statement hari itu belum ada, tampilkan penanda **stale** (ikon jam, border putus-putus). |
| Debit dan credit | Dua kolom terpisah di tabel transaksi. Di ringkasan, tanda + atau − beserta ikon panah, tidak bergantung pada warna. |
| Nomor rekening | Selalu masking. Nomor lengkap hanya untuk role yang diotorisasi, dengan aksi eksplisit. |
| Posted tidak bisa diubah | Statement Posted tidak punya tombol Edit atau Delete. Koreksi hanya lewat **Reverse** atau **Adjust** yang menautkan transaksi asli. |
| Maker bukan Checker | Tombol Approve nonaktif untuk maker, dengan alasan terlihat. |
| Sumber jelas | Setiap angka dapat ditelusuri ke statement sumbernya. |

## Peta token semantik

| Konsep | Token teks | Token latar | Pendamping non-warna |
| --- | --- | --- | --- |
| Tiket Open, In Progress | `status-open` | `status-open-bg` | Ikon lingkaran, teks status |
| Tiket Pending | `status-pending` | `status-pending-bg` | Ikon jeda, sub-reason |
| Tiket Resolved | `status-resolved` | `status-resolved-bg` | Ikon centang |
| Tiket Closed, Cancelled | `status-closed` | `status-closed-bg` | Ikon kunci atau silang |
| Prioritas Urgent | `priority-urgent` | `priority-urgent-bg` | Ikon peringatan, teks Urgent |
| SLA at risk | `sla-warning` | `sla-warning-bg` | Ikon jam, sisa waktu |
| SLA breach | `sla-breach` | `sla-breach-bg` | Ikon jam, teks Breach |
| Pending Approval | `approval` | `approval-bg` | Ikon perisai |
| Reconciled | `reconciled` | `reconciled-bg` | Ikon centang ganda |
| Stale | `stale` | `stale-bg` | Ikon jam, border putus-putus |
| Credit dan Debit | `fin-credit`, `fin-debit` | — | Tanda + dan − |

Status tiket Pending (amber) dan SLA at risk (jingga) berdekatan di daftar tiket. Keduanya selalu disertai ikon dan teks yang berbeda; jangan pernah membedakannya hanya dengan warna.

## Ikonografi

Lucide, stroke 1.75, 16px di baris dan badge, 20px di navigasi. Ikon status tidak berdiri sendiri: selalu ada label teks atau `aria-label`. Tidak ada emoji.

## Aksesibilitas

- Teks 4.5:1 terhadap latarnya di kedua tema. Border kontrol dan outline fokus 3:1.
- Fokus keyboard terlihat: outline 2px `focus-ring`, offset 2px.
- Seluruh alur ticket dan statement dapat dioperasikan dengan keyboard.
- Tabel memakai `<th scope>` dan angka rata kanan.
- Perubahan status tampil juga sebagai teks, tidak hanya perubahan warna.

## Pemetaan ke shadcn/ui dan Tailwind

| Variabel shadcn | Token sistem ini |
| --- | --- |
| `--background` | `bg` |
| `--card`, `--popover` | `surface` |
| `--foreground` | `text` |
| `--muted`, `--accent` | `surface-subtle` |
| `--muted-foreground` | `text-muted` |
| `--primary`, `--primary-foreground` | `primary`, `text-on-solid` |
| `--destructive` | `danger-solid` |
| `--border`, `--input` | `border`, `border-strong` |
| `--ring` | `focus-ring` |
| `--radius` | `radius-md` |

## Asumsi dan hal yang masih terbuka

- Palet dasar dan font diambil dari spesifikasi 6.1. Varian teks, latar subtle, tema dark, dan token semantik adalah turunan saya dan perlu ditinjau.
- Belum ada logo atau nama merek final.
- Keputusan §9 (apakah ada portal requester terpisah) menentukan perlu tidaknya varian layout requester; draft ini baru mencakup agent workspace dan layar Treasury.
- Komponen yang sudah ada: Button, FormField, TicketStatusBadge, SlaIndicator, TicketListItem, Amount, BalanceCard, UploadZone, ValidationSummary, TransactionTable, StatementStatus, ApprovalBanner, CashPositionTotals, DailyMovementChart, KpiTile, AccountBalanceTable, SidebarNav, FilterBar, ConfirmDialog, Toast, Tabs, DropdownMenu, Pagination, Avatar, EmptyState, Skeleton, TicketThread, ApprovalTimeline. Halaman contoh (grup Pages): AgentWorkspacePage, CashDashboardPage, StatementUploadPage, StatementApprovalPage. Belum ada: date picker kustom, tooltip generik, checkbox dan radio, kartu detail rekening, halaman reconciliation dan audit viewer.
- Grafik memakai `chart-credit` (biru) dan `chart-debit` (jingga), bukan hijau dan merah, agar terbedakan pada buta warna merah-hijau. Pada tabel dan ringkasan, credit dan debit tetap memakai `fin-credit` dan `fin-debit` dengan tanda + dan −. Dua pasang warna ini sengaja berbeda; perlu keputusan tim apakah ingin disamakan.
- Data pada preview (nominal, tanggal, nama company dan bank) hanyalah contoh.

## Menggunakan di repo ini

- `tokens.json` adalah sumber kebenaran token. `tokens.css` dihasilkan darinya (variabel CSS untuk tema `light` dan `dark`, lewat atribut `data-theme` pada elemen akar); jangan diedit tangan.
- `components/bundle.css` memuat gaya komponen referensi (kelas `tsd-*`). Ini acuan visual untuk implementasi shadcn/ui dan Tailwind, bukan kode produksi.
- Setiap `components/<Nama>/README.md` berisi pedoman; `preview.html` dapat dibuka langsung di browser (memuat `tokens.css` dan `bundle.css` secara relatif). Font Inter dimuat dari Google Fonts; ganti dengan font yang di-host sendiri bila lingkungan produksi membatasi akses keluar.
- Salinan interaktif sistem ini ada sebagai artifact di Claude. Bila token berubah, perbarui `tokens.json` lebih dulu, lalu hasilkan ulang `tokens.css`.
