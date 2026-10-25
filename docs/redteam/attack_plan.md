# Attack Plan — Kelompok 3 B

## Skenario Pengujian Keamanan

Pengujian dilakukan pada web monitoring kompetisi robot berbasis Laravel dan MySQL yang berjalan di Ubuntu Server. Seluruh pengujian dilakukan dalam lingkungan virtual terisolasi.

| No. | Skenario Serangan | Tujuan | Attacker | Target | Tools | Aktivitas Pengujian | Hasil yang Diharapkan |
|---|---|---|---|---|---|---|---|
| 1 | Network Reconnaissance & Port Scanning | Mengidentifikasi port dan layanan yang aktif pada server target. | Kali Linux (`192.168.3.100`) | Ubuntu Server (`192.168.3.5`) | Nmap | Memindai port dan mengidentifikasi layanan yang berjalan pada server. | Mengetahui port terbuka dan mengidentifikasi layanan yang tidak diperlukan. |
| 2 | Web Application Security Testing | Mengidentifikasi potensi kerentanan pada aplikasi web Laravel. | Kali Linux (`192.168.3.100`) | Ubuntu Server (`192.168.3.5`) | OWASP ZAP | Menguji validasi input, konfigurasi keamanan HTTP, dan potensi kerentanan aplikasi web. | Memperoleh temuan keamanan dan rekomendasi perbaikan aplikasi. |
| 3 | Authentication Security Testing | Mengevaluasi keamanan mekanisme autentikasi aplikasi. | Kali Linux (`192.168.3.100`) | Ubuntu Server (`192.168.3.5`) | Browser, OWASP ZAP | Menguji pembatasan percobaan login dan respons aplikasi terhadap percobaan autentikasi berulang menggunakan akun pengujian. | Memastikan autentikasi dan rate limiting berfungsi sesuai konfigurasi. |

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
