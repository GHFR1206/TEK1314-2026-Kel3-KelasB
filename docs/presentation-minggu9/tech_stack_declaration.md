# Deklarasi Teknologi dan Replikasi

Tabel berikut menjelaskan teknologi yang digunakan pada proyek IoT asli dan implementasinya pada Target Node untuk kebutuhan pengujian keamanan.

| Komponen | Teknologi pada Proyek IoT Asli | Direplikasi sebagai (Target Node) |
|---|---|---|
| Sistem Operasi backend | Ubuntu Server sebagai server aplikasi | Ubuntu Server 26.04 LTS (`192.168.3.5`) |
| Database/penyimpanan data | MySQL untuk menyimpan data kompetisi robot, tim, skor, dan hasil pertandingan | MySQL 8.4 dengan database Laravel pada Ubuntu Server |
| Protokol komunikasi sensor | HTTP REST untuk pertukaran data antara perangkat dan backend | HTTP/HTTPS melalui Nginx untuk akses aplikasi web dan komunikasi dengan backend Laravel |
| Dashboard/monitoring | Dashboard web untuk memantau kompetisi robot dan menampilkan data pertandingan | Aplikasi Laravel yang diakses melalui browser dengan Nginx sebagai web server |
| Web server/reverse proxy | Nginx untuk melayani aplikasi web | Nginx 1.28.3 dengan HTTP-to-HTTPS redirect dan TLS |
| Autentikasi dan keamanan | Autentikasi pengguna serta pembatasan hak akses | SSH key authentication, UFW firewall, Fail2ban, dan pembatasan hak akses user database |
