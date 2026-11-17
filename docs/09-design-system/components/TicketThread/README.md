Percakapan tiket pada panel detail: balasan publik, catatan internal, peristiwa sistem, dan composer.

## Jenis entri

| Jenis | Tampilan | Terlihat oleh |
| --- | --- | --- |
| Pesan requester | Kartu `surface` | Requester dan agent |
| Balasan agent (publik) | Kartu `primary-subtle` | Requester dan agent |
| Catatan internal | Kartu `warning-subtle`, border putus-putus, label "Catatan internal" dengan ikon kunci | Hanya agent dan supervisor |
| Peristiwa sistem | Satu baris kecil, teks `text-muted`: perubahan status, assignee, SLA, escalation | Sesuai kebijakan |

## Aturan

- Catatan internal harus tidak mungkin tertukar dengan balasan publik: latar, border, label teks, dan ikon berbeda; di composer tab Balas dan Catatan memakai label jelas dan tombol kirim berganti teks ("Kirim Balasan" atau "Simpan Catatan").
- Setiap entri memuat avatar, nama, dan waktu (rata kanan, `tabular-nums`).
- Peristiwa sistem merekam perubahan status, assignee, prioritas, dan SLA sesuai kebutuhan ticket history, dan memuat pelaku.
- Lampiran tampil sebagai baris file di bawah pesan, dengan nama dan ukuran.
- Pesan baru diumumkan lewat `aria-live="polite"` pada daftar.
- Composer: textarea dengan fokus terlihat; mengirim balasan pada tiket Resolved membuka kembali tiket (aksi Reopen) dan harus diberi tahu.

## Token

`surface`, `primary-subtle`, `warning-subtle`, `warning-text`, `border`, `border-strong`, `text-muted`, `radius-lg`.
