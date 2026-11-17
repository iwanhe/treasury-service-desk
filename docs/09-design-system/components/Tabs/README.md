Tab untuk berpindah antar tampilan dalam satu halaman, misalnya detail tiket (Percakapan, Riwayat, Terkait) atau detail rekening (Saldo, Transaksi, Statement).

## Aturan

- Tab terpilih ditandai garis bawah 2px `primary`, teks `primary-text`, dan `aria-selected="true"`. Tidak hanya warna: bobot dan garis bawah ikut berubah.
- Pola ARIA: `role="tablist"`, `role="tab"`, `role="tabpanel"`. Panah kiri dan kanan berpindah tab, Home dan End ke tab pertama dan terakhir.
- Hitungan opsional di kanan label, selalu angka.
- Maksimal enam tab; selebihnya masuk menu "Lainnya".
- Tab bukan navigasi antar halaman: untuk itu pakai SidebarNav.

## Token

`primary`, `primary-text`, `text-muted`, `border`, `focus-ring`.
