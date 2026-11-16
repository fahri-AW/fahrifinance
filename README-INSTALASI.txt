FINANCEFLOW - PERBAIKAN FRONTEND VERCEL

Salin isi ZIP ini ke ROOT project FinanceFlow (folder yang sama dengan server.js,
db.js, package.json, dan nlp-parser.js).

Struktur yang diharapkan:
  index.html
  app.js
  style.css
  vercel.json
  api/
    index.js
  server.js
  db.js
  nlp-parser.js
  package.json

PENTING:
- File HTML memanggil ./style.css dan ./app.js, jadi ketiganya harus berada
  di root yang sama.
- api/index.js adalah fungsi API, jangan letakkan di root.
- Jangan menghapus server.js, db.js, package.json, atau nlp-parser.js.
- vercel.json di ZIP menambahkan rewrite khusus "/" ke "/index.html"
  dan mempertahankan rewrite API yang sudah ada.
- Setelah menyalin, commit dan push lalu tunggu deployment Vercel selesai.
