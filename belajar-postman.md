# 📌 Panduan Dasar Postman

## 🔹 Apa Itu Postman?
Postman adalah alat yang digunakan untuk menguji API (Application Programming Interface). Dengan Postman, kita dapat melakukan permintaan HTTP dan melihat respons dari server tanpa harus menulis kode terlebih dahulu.

## 🔹 Mengapa Menggunakan Postman?
- **Mudah digunakan** - Antarmuka grafis yang ramah pengguna.
- **Mendukung berbagai metode HTTP** - GET, POST, PUT, DELETE, PATCH, dll.
- **Dapat menyimpan dan mengelola request** - Memudahkan pengujian API secara terstruktur.
- **Mendukung environment variables** - Mempermudah pengujian pada berbagai lingkungan (dev, staging, production).
- **Otomasi pengujian API** - Dapat digunakan untuk pengujian otomatis dengan skrip.

---

## 🔹 Cara Menggunakan Postman

### 1️⃣ **Menginstal Postman**
- Unduh Postman dari situs resminya: [https://www.postman.com/downloads/](https://www.postman.com/downloads/)
- Instal sesuai dengan sistem operasi yang digunakan (Windows, macOS, Linux).

### 2️⃣ **Menjalankan Request API**
1. **Buka Postman** dan pilih **"New Request"**.
2. Pilih **metode HTTP** (GET, POST, PUT, DELETE, dll.).
3. Masukkan **URL API** yang ingin diuji.
4. (Opsional) Tambahkan **header**, **body**, atau **parameter** yang diperlukan.
5. Klik **"Send"** untuk mengirim permintaan.
6. Lihat respons API di bagian bawah.

### 3️⃣ **Menambahkan Header dan Parameter**
- **Headers**: Digunakan untuk mengirim informasi tambahan seperti `Authorization`, `Content-Type`, dll.
- **Params**: Menambahkan parameter ke URL API (misalnya, `?id=123` untuk permintaan GET).
- **Body**: Digunakan dalam metode POST/PUT untuk mengirimkan data (JSON, form-data, dll.).

### 4️⃣ **Menggunakan Environment Variables**
- Klik ikon **"Manage Environments"**.
- Buat environment baru dan tambahkan variabel (misalnya, `{{base_url}}` untuk menyimpan URL API utama).
- Gunakan dalam request: `{{base_url}}/endpoint`.

### 5️⃣ **Otomasi dengan Skrip**
Postman mendukung **JavaScript scripting** untuk melakukan pengujian otomatis.
- **Pre-request Script**: Dijalankan sebelum request dikirim.
- **Test Script**: Dijalankan setelah respons diterima.

Contoh script untuk memeriksa status code:
```javascript
pm.test("Status code harus 200", function () {
    pm.response.to.have.status(200);
});
```

### 6️⃣ **Menyimpan dan Membagikan Koleksi API**
- Gunakan fitur **Collections** untuk menyimpan dan mengatur request API.
- Dapat diekspor dan dibagikan dengan tim.

---

## 🔹 Kesimpulan
Postman adalah alat yang sangat berguna untuk menguji API dengan mudah. Dengan fitur-fitur seperti environment variables, automation testing, dan collections, Postman dapat membantu dalam pengembangan dan debugging API dengan lebih efisien.

📌 **Selamat mencoba!** 🚀
