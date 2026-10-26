# Hardening Checklist

## A. Access & Authentication

| No. | Kontrol Hardening | Status | Evidence |
|---|---|---|---|
| A1 | Menonaktifkan SSH Password Authentication dan menggunakan Key Authentication | Sudah | [SSH Configuration](evidence/After%20-%20SSH%20Configuration%20and%20Service%20Verification.jpeg) |
| A2 | Menonaktifkan `PermitRootLogin` pada SSH | Sudah | [SSH Root and Password Restriction](evidence/After%20-%20SSH%20Root%20and%20Password%20Authentication%20Restriction.jpeg) |
| A3 | Mengaktifkan Fail2ban untuk melindungi SSH dari percobaan login berulang | Sudah | [Fail2ban Service](evidence/After%20-%20Fail2ban%20Service%20Activation%20and%20Verification.jpeg) |
| A4 | Memverifikasi pemantauan percobaan login SSH oleh Fail2ban | Sudah | [SSH Brute-Force Monitoring](evidence/After%20-%20SSH%20Brute-Force%20Monitoring%20and%20Ban%20Status.jpeg) |
| A5 | Memverifikasi autentikasi SSH menggunakan public key | Sudah | [SSH Key Authentication](evidence/After%20-%20SSH%20Key-Based%20Authentication%20Verification.jpeg) |

## B. Service & Attack Surface

| No. | Kontrol Hardening | Status | Evidence |
|---|---|---|---|
| B1 | Mengaktifkan UFW dengan kebijakan default deny incoming dan mengizinkan port 2222, 80, serta 443 | Sudah | [UFW Firewall](evidence/After%20-%20UFW%20Firewall%20Enabled%20with%20Restricted%20Incoming%20Access.jpeg) |
| B2 | Membatasi akses jaringan ke port MySQL 3306 dan 33060 | Sudah | [MySQL Ports Filtered](evidence/After%20-%20MySQL%20Ports%20Filtered%20from%20Network%20Access.jpeg) |
| B3 | Membatasi MYSQL agar hanya listen pada localhost | Sudah | [MariaDB Localhost Binding](evidence/After%20-%20MariaDB%20Bound%20to%20Localhost%20Only.jpeg) |
| B4 | Membandingkan port dan layanan yang terbuka sebelum dan sesudah hardening | Sudah | [Port Exposure Comparison](evidence/After%20-%20Port%20Exposure%20Comparison%20Before%20After%20Hardening.jpeg) |

## C. Data & Application

| No. | Kontrol Hardening | Status | Evidence |
|---|---|---|---|
| C1 | Mengonfigurasi HTTP redirect ke HTTPS menggunakan status 301 | Sudah | [HTTP to HTTPS Redirect](evidence/After%20-%20HTTP%20to%20HTTPS%20Redirect.jpeg) |
| C2 | Membuat user database khusus aplikasi `laravel_app` | Sudah | [Database User Creation](evidence/Before%20-%20Dedicated%20Application%20Database%20User%20Creation.jpeg) |
| C3 | Membatasi hak akses user database aplikasi terhadap database sistem | Sudah | [Database Least-Privilege Verification](evidence/After%20-%20Database%20Least-Privilege%20Verification.jpeg) |
| C4 | Membatasi permission file `.env` Laravel menggunakan `chmod 600` | Sudah | [Laravel .env File Permission Restricted to 600](evidence/After%20-%20Laravel%20.env%20File%20Permission%20Restricted%20to%20600.jpeg) |

- Screenshot yang menunjukkan percobaan login gagal tidak otomatis membuktikan bahwa IP penyerang berhasil diblokir oleh Fail2ban.
- Permission file `.env`, Nginx security headers, dan `server_tokens off` perlu diverifikasi secara terpisah jika ingin dimasukkan sebagai kontrol yang telah diterapkan.
