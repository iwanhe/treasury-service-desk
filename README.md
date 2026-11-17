# Treasury Service Desk

Platform Treasury Service Desk dan Cash Position Management: ticketing bergaya agent workspace untuk tim Treasury, registry rekening bank, pemrosesan bank statement (CSV/XLSX) dengan approval maker-checker, dan dashboard posisi kas.

> Status: tahap desain. Repo ini baru berisi dokumentasi dan design system; belum ada kode aplikasi.

## Ruang lingkup

- **Service desk:** tiket Treasury, thread percakapan, catatan internal, SLA.
- **Rekening bank:** registry rekening per company, nomor tersamar, template import per bank.
- **Bank statement:** upload CSV/XLSX, validasi, approval maker-checker, posting. Statement yang sudah diposting tidak dapat diubah (hanya Reverse atau Adjust).
- **Cash position:** saldo per rekening dan per mata uang, dengan tiga jenis saldo (Bank reported, Calculated, Reconciled) dan penanda data stale.
- **Administrasi:** pengguna dan role, approval matrix, import mapping, kebijakan SLA, company dan grup.

## Rencana stack

Next.js, Tailwind CSS, shadcn/ui, Radix, Lucide, TanStack Table. Antarmuka berbahasa Indonesia.

## Struktur repo

| Path | Isi |
| --- | --- |
| `docs/09-design-system/` | Design system: token, pola UI, dan komponen |
| `docs/09-design-system/README.md` | Panduan merek: prinsip, aturan finansial, aksesibilitas, pemetaan shadcn |
| `docs/09-design-system/tokens.json` | Sumber token (warna, tipografi, spasi, radius, elevasi), terang dan gelap |
| `docs/09-design-system/tokens.css` | CSS variable hasil generate dari `tokens.json` |
| `docs/09-design-system/ui-patterns.md` | Pola antarmuka lintas komponen |
| `docs/09-design-system/components/` | Satu folder per komponen atau halaman contoh, berisi `README.md` dan `preview.html`; gaya bersama di `bundle.css` |

## Melihat preview

Setiap `components/<Nama>/preview.html` memuat `tokens.css` dan `bundle.css` lewat tautan relatif, jadi dapat dibuka langsung di browser tanpa build. Tema gelap memakai atribut `data-theme="dark"` pada elemen akar.

## Aturan inti design system

- Tiga jenis saldo selalu dipisahkan dan diberi label; nilai tidak dijumlahkan lintas mata uang.
- Setiap angka disertai tanggal "per" dan penanda stale bila data lama.
- Debit dan credit dibedakan dengan tanda +/− dan ikon, bukan warna saja.
- Nomor rekening tersamar (`•••• 4417`).
- Maker tidak boleh menyetujui pekerjaannya sendiri; tombol Approve nonaktif disertai alasan.
- Format angka id-ID (`IDR 485.000.000,00`).

## Tahap berikutnya

Menerjemahkan token dan komponen ke React/shadcn/ui, dimulai dari token, Button, Amount, dan TransactionTable.

## Catatan

Seluruh data pada preview adalah data ilustrasi. Ikon pada preview digambar manual dengan gaya Lucide dan akan diganti dengan paket Lucide saat implementasi. Belum ada logo atau nama merek final.
