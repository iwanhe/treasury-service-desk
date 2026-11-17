Badge status impor dan posting bank statement.

## Status

| Status | Token | Ikon | Catatan |
| --- | --- | --- | --- |
| Uploaded, Processing | `status-open` | Lingkaran | File diterima atau sedang diproses |
| Validation Failed, Failed | `danger-text` | Silang | Bedakan gagal parsing, gagal validasi, gagal posting di teks |
| Validated | `status-open` | Centang | Lulus validasi, belum diajukan |
| Pending Approval | `approval` | Perisai | Menunggu Checker |
| Rejected | `danger-text` | Silang | Alasan wajib tampil |
| Approved, Posting | `approval` | Perisai | Approved dan sedang diposting |
| Posted | `success-text` | Centang | Final; tidak dapat diedit atau dihapus |

## Aturan

- Teks status mengikuti istilah spesifikasi (dalam bahasa Inggris) agar sama dengan backend.
- Failed selalu menyebut jenis kegagalan: "Failed · Parsing", "Failed · Validasi", "Failed · Posting".
- Hanya Posted yang memengaruhi saldo; badge Posted tidak pernah disertai aksi Edit atau Delete.
- Jangan dipakai untuk status tiket.
