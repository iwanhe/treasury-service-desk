Navigasi kiri agent workspace, lebar `layout-nav` 220px.

## Struktur

Mengikuti struktur navigasi produk: Workspace (Overview, Unified Inbox, My Tickets, Team Tickets, Unassigned, Pending Approval, SLA at Risk), Bank Accounts, Bank Statements, Treasury Dashboard, Reports, Administration. Menu yang tidak diizinkan untuk role pengguna tidak ditampilkan.

## Aturan

- Item aktif: latar `primary-subtle`, teks `primary-text`, dan `aria-current="page"`. Aktif tidak hanya ditandai warna: ikon dan label tetap sama, sehingga bentuk latar yang membawa penanda; di mode kontras tinggi ditambah outline.
- Hitungan (count) di kanan: netral untuk antrean biasa, `approval` untuk Pending Approval, `sla-warning` untuk SLA at Risk. Angka selalu tertulis.
- Ikon 20px, stroke 1.75, selalu dengan label teks.
- Tinggi item minimal 36px. Fokus keyboard memakai outline `focus-ring`.
- Pada tablet dan mobile, navigasi menjadi drawer dan panel berpindah bertahap.

## Token

`surface`, `border`, `surface-subtle`, `primary-subtle`, `primary-text`, `approval`, `sla-warning`, `layout-nav`, `radius-md`.
