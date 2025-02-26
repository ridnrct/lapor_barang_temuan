# Website Pelaporan Barang Temuan

## 📚 Deskripsi
Website ini memungkinkan pengguna melaporkan barang temuan. Fitur utama meliputi:
- Registrasi dan verifikasi email pengguna.
- Login untuk pengguna dan admin.
- Upload barang temuan dengan gambar.
- Admin dapat memverifikasi, menerima, atau menolak laporan.
- Penghapusan otomatis barang setelah 3 hari.
- Notifikasi email untuk setiap tindakan penting.

---

## ⚡️ Teknologi yang Digunakan
- **Python** (Flask Framework)
- **MySQL** untuk database
- **HTML, CSS, dan Bootstrap** untuk frontend
- **Flask-Mail** untuk pengiriman email
- **APScheduler** untuk penjadwalan otomatis
- **Werkzeug** untuk pengelolaan file

---

## 🚀 Instalasi dan Konfigurasi

### 1️⃣ **Clone Repository**
```bash
git clone https://github.com/username/website-pelaporan-barang-temuan.git
cd website-pelaporan-barang-temuan
```

### 2️⃣ **Buat dan Aktifkan Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\\Scripts\\activate   # Windows
```

### 3️⃣ **Instalasi Library**
```bash
pip install -r requirements.txt
```

### 4️⃣ **Konfigurasi Database**
- Pastikan MySQL berjalan.
- Buat database `web_barang_hilang` dan import skema SQL.
- Perbarui konfigurasi pada `app.config`:
  ```python
  app.config['MYSQL_HOST'] = 'localhost'
  app.config['MYSQL_USER'] = 'root'
  app.config['MYSQL_PASSWORD'] = 'password_anda'
  app.config['MYSQL_DB'] = 'web_barang_hilang'
  ```

### 5️⃣ **Konfigurasi Email (Flask-Mail)**
- Konfigurasikan `MAIL_USERNAME` dan `MAIL_PASSWORD` di `app.config`:
  ```python
  app.config['MAIL_USERNAME'] = 'email_anda@gmail.com'
  app.config['MAIL_PASSWORD'] = 'password_aplikasi_anda'
  ```

---

## 🔧 Cara Menjalankan
```bash
python app.py
```
Akses website di: [http://127.0.0.1:5000](http://127.0.0.1:5000)

---

## 🎞️ Konfigurasi Path Upload
- Path upload default: `uploads/`
- Pastikan folder `uploads/` ada di root project.

---

## 🌐 Cara Menggunakan
1. **Register**: Daftar akun dengan verifikasi email.
2. **Login**: Masuk dan laporkan barang temuan.
3. **Admin**: Verifikasi, terima, atau tolak laporan.
4. **Riwayat**: Pantau status laporan.

---

## 🏃 Fitur Otomatis
- **Penghapusan otomatis** barang yang diterima setelah 3 hari.
- **Notifikasi email** untuk setiap perubahan status barang.

---

## 💻 Konfigurasi SMTP Gmail
- Aktifkan 2FA dan buat **App Password** di akun Google Anda.
- Gunakan App Password tersebut di `MAIL_PASSWORD`.

---

## 💾 Deployment
- Pastikan port yang digunakan tidak diblokir.
- Konfigurasi environment di layanan cloud jika diperlukan.
