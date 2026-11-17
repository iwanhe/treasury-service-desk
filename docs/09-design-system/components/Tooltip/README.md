Tooltip generik untuk penjelasan singkat pada ikon, singkatan, dan kontrol nonaktif.

## Aturan
- Isinya satu kalimat pendek, tanpa tautan, tombol, atau informasi penting. Hal yang wajib dibaca pengguna tidak boleh hanya ada di tooltip.
- Muncul saat hover dan saat fokus keyboard; hilang dengan Esc. Pemicu menunjuk ke tooltip lewat `aria-describedby`.
- Tombol nonaktif tetap dapat diberi fokus (`aria-disabled`) agar alasannya terbaca, contohnya "Maker tidak dapat menyetujui statement miliknya sendiri".
- Tombol ikon tanpa teks wajib punya `aria-label` selain tooltip.
- Warna terbalik (latar teks, isi surface) agar kontras sama di light dan dark. Posisi default di atas, berpindah otomatis bila terpotong.
- Tooltip chart memakai komponen terpisah (DailyMovementChart) karena memuat nilai terstruktur.
