# MNP Dashboard: Konsolidasi Kargo KTI

Prototipe dashboard Solusi 1 (Monitoring End-to-End) untuk case competition Makassar New Port. Halaman statis satu berkas (`public/index.html`), tanpa proses build. Dideploy sebagai Cloudflare Worker dengan static assets (lihat `wrangler.jsonc`).

## Isi
- Ringkasan KPI, tren TEU mingguan, dan peringatan aktif
- Peta skematik titik konsolidasi KTI menuju MNP
- Pipeline, scorecard, heatmap, dan simulasi partner mundur
- Tracker truk dan feeder terhadap cut-off direct call
- Proyeksi tiga skenario dan simulator ambang direct call

## Deploy ke Cloudflare
1. Cloudflare dashboard, Workers & Pages, Create, Import a repository.
2. Pilih repo ini. Project name `mnp-dashboard`.
3. Build command dikosongkan. Deploy command `npx wrangler deploy`.
4. Deploy. Setiap push ke `main` akan ter-deploy otomatis.

Seluruh angka, nama partner, dan status kemitraan bersifat ilustratif.
