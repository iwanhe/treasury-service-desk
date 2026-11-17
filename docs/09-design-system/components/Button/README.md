Tombol aksi dengan empat varian: primary, secondary, ghost, danger.

## Kapan dipakai

| Varian | Dipakai untuk |
| --- | --- |
| Primary | Satu aksi utama per area: Kirim Balasan, Submit for Approval, Approve |
| Secondary | Aksi pendukung: Simpan Draft, Assign, Export |
| Ghost | Aksi ringan di baris atau toolbar: Lihat Detail, Batal |
| Danger | Aksi destruktif atau penolakan: Reject, Reverse |

## Aturan

- Maksimal satu tombol primary per area.
- Tombol nonaktif karena kontrol bisnis (misalnya Approve oleh maker) wajib menampilkan alasan lewat teks bantu atau tooltip, bukan sekadar abu-abu.
- Label memakai kata kerja. Aksi Post dan Reverse selalu meminta konfirmasi.
- Tinggi 36px (default) atau 28px (`sm`, di baris tabel).

## Token

`primary`, `primary-hover`, `primary-subtle`, `primary-text`, `danger-solid`, `text-on-solid`, `border-strong`, `focus-ring`, `radius-md`.

## Aksesibilitas

Elemen `<button>`. Fokus memakai outline 2px. Tombol nonaktif memakai atribut `disabled` dan `aria-describedby` ke alasannya.
