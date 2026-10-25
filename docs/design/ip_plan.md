# IP Plan — Kelompok 3 B

**Skenario:** Simulasi serangan dan monitoring pada segmen jaringan terisolasi kelompok, menggunakan Kali Linux sebagai *attacker* dan Ubuntu Server sebagai *target* yang menjalankan web monitoring kompetisi robot berbasis Laravel dan MySQL, dipantau oleh Security Onion.

**Subnet kelompok:** `192.168.3.0/24`

| Hostname | IP Address | OS | Note/Port Target |
|---|---|---|---|
| Target | `192.168.3.5` | Ubuntu Server | Port 22 (SSH), 80 (HTTP), 443 (HTTPS). MySQL (3306, internal) |
| Attacker | `192.168.3.100` | Kali Linux | Attacker Node |
| Monitoring | `192.168.3.200` | Security Onion | IDS & Traffic Monitoring |

## Keterangan

- **Target — Ubuntu Server (`192.168.3.5`):** Menjalankan Apache, Laravel, dan MySQL sebagai platform web monitoring kompetisi robot.
- **Attacker — Kali Linux (`192.168.3.100`):** Digunakan untuk melakukan pengujian keamanan terhadap layanan web dan jaringan secara terotorisasi.
- **Monitoring — Security Onion (`192.168.3.200`):** Digunakan untuk memantau lalu lintas jaringan dan mendeteksi aktivitas mencurigakan selama pengujian keamanan.
