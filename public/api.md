Alur lengkap Login API-only (Final Summary)

Ini alur sistemmu sekarang:

1. Login lokal (email + password)

Endpoint: POST /api/login

Output: Bearer Token Sanctum

Tanpa session, tanpa cookie

State: stateless full API-only

2. Cek user login

Endpoint: GET /api/me

Header: Authorization: Bearer <token>

3. Google Login API-only

Flow modern ala aplikasi mobile / SPA:

Client login Google → dapat ID Token

Client kirim ID Token ke /api/auth/google

Backend verifikasi JWT Google via Socialite

Jika email belum ada → buat user

Buat token Sanctum

Return JSON login sukses

4. Semua token di-backend stateless

Kamu gak pakai cookie

Kamu gak pakai redirect

Kamu gak pakai session web

Full API-only, bersih, efisien, aman