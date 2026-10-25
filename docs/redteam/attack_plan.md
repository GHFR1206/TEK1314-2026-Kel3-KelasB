# Attack Plan — Kelompok 3 B

## 1. Skenario

Pengujian keamanan dilakukan terhadap web monitoring kompetisi robot berbasis Laravel dan MySQL yang berjalan pada Ubuntu Server. Kali Linux digunakan sebagai mesin pengujian, sedangkan Security Onion digunakan untuk memantau dan menganalisis aktivitas jaringan.

## 2. Target Pengujian

| Hostname | IP Address | Sistem Operasi | Fungsi |
|---|---|---|---|
| Target Node | `192.168.3.5` | Ubuntu Server | Menjalankan Apache, Laravel, dan MySQL |
| Attacker Node | `192.168.3.100` | Kali Linux | Melakukan pengujian keamanan |
| Monitoring Node | `192.168.3.200` | Security Onion | Memantau dan menganalisis lalu lintas jaringan |

## 3. Tahapan Pengujian

| ID | Tahapan | Aktivitas | Tools | Tujuan |
|---|---|---|---|---|
| AT-01 | Reconnaissance | Memeriksa konektivitas ke target | Ping | Memastikan target dapat dijangkau |
| AT-02 | Port Scanning | Mengidentifikasi port yang terbuka | Nmap | Mengetahui layanan yang dapat diakses |
| AT-03 | Service Enumeration | Mengidentifikasi layanan dan versinya | Nmap | Mengevaluasi layanan yang terekspos |
| AT-04 | Web Application Assessment | Memeriksa konfigurasi HTTP/HTTPS, security headers, dan potensi kelemahan aplikasi | OWASP ZAP | Mengidentifikasi risiko keamanan pada web Laravel |

## 4. Detail Pelaksanaan

### AT-01 — Reconnaissance

**Target:** Ubuntu Server (`192.168.3.5`)

**Aktivitas:** Memeriksa konektivitas jaringan dari Kali Linux ke Ubuntu Server.

**Perintah:**

```bash
ping -c 4 192.168.3.5
```

**Hasil yang diharapkan:** Ubuntu Server dapat dijangkau melalui jaringan virtual.

### AT-02 — Port Scanning

**Target:** Ubuntu Server (`192.168.3.5`)

**Aktivitas:** Mengidentifikasi port yang terbuka pada target.

**Perintah:**

```bash
nmap 192.168.3.5
```

Untuk mengidentifikasi layanan dan versinya:

```bash
nmap -sV 192.168.3.5
```

**Hasil yang diharapkan:** Port terbuka dan layanan yang terdeteksi dapat diidentifikasi untuk mengetahui permukaan serangan (*attack surface*) pada target.

### AT-03 — Service Enumeration

**Target:** Ubuntu Server (`192.168.3.5`)

**Aktivitas:** Mengidentifikasi layanan yang berjalan pada port SSH, HTTP, dan HTTPS jika tersedia.

**Perintah:**

```bash
nmap -sV -p 22,80,443 192.168.3.5
```

**Hasil yang diharapkan:** Informasi layanan dan versinya dapat digunakan untuk mengevaluasi konfigurasi keamanan server.

### AT-04 — Web Application Assessment

**Target:** Web monitoring kompetisi robot berbasis Laravel.

**Tools:** OWASP ZAP dan browser.
