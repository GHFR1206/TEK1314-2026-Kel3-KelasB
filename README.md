# Selamat datang di TEK1314-2026-Kel3-KelasB

Ini adalah repositori Kelompok 3 Kelas B

Anggota:
1. Ghifari Hamdanigiar (J0404241050) -> Red Team
2. Asti Indriyanti (J0404241060) -> Lead
3. Muhammad Fauzan Azhim (J0404241087) -> Blue Team

## Skenario Proyek

Kelompok kami menjalankan simulasi keamanan siber dengan skenario **web/database attack-defense** pada jaringan terisolasi:

- **Attacker Node**: Kali Linux (192.168.3.100) — menjalankan reconnaissance dan eksploitasi terhadap target.
- **Target Node**: Metasploitable 2 (192.168.3.6) — server korban dengan celah keamanan pada service FTP (21), SSH (22), HTTP (80), dan MySQL (3306).
- **Monitoring Node**: Security Onion (192.168.3.200) — memantau seluruh lalu lintas antara Attacker dan Target Node untuk keperluan deteksi intrusi (IDS) dan analisis trafik.

Seluruh node berada dalam subnet `192.168.3.0/24`. Dokumen desain topologi dan skema IP lengkap tersedia di folder [`docs/design/`](docs/design/).
