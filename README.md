[README.md](https://github.com/user-attachments/files/22553750/README.md)
# Laporan Praktikum Git & GitHub  

## Tujuan  
Praktikum ini bertujuan untuk memahami penggunaan Git dan GitHub, mulai dari instalasi, konfigurasi awal, alur kerja dasar secara lokal, hingga kolaborasi tim menggunakan *feature branch workflow*.  

## Bagian 1: Instalasi & Konfigurasi Awal Git  
1. **Instalasi Git**  
   - **Windows**: Unduh installer dari [git-scm.com](https://git-scm.com/download/win), jalankan, dan cek dengan `git --version`.  
   - **macOS**: Instal via Homebrew dengan `brew install git`.  
   - **Linux (Ubuntu/Debian)**: Jalankan `sudo apt update && sudo apt install git`.  

2. **Konfigurasi Awal**  
   ```bash
   git config --global user.name "Nama Kamu"
   git config --global user.email "email@kamu.com"
   ```

## Bagian 2: Alur Kerja Dasar Git (Lokal)  
1. Buat folder proyek & inisialisasi Git:  
   ```bash
   mkdir proyek-web
   cd proyek-web
   git init
   ```  
2. Tambah file dan cek status:  
   ```bash
   echo "<h1>Selamat Datang</h1>" > index.html
   mkdir css
   echo "body { font-family: sans-serif; }" > css/style.css
   git status
   git add .
   git commit -m "feat: Inisialisasi proyek dengan file index dan css"
   ```  
3. Membuat dan berpindah branch baru:  
   ```bash
   git checkout -b fitur-kontak
   echo "<h1>Halaman Kontak</h1>" > kontak.html
   git add .
   git commit -m "feat: Menambahkan halaman kontak"
   ```  
4. Gabungkan branch ke main:  
   ```bash
   git checkout main
   git merge fitur-kontak
   ```

## Bagian 3: Integrasi dengan GitHub  
1. Buat repository di GitHub.  
2. Hubungkan repository lokal dengan GitHub:  
   ```bash
   git remote add origin https://github.com/NamaUserKamu/proyek-web-pertama.git
   git branch -M main
   git push -u origin main
   ```

## Bagian 4: Workflow Kerja Kelompok (Feature Branch Workflow)  
1. Clone repository:  
   ```bash
   git clone <URL_REPOSITORY>
   ```  
2. Tarik pembaruan dari branch utama:  
   ```bash
   git checkout main
   git pull origin main
   ```  
3. Buat branch baru untuk fitur:  
   ```bash
   git checkout -b nama-fitur-baru
   ```  
4. Tambah dan commit perubahan:  
   ```bash
   git add .
   git commit -m "pesan commit yang jelas"
   ```  
5. Push branch ke GitHub:  
   ```bash
   git push origin nama-fitur-baru
   ```  
6. Buat *Pull Request* di GitHub.  
7. Reviewer memeriksa perubahan → Merge ke main.  
8. Sinkronisasi ulang setelah merge:  
   ```bash
   git checkout main
   git pull origin main
   ```

---
<img width="1920" height="1080" alt="Screenshot 2025-09-26 111803" src="https://github.com/user-attachments/assets/a4d39947-6c8c-47eb-8865-b95f167b4e04" />

## Kesimpulan  
Melalui praktikum ini, mahasiswa mempelajari alur lengkap penggunaan Git dan GitHub mulai dari instalasi, konfigurasi, manajemen version control secara lokal, hingga kolaborasi tim dengan workflow yang baik.  
