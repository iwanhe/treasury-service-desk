Indikator sisa waktu SLA pada baris tiket dan detail tiket.

## Keadaan

| Keadaan | Token | Teks contoh |
| --- | --- | --- |
| Aman | `text-muted` | SLA 3 j 20 m |
| At risk | `sla-warning` | Mendekati breach · 42 m |
| Breach | `sla-breach` | Breach · lewat 1 j 05 m |
| Dijeda | `status-pending` | SLA dijeda · Waiting for Bank |

## Aturan

- Selalu ikon jam dan teks waktu; angka sisa waktu rata kiri dengan `tabular-nums`.
- Ambang at risk mengikuti kebijakan SLA yang dikonfigurasi, bukan nilai tetap di komponen.
- Jeda dan lanjut mengikuti kebijakan pause/resume SLA; keadaan dijeda harus terlihat.
- Jangan membedakan at risk dan Pending hanya dengan warna; teks dan ikon berbeda.

## Aksesibilitas

Keadaan dibacakan lewat teks. Perubahan keadaan ke breach diumumkan dengan `aria-live="polite"` pada detail tiket.
