Contoh halaman Approval Matrix (Administrasi): siapa boleh melakukan apa pada statement.

## Komposisi

Tabel aktivitas terhadap role (Maker, Checker, Supervisor, Manager), mengikuti matriks pada spesifikasi: Upload, Validate, Approve, Reject, Post, Configure account, View cash position.

## Penanda sel

| Penanda | Arti | Tampilan |
| --- | --- | --- |
| Boleh | Role dapat melakukan aktivitas | Ikon centang dan teks "Ya" |
| Tidak | Role tidak dapat melakukan | Ikon silang dan teks "Tidak" |
| Berdasarkan permission | Boleh bila permission diberikan | Ikon centang dan teks "Ya*" |
| Sistem | Dijalankan otomatis oleh sistem | Ikon roda gigi dan teks "Sistem" |

## Aturan

- Keterangan di bawah tabel: "* Berdasarkan permission yang diberikan."
- Aturan wajib ditampilkan di atas tabel: pengguna tidak boleh menyetujui pekerjaannya sendiri; bila tidak ada Checker lain, statement tetap menunggu dan tidak diposting.
- Mode statement (Controlled atau Automatic) dikonfigurasi per rekening, dengan Controlled sebagai default; Automatic hanya untuk rekening yang diuji dan disetujui Treasury Manager.
- Perubahan matriks dicatat di audit trail, dan hanya pengguna dengan izin konfigurasi yang dapat mengubahnya.

Halaman ini memakai data ilustrasi.
