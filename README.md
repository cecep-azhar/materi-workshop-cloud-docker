# 🚀 Workshop: Manajemen Server Cloud & Infrastruktur Virtualisasi (Docker)

Repositori ini berisi materi, panduan praktikum, cheatsheet perintah, dan slide presentasi resmi untuk **Workshop Manajemen Server Cloud & Infrastruktur Virtualisasi (Docker)**.

Dirancang khusus untuk siswa SMK TKJ / Mahasiswa / Praktisi IT pemula agar memahami fundamental server modern, transisi dari arsitektur fisik/VM ke Container, hingga deployment multi-container siap produksi.

---

## 📅 Struktur & Silabus Workshop

### 📌 Hari 1 — Fondasi Cloud Server & Virtualisasi Modern
1. **Dasar Server & Linux CLI:** Refresher terminal, SSH key security (`chmod 600`), port & service management.
2. **Arsitektur Cloud & Shared Responsibility:** Perbedaan On-Premise, IaaS, PaaS, dan SaaS serta tanggung jawab keamanan data.
3. **Evolusi Virtualisasi:** Dari Bare-metal Server, Hypervisor Tipe 1 & 2 (VM), hingga Container Engine.
4. **Pengenalan Docker:** Mengapa Container? Isolasi proses, efisiensi resource, dan pemecahan masalah *"it works on my machine"*.

### 📌 Hari 2 — Praktikum Hands-on & Ujian Sertifikasi
1. **Lab 1 (Container Lifecycle):** Menjalankan web server Nginx & memahami port forwarding (`-p host:container`).
2. **Lab 2 (Data Persistence):** Menghubungkan Docker Volume & Bind Mount agar data database tidak hilang saat container restart.
3. **Lab 3 (Custom Image & Dockerfile):** Menulis `Dockerfile` berlapis (`FROM`, `COPY`, `EXPOSE`, `CMD`) dan build image kustom.
4. **Lab 4 (Multi-Container Orchestration):** Menghubungkan Web App + PostgreSQL Database menggunakan **Docker Compose**.
5. **Ujian Teori & Praktikum:** Evaluasi pemahaman melalui studi kasus deployment live.

---

## 🛠️ Persiapan Alat (Prerequisites Peserta)

Pastikan laptop/PC peserta telah terpasang perangkat lunak berikut sebelum praktikum:

* **SSH Client & Terminal:** [CATerm](https://caterm.fathforce.com), Windows Terminal / PowerShell, atau Termius.
* **Docker Desktop / Docker Engine:** Docker CE v24+ & Docker Compose v2+.
* **Code Editor:** VS Code / Zed Editor / Cursor.
* **Git:** Git CLI untuk cloning modul praktikum.

---

## ⚡ Cheatsheet Perintah Penting (Quick Reference)

### 🔑 1. Remote SSH Akses
```bash
# Akses remote server via SSH
ssh siswa@ssh.xpc.my.id

# Set permission private key (Linux/macOS)
chmod 600 ~/.ssh/id_ed25519
```

### 🐳 2. Perintah Dasar Docker
```bash
# Cek versi docker
docker version

# Download image dari registry
docker pull nginx:alpine

# Jalankan container web server
docker run -d -p 8080:80 --name web-latihan nginx:alpine

# Melihat container yang sedang berjalan
docker ps

# Melihat semua container (termasuk yang berhenti)
docker ps -a

# Menghentikan dan menghapus container
docker stop web-latihan
docker rm web-latihan

# Melihat log container secara live
docker logs -f web-latihan
```

### 📦 3. Docker Volume & Compose
```bash
# Menjalankan container dengan volume persistent
docker run -d -p 5432:5432 --name db-latihan -v pgdata:/var/lib/postgresql/data -e POSTGRES_PASSWORD=secret postgres:16-alpine

# Menjalankan multi-container via Docker Compose
docker compose up -d

# Mematikan service Docker Compose beserta volumenya
docker compose down -v
```

---

## 📖 Berkas & Dokumen Presentasi

* 📄 **[Hari-1-Materi.pdf](./Hari-1-Materi.pdf)** — Slide presentasi lengkap pengenalan Cloud Server, Arsitektur Virtualisasi & Konsep Docker.

---

## 👨🏫 Instruktur / Fasilitator
**Cecep Azhar**  
*Software Engineer & AI Systems Architect*  
* Website: [cecepazhar.com](https://cecepazhar.com)  
* GitHub: [@cecep-azhar](https://github.com/cecep-azhar)  
* LinkedIn: [linkedin.com/in/cecepazhar](https://linkedin.com/in/cecepazhar)

---
*Materi ini disusun untuk kegiatan pelatihan & workshop vokasi teknologi informasi.*
