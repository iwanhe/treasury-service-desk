Contoh halaman Users & Roles (SCR-014) untuk System Administrator.

## Komposisi

- FilterBar: pencarian, role, company, status.
- Tabel pengguna: nama, email, role (badge), akses company, status (Aktif, Nonaktif), login terakhir.
- Panel samping saat satu pengguna dipilih: role, akses company, permission efektif.

## Aturan

- Satu pengguna dapat memiliki beberapa role, tetapi otorisasi dibatasi per company dan permission; kedua hal ini tampil terpisah di panel samping.
- Peringatan terlihat bila satu pengguna memegang kombinasi yang melanggar pemisahan tugas (misalnya Maker dan Checker pada rekening yang sama).
- Menonaktifkan pengguna tidak menghapus riwayatnya; tidak ada hard delete.
- Setiap perubahan role atau akses company tercatat di audit trail dengan pelaku.
- Autentikasi lewat OIDC; halaman ini tidak menyimpan atau menampilkan kata sandi.

Halaman ini memakai data ilustrasi.
