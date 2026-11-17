Menu aksi yang muncul dari tombol "Aksi lainnya" pada baris atau header.

## Aturan

- Item berupa kata kerja. Aksi destruktif atau finansial (Reject, Reverse) dipisah dengan garis dan memakai `danger-text`, selalu dengan ikon dan teks.
- Item yang tidak diizinkan tetap tampil, `aria-disabled="true"`, dengan alasan pada tooltip atau teks bantu, supaya pengguna tahu aksinya ada tetapi dikunci (misalnya Approve oleh Maker).
- Pola ARIA menu: `role="menu"` dan `role="menuitem"`. Panah atas dan bawah berpindah item, Enter memilih, Escape menutup dan mengembalikan fokus ke pemicu.
- Aksi pada statement Posted hanya Reverse dan Adjust; tidak ada Edit atau Delete.
- Menu memakai `elevation-2` karena melayang di atas konten.

## Token

`surface`, `border`, `elevation-2`, `radius-md`, `surface-subtle`, `danger-text`, `focus-ring`.
