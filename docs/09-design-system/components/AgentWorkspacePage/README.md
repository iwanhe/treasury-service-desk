Contoh halaman agent workspace tiga kolom, menyusun SidebarNav, TicketListItem, TicketThread, Tabs, dan metadata tiket.

## Komposisi

- Kiri: SidebarNav, lebar `layout-nav` 220px.
- Tengah: panel daftar tiket, lebar `layout-list` 380–440px; baris `row-compact` 44px; header berisi judul tampilan, hitungan, dan filter ringkas.
- Kanan: detail tiket fleksibel. Header memuat subjek, ticket number (mono), badge status dan prioritas, SLA, dan aksi (Assign, Resolve). Di bawahnya Tabs (Percakapan, Riwayat, Terkait, Lampiran), thread, composer, dan panel metadata.

## Perilaku responsif

Desktop menampilkan tiga kolom bersamaan. Tablet: navigasi menjadi drawer, daftar dan detail berdampingan. Mobile: daftar, lalu detail sebagai layar terpisah dengan tombol Kembali.

## Aturan

- Topbar (pencarian global, notifikasi, profil) berada di luar komposisi ini dan memakai tinggi tetap.
- Memilih tiket tidak memuat ulang daftar dan mempertahankan posisi gulir.
- Aksi massal muncul sebagai bar di atas daftar saat satu atau lebih baris dipilih.

Halaman contoh ini memakai data ilustrasi.
