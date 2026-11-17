Contoh halaman konfigurasi kebijakan SLA (Administrasi).

## Komposisi
Tabel kebijakan per prioritas dengan target respons pertama dan target resolusi, jam kerja yang dipakai, dan ambang peringatan (persentase waktu terpakai sebelum status "Hampir lewat"). Panel pratinjau menunjukkan bagaimana tiket contoh akan tampil.

## Aturan
- Waktu SLA dihitung di server pada jam kerja yang dikonfigurasi, dan dijeda saat status Pending.
- Perubahan kebijakan berlaku untuk tiket baru; tiket berjalan tetap memakai kebijakan saat dibuat, agar riwayat tidak berubah.
- Satuan selalu eksplisit ("4 jam kerja", bukan "4").
- Perubahan dicatat di audit trail dengan nilai lama dan baru.
- Ambang peringatan harus lebih kecil dari 100%; validasi ditampilkan di bawah kolom.
