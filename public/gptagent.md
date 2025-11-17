🔥 FITUR 1 — Codex Thread (Contextual AI per-file / per-rule)

Ini fitur paling OP, jauh melampaui Copilot.

Fungsi:

Bikin 1 thread AI khusus untuk 1 bagian project, jadi AI fokus ke file itu saja, gak ngawang-ngawang.

Cara pakainya:

Buka file apa pun, misalnya:

app/Http/Controllers/Auth/LoginController.php


Tekan:

Ctrl + Shift + P
→ ketik: "New Codex Panel"


Muncul panel Codex Thread di kanan.

Now:
Codex akan hanya fokus pada file itu & struktur project kamu.

Contoh penggunaan:

Ketik di panel Codex:

“Refactor method login() agar lebih aman, gunakan try-catch, validasi lebih ketat, dan kembalikan menggunakan ApiResponse helper.”

Codex nggak bakal bingung.
Dia bakal:

baca file

baca helper ApiResponse

baca struktur folder

refactor method langsung industri-level

Ini lebih presisi daripada Copilot yang tebak-tebak buah mangga.

🔥 FITUR 2 — Implement TODO (auto-generate method/code dari komentar)
Fungsi:

Kamu tulis komentar TODO
→ Codex generate fungsinya lengkap.

Cara pakainya (super gampang):

Buka file lalu tulis:

// TODO: buat function untuk hash refresh token & simpan ke DB users


Lalu:

klik tulisan Implement with Codex yang muncul di atas komentar
(itu CodeLens otomatis)

Codex akan bikin:

private function generateRefreshToken($user)
{
    $token = Str::random(64);

    $user->refresh_token = hash('sha256', $token);
    $user->save();

    return $token;
}


Dan itu dihasilkan dari konteks project kamu, bukan template generik.

🔥 FITUR 3 — Add To Codex Thread (analisis multi-file)

Kalau kamu punya 2–3 file yang saling terkait:

Misal:

LoginController.php

User.php

ApiResponse.php

Lalu kamu buka Codex Panel → di file lain kamu klik:

Cmd Palette → "Add to Codex Thread"


Codex sekarang membaca file tambahan itu sebagai konteks.
Cocok untuk debugging error lintas file.

Contoh:

Tanya:

“Kenapa token refresh saya tidak terputar?
Lihat file User.php dan LoginController.”

Codex akan analisis:

logic salah

validation miss

return structure tidak sesuai

ApiResponse salah format

Ini fitur yang Copilot sama sekali tidak punya.

🔥 FITUR 4 — New Codex Agent (buat spesifik keperluan)

Ini mirip kamu bikin bot khusus.

Tekan:

Ctrl + Shift + P → New Codex Agent


Pilih role (debug, refactor, docs, dll.)

AI menjadi mode yang kamu pilih.

Contoh:

Kamu pilih Refactor Agent
Ketik:

“Buatkan versi yang lebih efisien dari StaticHostingService.php, kurangi duplicate code.”

Agent langsung:

generate ulang file

highlight apa yang diubah

kasih alasan

🔥 FITUR 5 — Sidebar Mode (Coding Copilot mode)

Kamu bisa buka sidebar:

Ctrl + Shift + P → Open Codex Sidebar


Nah di situ kamu tinggal:

drag file → AI baca

select code block → klik “Ask Codex”

minta penjelasan baris demi baris

atau minta generate dokumentasi

Contoh:

Select 20 baris kode Laravel
Klik kanan → “Ask Codex”

Tanya:

“Ini logic apa dan bagaimana cara mengoptimalkannya?”

Dia bakal jelasin kayak senior engineer, bukan kayak chatbot malas.

🔥 FITUR 6 — Explain File / Fix Error otomatis

Codex bisa baca error dari terminal.
Kamu copy error log → paste ke Codex Panel.

Contoh error:
Call to a member function createToken() on null


Ketik:

“Fix error ini, tunjukkan baris mana yang salah dan perbaiki.”

Codex:

baca controller

cari objek null

perbaiki logic

kasih kode final

Gemini sering gagal di cross-file PHP.
Copilot cuma ngasih saran separuh.

Tapi Codex jalan karena dia baca project kamu via thread.

🔥 FITUR 7 — Code Refactor in-place

Select code → tekan:

Ctrl + Shift + P → "Implement with Codex"


Dia akan:

reorganize

simplify

extract method

rename variabel

kasih alasan

🎁 CONTOH PALING SIMPLE (biar kamu langsung paham)

Kamu buka file LoginController.
Dalam panel Codex ketik:

“Refactor function login() supaya:

validasi lebih ketat

struktur jelas

ApiResponse konsisten

error handling rapi

hindari duplicate code

aman dari brute force”

Codex bakal langsung kirim:

versi login() yang lebih rapih

alasan perubahan

block kode final

Kamu tinggal copy → paste.

Selesai.