Baris tiket pada daftar kolom tengah agent workspace.

## Isi

Subjek (satu baris, terpotong), ticket number (mono), requester dan company, badge status, badge prioritas bila Urgent, indikator SLA, waktu pembaruan terakhir, assignee.

## Keadaan

| Keadaan | Tampilan |
| --- | --- |
| Default | Latar `surface`, border bawah |
| Belum dibaca | Subjek tebal (600) dan titik penanda dengan teks tersembunyi "Belum dibaca" |
| Terpilih | Latar `primary-subtle` dan outline 2px `primary` |
| Fokus keyboard | Outline `focus-ring` |

## Aturan

- Tinggi minimal `row-compact` 44px pada mode compact.
- Maksimal tiga baris metadata; kelebihan dipotong, detail ada di panel kanan.
- Tiket yang melanggar SLA tidak diubah warna latarnya; indikator SLA yang membawa informasinya.
- Mendukung seleksi massal lewat checkbox untuk bulk update.
