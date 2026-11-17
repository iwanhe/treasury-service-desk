Tampilan saat daftar atau halaman belum memiliki data, atau pengguna tidak berwenang.

## Variasi

| Keadaan | Pesan | Aksi |
| --- | --- | --- |
| Belum ada data | Satu kalimat yang menjelaskan apa yang kosong dan mengapa | Satu aksi utama, misalnya Upload Statement |
| Hasil filter kosong | "Tidak ada tiket yang cocok dengan filter" | Reset filter |
| Tidak berwenang | "Anda tidak memiliki akses ke company ini" (HTTP 403) | Hubungi administrator |
| Gagal memuat | Pesan spesifik, bukan "Terjadi kesalahan" | Coba lagi |

## Aturan

- Tanpa ilustrasi dekoratif; ikon 24px dan teks cukup.
- Akses ditolak tidak boleh ditampilkan sebagai data kosong, karena akan menyamarkan masalah otorisasi.
- Judul satu baris, isi maksimal dua kalimat, satu tombol.

## Token

`surface`, `border`, `radius-lg`, `space-10`, `text-muted`.
