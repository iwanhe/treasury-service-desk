Garis waktu alur statement: upload, validasi, pengajuan, review Checker, posting.

## Keadaan langkah

| Keadaan | Penanda |
| --- | --- |
| Selesai | Titik hijau dengan ikon centang; pelaku dan waktu |
| Sedang berjalan | Titik violet (`approval`) dengan ikon perisai; menyebut siapa yang ditunggu |
| Belum | Titik netral dengan ikon kosong; tanpa pelaku |
| Ditolak | Titik merah dengan ikon silang; alasan tampil |

## Aturan

- Setiap langkah memuat nama langkah, pelaku (Maker, Checker, Sistem), dan waktu. Pelaku dan waktu berasal dari audit trail.
- Penanda tidak hanya warna: ikon dan teks status berbeda untuk setiap keadaan.
- Alur Controlled mode menampilkan semua langkah; Automatic mode tetap menampilkan langkah posting dan audit, dengan keterangan kebijakan yang dipakai.
- Hanya baca. Aksi Approve dan Reject berada di luar timeline.

## Token

`success-text`, `success-subtle`, `approval`, `approval-bg`, `border-strong`, `text-muted`.
