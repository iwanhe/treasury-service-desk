Contoh halaman dashboard cash position, menyusun FilterBar, CashPositionTotals, KpiTile, dan AccountBalanceTable (DailyMovementChart ditempatkan di antara KPI dan tabel pada implementasi).

## Urutan dari atas

1. **FilterBar**: satu baris, mencakup seluruh halaman.
2. **CashPositionTotals**: total per currency, satu baris penuh.
3. **KpiTile**: Pending approval, Ticket backlog, SLA at risk.
4. **DailyMovementChart** (satu currency per grafik) dan Latest Statement.
5. **AccountBalanceTable**: saldo per rekening dengan status Reconciled atau Stale.

## Aturan

- Hanya satu angka utama per currency yang menonjol; tidak ada angka "hero" yang mencampur currency.
- Semua widget memakai irisan data yang sama dari filter.
- Setiap nominal memuat tanggal saldo; rekening stale ditandai di tabel dan di total currency terkait.
- Halaman dapat diekspor ke Excel dari header; ekspor membawa tanggal saldo dan jenis saldo.
- Data di preview adalah ilustrasi.
