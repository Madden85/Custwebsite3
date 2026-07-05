CUSTOMER WEBSITE 3 - DIRECT ADMIN / DAPATKAN AKAUN
Version: 2026-07-05 V1

APA YANG DIBUAT
1. Design ikut Customer Website 2.
2. Button pakej dan Hot Selling ditukar kepada: DAPATKAN AKAUN.
3. Bila customer tekan button, website terus buka Telegram admin dengan ayat order siap.
4. Tiada payment modal.
5. Tiada redirect ke ToyyibPay.
6. Stock, promo price dan Hot Selling masih sync dari endpoint sedia ada.

FLOW CUSTOMER
Website 3 -> pilih produk -> lihat pakej -> tekan DAPATKAN AKAUN -> stock check -> create lead/log jika backend sudah update -> fallback local jika backend belum update -> buka Telegram admin dengan mesej order siap.

FILE UNTUK DEPLOY WEBSITE
Upload semua file dalam folder ini ke hosting/subdomain Website 3.
Main file: index.html, app.js, app2.js, image files.
Note: success.html tidak diperlukan untuk Website 3 sebab tiada payment gateway redirect.

SETTING ADMIN TELEGRAM
Edit app2.js:
window.NUMO_ADMIN_CONFIG.ADMIN_TELEGRAM_USERNAME

NOTA BACKEND
Website ini boleh jalan tanpa update backend kerana ada fallback local Lead ID.
Tapi kalau nak semua lead masuk Google Sheet LEADS, deploy Apps Script patch V10 yang disediakan dalam package utama.
