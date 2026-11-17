Contoh halaman Statement Approval (SCR-010) untuk Checker, ditampilkan di sini dari sudut pandang Maker yang tidak boleh menyetujui.

## Komposisi

- ApprovalBanner di atas: status dan siapa yang bertindak berikutnya.
- Ringkasan: rekening (masking), periode, jumlah transaksi, opening, total credit, total debit, closing, dan rumus saldo.
- Tabel transaksi (hanya baca) dengan footer total.
- Kolom kanan: ApprovalTimeline dan aksi.

## Aturan

- Approve dan Reject hanya aktif bagi Checker yang bukan Maker. Bagi Maker, Approve nonaktif dengan alasan terlihat, dan Reject tidak ditampilkan.
- Approve membuka ConfirmDialog "Post statement?" yang menyebut dampaknya; Reject meminta alasan wajib.
- Tidak ada Edit atau Delete. Statement Posted hanya dapat dikoreksi lewat Reverse atau Adjust.
- Setelah aksi, status baru tampil permanen di banner dan timeline, tidak hanya sebagai toast.

Halaman ini memakai data ilustrasi.
