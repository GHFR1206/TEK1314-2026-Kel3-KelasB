# Selamat datang di TEK1314-2026-Kel3-KelasB

Repositori resmi Kelompok 3 Kelas B.

## Anggota Kelompok

| No. | Nama | NIM | Peran |
|---|---|---|---|
| 1 | Ghifari Hamdanigiar | J0404241050 | Blue Team |
| 2 | Asti Indriyanti | J0404241060 | Lead |
| 3 | Muhammad Fauzan Azhim | J0404241087 | Red Team |

## Skenario Proyek

Kelompok kami menjalankan simulasi keamanan siber pada sistem web monitoring kompetisi robot berbasis Laravel dan MySQL dalam jaringan virtual yang terisolasi. Simulasi ini bertujuan untuk menguji keamanan layanan, memantau aktivitas jaringan, serta menerapkan langkah-langkah pengamanan pada server dan aplikasi.

## Arsitektur Jaringan

**Subnet Kelompok:** `192.168.3.0/24`

| Hostname | IP Address | Sistem Operasi | Fungsi |
|---|---|---|---|
| Target Node | `192.168.3.5` | Ubuntu Server | Menjalankan Apache, Laravel, dan MySQL sebagai platform web monitoring kompetisi robot. |
| Attacker Node | `192.168.3.100` | Kali Linux | Melakukan pengujian keamanan terhadap layanan dan aplikasi web. |
| Monitoring Node | `192.168.3.200` | Security Onion | Memantau lalu lintas jaringan dan menganalisis aktivitas yang terdeteksi selama pengujian. |

Seluruh node direncanakan berada dalam subnet `192.168.3.0/24`. Pengujian dilakukan pada lingkungan virtual terisolasi untuk mendukung analisis keamanan dan evaluasi efektivitas hardening.

## Dokumentasi

Dokumen desain topologi dan skema IP lengkap tersedia di folder [`docs/design/`](docs/design/).
