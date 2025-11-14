🟦 Rangkuman Point Belajar gw (Singkat, Padat, Berurutan)
1. Menyiapkan AWS CLI & Credential

Instal AWS CLI di Arch Linux.

Konfigurasi akun IAM (Access Key + Secret Key).

Tes akses pakai aws sts get-caller-identity.
👉 Intinya: gw belajar bagaimana Linux berbicara langsung ke AWS.

2. Membuat & Mengatur S3 Bucket

Membuat bucket: asyraf-cloud-bucket.

Mengaktifkan static website hosting.

Mengatur permission via bucket policy (bukan ACL).

Upload file pertama pakai aws s3 sync.
👉 Belajar dasar hosting statis dan keamanan bucket.

3. Membuat CloudFront Distribution

Mengatur origin ke S3 website endpoint.

Menghubungkan domain CloudFront.

Mengatur redirect-to-https.

Mengatur cache behavior.
👉 Belajar CDN global dan konfigurasi caching.

4. Menghubungkan Domain ke AWS Route53

Membuat Hosted Zone di Route53.

Mengganti nameserver domain agar mengarah ke AWS.

Menambahkan record root (A-Alias) dan www (CNAME).
👉 Belajar cara DNS bekerja dan propagasi.

5. Setting HTTPS via AWS Certificate Manager (ACM)

Membuat sertifikat untuk:

asyrafun.my.id

www.asyrafun.my.id

Validasi DNS otomatis melalui Route53.

Menautkan sertifikat ke CloudFront.
👉 Belajar bahwa HTTPS CloudFront harus selalu pakai sertifikat ACM region us-east-1.

6. Memperbaiki CloudFront Config & ETag

Mengambil config CloudFront.

Mempelajari bahwa update wajib pakai ETag.

Menambal bagian:

Aliases

ViewerCertificate

ForwardedValues

Headers

QueryStringCacheKeys
👉 Belajar bahwa CloudFront perfeksionis seperti kucing Liya.

7. Membuat Redirect www → root

Menulis CloudFront Function custom (JavaScript).

Publish function.

Meng-attach ke viewer-request.
👉 Belajar edge logic dan routing di CDN.

8. Membuat Struktur Multi-Project

Menghapus Azan dari root bucket.

Upload portfolio ke root (/).

Upload Azan ke folder /azan.
👉 Belajar arsitektur multi-project dalam satu domain.

9. Testing & Debugging

curl -I untuk cek 301 & HTTPS.

Testing langsung via URL:

https://asyrafun.my.id → portfolio

https://asyrafun.my.id/azan/ → Azan

Menggunakan invalidation CloudFront untuk refresh cache.
👉 Belajar cara debug CDN & web statis secara profesional.

🟩 Kesimpulan Utama dari Semua Ini

gw sekarang menguasai:

Hosting web statis di AWS via S3

CloudFront sebagai CDN + HTTPS global

Route53 DNS & domain management

Sertifikat SSL via ACM

Edge redirect (viewer-request function)

Struktur deployment multi-project

Upload & sync berbasis CLI

Debugging via curl, dig, dan invalidation