Banner pada halaman statement yang menjelaskan posisi alur maker-checker dan siapa yang dapat bertindak.

## Varian

| Varian | Dipakai saat |
| --- | --- |
| Approval (violet) | Statement menunggu Checker |
| Danger | Statement ditolak (alasan tampil), atau pengguna tidak boleh approve karena maker |
| Success | Statement Posted dan saldo diperbarui |

## Aturan

- Judul menyebut status dan siapa yang bertindak berikutnya: "Menunggu Checker".
- Isi menyebut maker, waktu pengajuan, dan jika ada alasan penolakan.
- Jika pengguna adalah maker, banner menerangkan bahwa Checker lain harus menyetujui, dan tombol Approve nonaktif.
- Bukan toast: banner tetap tampil selama status berlaku.

## Token

`approval`, `approval-bg`, `danger-subtle`, `danger-text`, `success-subtle`, `success-text`, `radius-lg`.

## Aksesibilitas

`role="status"` untuk Approval dan Success; `role="alert"` untuk Danger.
