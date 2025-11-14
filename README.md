# ☁️ Jurnal Belajar & Pengembangan Sistem Hosting di AWS

Halo! Selamat datang di *repository* ini. Proyek ini adalah jurnal pribadi saya untuk mencatat perjalanan belajar tentang **Amazon Web Services (AWS)** dari dasar hingga membangun dan mengoperasikan layanan **Domain & Web Hosting** yang fungsional.

Tujuan utama proyek ini adalah mendokumentasikan proses, arsitektur, dan tantangan yang dihadapi selama proses pengembangan *cloud engineering*.

---

## 🎯 Tujuan Utama Proyek

*   **Menguasai Layanan AWS Esensial:** Mempelajari dan menerapkan layanan-layanan dasar AWS seperti EC2, VPC, S3, dan Route 53.
*   **Membangun Arsitektur Skalabel:** Merancang sistem *hosting* yang andal, aman, dan dapat menangani lonjakan lalu lintas (menggunakan Auto Scaling, Load Balancer, dll.).
*   **Menerapkan Infrastructure as Code (IaC):** Belajar menggunakan tools seperti Terraform atau CloudFormation untuk mengelola infrastruktur.

## 📁 Struktur Repository

Repository ini dibagi menjadi dua bagian utama untuk memisahkan catatan belajar dari konfigurasi sistem yang sensitif.

| Folder | Status | Deskripsi Konten |
| :--- | :--- | :--- |
| **`public/`** | ✅ **Publik** | Berisi semua catatan belajar, konsep teori, *code snippets* yang aman, dan dokumentasi arsitektur umum. |
| **`private/`** | 🔒 **Private** | **Folder ini diabaikan oleh `.gitignore`**. Berisi kredensial, kunci API, file `.env`, *script* deployment dengan data sensitif, dan konfigurasi *private*. |

---

## 📚 Catatan Pembelajaran (Folder `/public/`)

Berikut adalah daftar topik dan modul yang sedang/telah dipelajari.

### Modul 1: Dasar-Dasar AWS (VPC & EC2)
*   **[Folder Belajar Pertama] - Pengantar VPC & Subnetting:** Pembuatan jaringan virtual, konfigurasi *routing*, dan *security groups*.
    *   [File 1-10] Cara *launching* dan mengkonfigurasi instance EC2 dasar.
*   *Lanjutan:* Mengamankan SSH, Elastic IP vs. IP Publik Dinamis.

### Modul 2: Penyimpanan dan Database (S3 & RDS)
*   Menggunakan S3 untuk penyimpanan statis (website hosting).
*   Setup database terkelola (RDS) dan konfigurasi *parameter group*.

### Modul 3: Jaringan dan Keamanan (Route 53 & Load Balancing)
*   Konfigurasi DNS dengan Route 53 untuk *custom domain*.
*   Menerapkan Application Load Balancer (ALB) untuk distribusi trafik.

---

## 🏗️ Status Pengembangan Sistem Hosting

*   [ ] Tahap 1: Setup Infrastruktur Dasar (VPC, Subnet, Internet Gateway)
*   [X] Tahap 2: Deployment EC2 Web Server (Nginx/Apache)
*   [ ] Tahap 3: Implementasi Database (RDS)
*   [ ] Tahap 4: Konfigurasi Otomasi Deployment (CI/CD)
*   [ ] Tahap 5: Testing Skalabilitas dan Keamanan

---

## 🤝 Kontribusi

*Repository* ini adalah jurnal pribadi. Namun, saran, *feedback*, atau koreksi konsep sangat diterima melalui *Issues* atau *Pull Requests*.

---