Notifikasi sementara untuk hasil aksi ringan.

## Varian

| Varian | Dipakai untuk | Role |
| --- | --- | --- |
| Success | Balasan terkirim, tiket di-assign, filter disimpan | `status` |
| Error | Aksi gagal dan perlu dicoba ulang | `alert` |
| Info | Perubahan di latar belakang, misalnya import selesai diproses | `status` |

## Aturan

- Ikon, judul, dan satu kalimat isi. Warna hanya penguat.
- Toast sukses hilang setelah sekitar 5 detik; toast error tetap sampai ditutup.
- Hasil aksi finansial (Post, Approve, Reject, Reverse) tidak boleh hanya berupa toast: status juga tampil permanen di halaman dan di audit trail.
- Toast tidak menampung aksi destruktif atau Undo untuk transaksi yang sudah diposting.
- Pesan error spesifik dan memuat langkah berikutnya: "Statement gagal diposting. Tidak ada transaksi yang tercatat. Coba lagi atau hubungi administrator."
- Posisi kanan atas, tumpuk maksimal tiga.

## Token

`surface`, `border`, `elevation-2`, `radius-md`, `success-text`, `danger-text`, `primary-text`.
