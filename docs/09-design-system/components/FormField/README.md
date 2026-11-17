Field form dengan label, input, teks bantu, dan pesan error.

## Aturan

- Label selalu terlihat di atas input; placeholder bukan pengganti label.
- Error tampil di bawah field dengan ikon dan teks (`danger-text`), input mendapat `aria-invalid="true"` dan `aria-describedby` ke pesan.
- Pesan error spesifik: "Format tanggal tidak valid. Gunakan DD/MM/YYYY", bukan "Input salah".
- Field wajib ditandai teks "(wajib)" pada label, tidak hanya tanda bintang.
- Input nonaktif karena role atau status menampilkan alasannya di teks bantu.
- Tinggi 36px; border `border-strong` (3:1 terhadap surface); fokus outline 2px `focus-ring`.

## Token

`border-strong`, `surface`, `surface-subtle`, `danger-text`, `focus-ring`, `radius-sm`.
