Pemilih tanggal tunggal dan rentang untuk filter, tanggal statement, dan value date.

## Komposisi
Input teks dengan format `DD/MM/YYYY` (selalu bisa diketik) dan kalender popover. Header bulan dengan tombol sebelumnya/berikutnya, grid 7 kolom mulai Senin, footer dengan "Hari ini" dan "Terapkan".

## Status sel
| Status | Tampilan |
| --- | --- |
| Hari ini | Garis tepi tebal dan teks tebal |
| Awal/akhir rentang | Isi primary dengan teks putih |
| Di dalam rentang | Isi primary-subtle |
| Dinonaktifkan | Teks muted dan dicoret, dengan alasan di tooltip |
| Di luar bulan | Teks muted |

## Aturan
- Input teks adalah jalur utama; kalender hanya alat bantu. Format salah menampilkan error di bawah input, bukan menghapus nilai.
- Tanggal tidak boleh ditebak: selalu tampil `17 Nov 2026` di luar input, tidak `17/11`.
- Tanggal setelah hari ini dinonaktifkan untuk tanggal statement; alasannya muncul di tooltip.
- Preset rentang tersedia di luar kalender: Hari ini, 7 hari, Bulan ini.
- Keyboard: panah menggeser hari, PageUp/PageDown pindah bulan, Enter memilih, Esc menutup dan mengembalikan fokus ke input.
- Zona waktu mengikuti perusahaan; sel tidak menampilkan jam.
