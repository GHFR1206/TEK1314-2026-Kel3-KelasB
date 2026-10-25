# Attack Plan — Kelompok 3 B

## Attack Scenarios

Pengujian dilakukan pada web monitoring kompetisi robot berbasis Laravel dan MySQL yang berjalan di Ubuntu Server. Seluruh pengujian dilakukan dalam lingkungan virtual terisolasi.

| No. | Kategori | Skenario Serangan | Tools | Target | Tujuan Pengujian |
|---|---|---|---|---|---|
| 1 | Reconnaissance | Port & Service Scanning | Nmap | Ubuntu Server (`192.168.3.5`) | Mengidentifikasi port terbuka, layanan aktif, dan potensi layanan yang tidak diperlukan. |
| 2 | Web/API/Protokol IoT | Web Application Security Testing | OWASP ZAP | Aplikasi Laravel (`192.168.3.5`) | Mengidentifikasi potensi kerentanan aplikasi web, konfigurasi HTTP, dan masalah validasi input. |
| 3 | Exploitation / Akses | Authentication Security Testing | Hydra | Halaman login Laravel (`192.168.3.5`) | Menguji ketahanan autentikasi terhadap percobaan login berulang menggunakan akun pengujian dan batas percobaan yang disepakati. |

## Monitoring dan Evaluasi

| No. | Aktivitas Monitoring | Komponen | Tujuan |
|---|---|---|---|
| 1 | Pemantauan aktivitas pemindaian port | Security Onion | Mengamati apakah aktivitas reconnaissance terdeteksi. |
| 2 | Analisis lalu lintas pengujian aplikasi web | Security Onion | Mengidentifikasi aktivitas HTTP/HTTPS yang mencurigakan. |
| 3 | Analisis aktivitas autentikasi | Security Onion dan log Ubuntu | Mengamati percobaan login berulang dan memeriksa pencatatan aktivitas autentikasi. |

## Ketentuan Pengujian

1. Seluruh pengujian dilakukan pada lingkungan virtual terisolasi dan telah mendapat izin.
2. Target pengujian dibatasi pada Ubuntu Server (`192.168.3.5`).
3. Gunakan akun dan data pengujian, bukan kredensial pengguna sebenarnya.
4. Dokumentasikan waktu pengujian, hasil, dan bukti pendukung.
5. Pengujian dilakukan sebelum dan sesudah hardening untuk mengevaluasi efektivitas pengamanan.
