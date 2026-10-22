# MNP Dashboard: Konsolidasi Kargo KTI

Prototipe dashboard Solusi 1 (Monitoring End-to-End) untuk case competition Makassar New Port. Halaman statis satu berkas (`index.html`), tanpa proses build.

## Isi
- Ringkasan KPI, tren TEU mingguan, dan peringatan aktif
- Peta skematik titik konsolidasi KTI menuju MNP
- Pipeline, scorecard, heatmap, dan simulasi partner mundur
- Tracker truk dan feeder terhadap cut-off direct call
- Proyeksi tiga skenario dan simulator ambang direct call

## Deploy ke Cloudflare Pages
1. Cloudflare dashboard, Workers & Pages, Create, Pages, Connect to Git.
2. Pilih repo ini, branch `main`.
3. Framework preset `None`, build command dikosongkan, output directory `/`.
4. Save and Deploy. Setiap push ke `main` akan ter-deploy otomatis.

Seluruh angka, nama partner, dan status kemitraan bersifat ilustratif.
