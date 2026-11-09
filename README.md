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

## API dummy tracker
Tab Tracker Armada membaca `public/api/v1/fleet.json`, yaitu data fiktif yang formatnya meniru feed AIS untuk kapal (MMSI, kecepatan dalam knot) dan GPS telematika untuk truk (ID perangkat, km/j). Untuk beralih ke data asli:
1. Siapkan endpoint dari penyedia AIS atau GPS (misalnya lewat Cloudflare Worker yang menyimpan API key sebagai secret, sehingga key tidak terlihat di halaman).
2. Samakan formatnya dengan `fleet.json`, lalu ubah konstanta `TRK_API` di `public/index.html` ke alamat endpoint tersebut.
