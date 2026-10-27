# Presentri API Testing Portfolio (Postman)

Repository ini berisi dokumen pengujian untuk **REST API Presentri (Attendance & Leave Request System)** menggunakan **Postman**.

---

## Scope & Feature Tested
1. **Authentication Module (`/api/v1/login`)**
   - Positive Test: Login dengan kredensial valid (HTTP 200 OK + JWT Token)
   - Negative Test: Login dengan password salah (HTTP 401 Unauthorized)

2. **Attendance Module (`/api/v1/attendance/checkin`)**
   - Positive Test: Check-in presensi di dalam radius & QR valid (HTTP 200 OK)
   - Negative Test: Check-in di luar radius lokasi (HTTP 422 Unprocessable Entity)
   - Edge Case: Check-in menggunakan QR code expired (HTTP 400 Bad Request)

3. **Leave Request Module (`/api/v1/leave/store`)**
   - Positive Test: Pengajuan izin/cuti dengan dokumen valid (HTTP 201 Created)

---

## How to Run Test Collection in Postman

1. Download atau clone repository ini.
2. Buka aplikasi **Postman**.
3. Klik tombol **Import** (di pojok kiri atas) $\rightarrow$ pilih file `Presentri_API_Collection.json` dari repo ini.
4. Set up **Environment Variables** (jika ada):
   - `base_url`: `https://staging-api.presentri.com`
   - `token`: `{{jwt_bearer_token}}`
5. Jalankan **Collection Runner** di Postman untuk melihat hasil eksekusi otomatis (*Pass/Fail Assertion*).

---

## 🔗 Live QA Documentation
- **Google Sheets Test Portfolio:** [[Manual Test]](https://docs.google.com/spreadsheets/d/1aVC6Dqrq1EivC3RnAOt8mX12QLYsQT9Xm4Y_INJkDQA/edit?usp=sharing)
- **Tester:** Indah Purnama Reta
