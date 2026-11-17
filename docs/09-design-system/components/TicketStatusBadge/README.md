Badge status dan prioritas tiket dengan ikon dan teks.

## Status

| Status | Token | Ikon |
| --- | --- | --- |
| Open, In Progress | `status-open` | Lingkaran |
| Pending (Waiting for Requester, Bank, Internal Team) | `status-pending` | Jeda |
| Resolved | `status-resolved` | Centang |
| Closed, Cancelled | `status-closed` | Kunci |
| Urgent (prioritas) | `priority-urgent` | Segitiga peringatan |

## Aturan

- Selalu ikon dan teks; tidak pernah warna saja.
- Pending menampilkan sub-reason bila ada: "Pending · Waiting for Bank".
- Urgent adalah prioritas, bukan status; tampil di sebelah badge status, bukan menggantikannya.
- Jangan dipakai untuk status statement (lihat StatementStatus).

## Aksesibilitas

Teks badge dibaca apa adanya. Ikon bersifat dekoratif (`aria-hidden`).
