Avatar pengguna berisi inisial, untuk requester, assignee, dan pelaku di audit trail.

## Aturan

- Inisial dua huruf dari nama; ukuran 24px (baris padat), 32px (default), 40px (header detail).
- Tidak ada warna acak per pengguna: semua avatar memakai `primary-subtle`. Warna acak akan bentrok dengan token status.
- Belum di-assign: avatar kosong berborder putus-putus dengan teks "Belum di-assign" di sebelahnya, bukan avatar abu-abu tanpa label.
- Avatar selalu didampingi nama atau `aria-label`; tidak berdiri sendiri sebagai satu-satunya identitas.
- Foto profil tidak dipakai di MVP.

## Token

`primary-subtle`, `primary-text`, `surface-subtle`, `border-strong`, `radius-full`.
