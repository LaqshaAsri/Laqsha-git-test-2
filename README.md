## Daftar Anggota dan Pembagian Tugas

Disini kami bekerja berdasarkan tabel jadi tiap tabel dicoding oleh 1 orang.

- 241111160 - Marcellino Tanaka = Tabel Users
- 241111879 - Ahmad Ziham = Tabel Authors & Borrowings
- 241112227 - Laqsha Asri = Menyiapkan folder kerja (pembuatan database, koneksi ke database) & Tabel Categories
- 241112424 - Tubagus Arsad = Tabel Books

## Struktur Proyek

Folder dan file utama yang harus didownload, bertanda - berarti opsional:
UTS/
├── config/
│ └── db.js
├── models/
│ ├── authorsModel.js
│ ├── booksModel.js
│ ├── borrowingsModel.js
│ ├── categoriesModel.js
│ └── usersModel.js
├── routes/
│ ├── authorsRoute.js
│ ├── booksRoute.js
│ ├── borrowingRoute.js
│ ├── categoriesRoute.js
│ └── usersRoute.js
├── index.js
├── init.sql
├── package.json
├── package-lock.json
└── README.md

## Panduan Setup:

1. Download Folder UTS yang ada di OneDrive dengan isi utama:
2. config = koneksi ke database
3. models = folder yang menyimpan query ke database untuk memanipulasi data
4. routes = folder yang menyimpan routing
5. index.js = file utama
6. init.sql = inisialisasi sql agar database terbentuk
7. package.json dan package-lock.json
8. Import terlebih dahulu file init.sql di database phpmyadmin agar database terbentuk
9. Lalu masuk ke folder UTS yang telah di download dan lakukan perintah (npm install express mysql2)
10. Run program menggunakan "node index.js" atau "nodemon index.js"
11. Server akan berjalan di: http://127.0.0.1:1140  
    • Program sudah bisa diuji di Postman, ThunderClient atau Software pengetesan API lainnya
12. Notes:
    • Pastikan MySQL sudah berjalan (Apache✔️, MySQL✔️)
    • Pastikan port tidak tabrakan
    • Gunakan JSON body untuk POST/PUT

## Struktur Routing:

- /authors
- /books
- /borrow
- /category
- /users

## Contoh Routing:

- /nama-tabel/ = GET
- /nama-tabel?q=... ?page=...&limit=... = GET Query/Pagination
- /nama-tabel/:id = GET by Id
- /nama-tabel/ = POST
- /nama-tabel/:id = PUT
- /nama-tabel/:id = DELETE by Id
- /nama-tabel/ = DELETE ALL

## Contoh request/response & skema error

#### 1. Tabel Authors

##### Request GET /authors/

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request GET /authors?q=novel&page=1&limit=2

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request GET /authors/1

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request POST /authors/

**Content-Type: application/json**

**Body**

```json

```

**Response Success (201) - Data Berhasil ditambahkan**

```json

```

**Response Error (400) - Field Kosong**

```json

```

**Response Error (400) - Data Duplikat**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request PUT /authors/:id

**Content-Type: application/json**

**Body**

```json

```

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (400) - Field Kosong**

```json

```

**Response Error (404) - Data Tidak Ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request DELETE /authors/1

**Response Success (200) - Data Berhasil dihapus**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request DELETE /authors/

**Response Success (200) - Data Berhasil dihapus**

```json

```

**Response Error (500) - Server Error**

```json

```

#### 2. Tabel Books

##### Request GET /books/

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request GET /books?q=novel&page=1&limit=2

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request GET /books/1

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request POST /books/

**Content-Type: application/json**

**Body**

```json

```

**Response Success (201) - Data Berhasil ditambahkan**

```json

```

**Response Error (400) - Field Kosong**

```json

```

**Response Error (400) - Data Duplikat**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request PUT /books/:id

**Content-Type: application/json**

**Body**

```json

```

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (400) - Field Kosong**

```json

```

**Response Error (404) - Data Tidak Ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request DELETE /books/1

**Response Success (200) - Data Berhasil dihapus**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request DELETE /books/

**Response Success (200) - Data Berhasil dihapus**

```json

```

**Response Error (500) - Server Error**

```json

```

#### 3. Tabel Borrowings

##### Request GET /borrow/

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request GET /borrow?q=novel&page=1&limit=2

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request GET /borrow/1

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request POST /borrow/

**Content-Type: application/json**

**Body**

```json

```

**Response Success (201) - Data Berhasil ditambahkan**

```json

```

**Response Error (400) - Field Kosong**

```json

```

**Response Error (400) - Data Duplikat**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request PUT /borrow/:id

**Content-Type: application/json**

**Body**

```json

```

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (400) - Field Kosong**

```json

```

**Response Error (404) - Data Tidak Ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request DELETE /borrow/1

**Response Success (200) - Data Berhasil dihapus**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request DELETE /borrow/

**Response Success (200) - Data Berhasil dihapus**

```json

```

**Response Error (500) - Server Error**

```json

```

#### 4. Tabel Categories

##### Request GET /category/

**Response Success (200) - Data Berhasil diambil**

```json
{
  "status": 200,
  "message": "Berhasil mengambil data",
  "data": [
    {
      "category_id": 1,
      "category_name": "Novel"
    },
    {
      "category_id": 2,
      "category_name": "Fantasy"
    },
    {
      "category_id": 3,
      "category_name": "Drama"
    },
    {
      "category_id": 4,
      "category_name": "Science Fiction"
    },
    {
      "category_id": 5,
      "category_name": "Mystery"
    }
  ]
}
```

**Response Error (404) - Data Tidak ditemukan**

```json
{
  "status": 404,
  "message": "Data kategori tidak ditemukan"
}
```

**Response Error (500) - Server Error**

```json
{
  "status": 500,
  "message": "Terjadi kesalahan pada server",
  "error": "Error message dari database"
}
```

##### Request GET /category?q=novel&page=1&limit=2

**Response Success (200) - Data Berhasil diambil**

```json
{
  "status": 200,
  "message": "Berhasil mengambil data",
  "data": [
    {
      "category_id": 1,
      "category_name": "Novel"
    }
  ]
}
```

**Response Error (404) - Data Tidak ditemukan**

```json
{
  "status": 404,
  "message": "Data kategori tidak ditemukan"
}
```

**Response Error (500) - Server Error**

```json
{
  "status": 500,
  "message": "Terjadi kesalahan pada server",
  "error": "Isi pesan error dari database"
}
```

##### Request GET /category/1

**Response Success (200) - Data Berhasil diambil**

```json
{
  "status": 200,
  "message": "Berhasil mengambil data",
  "data": [
    {
      "category_id": 1,
      "category_name": "Novel"
    }
  ]
}
```

**Response Error (404) - Data Tidak ditemukan**

```json
{
  "status": 404,
  "message": "Data tidak ditemukan"
}
```

**Response Error (500) - Server Error**

```json
{
  "status": 500,
  "message": "Terjadi kesalahan pada server",
  "error": "Isi pesan error dari database"
}
```

##### Request POST /category/

**Content-Type: application/json**

**Body**

```json
{
  "category_name": "Horror"
}
```

**Response Success (201) - Data Berhasil ditambahkan**

```json
{
  "status": 201,
  "message": "Berhasil menambahkan data",
  "id": 6
}
```

**Response Error (400) - Field Kosong**

```json
{
  "status": 400,
  "message": "category_name wajib diisi"
}
```

**Response Error (400) - Data Duplikat**

```json
{
  "status": 400,
  "message": "Category Name sudah ada"
}
```

**Response Error (500) - Server Error**

```json
{
  "status": 500,
  "message": "Terjadi kesalahan pada server",
  "error": "Isi pesan error dari database"
}
```

##### Request PUT /category/:id

**Content-Type: application/json**

**Body**

```json
{
  "category_name": "Romance"
}
```

**Response Success (200) - Data Berhasil diambil**

```json
{
  "message": "Category berhasil diupdate"
}
```

**Response Error (400) - Field Kosong**

```json
{
  "status": 400,
  "message": "category_name wajib diisi"
}
```

**Response Error (404) - Data Tidak Ditemukan**

```json
{
  "status": 404,
  "message": "Data tidak ditemukan"
}
```

**Response Error (500) - Server Error**

```json
{
  "status": 500,
  "message": "Terjadi kesalahan pada server",
  "error": "Isi pesan error dari database"
}
```

##### Request DELETE /category/1

**Response Success (200) - Data Berhasil dihapus**

```json
{
  "message": "Category berhasil dihapus"
}
```

**Response Error (404) - Data Tidak ditemukan**

```json
{
  "status": 404,
  "message": "Data tidak ditemukan"
}
```

**Response Error (500) - Server Error**

```json
{
  "status": 500,
  "message": "Terjadi kesalahan pada server",
  "error": "Isi pesan error dari database"
}
```

##### Request DELETE /category/

**Response Success (200) - Data Berhasil dihapus**

```json
{
  "message": "Semua data category berhasil dihapus"
}
```

**Response Error (500) - Server Error**

```json
{
  "status": 500,
  "message": "Terjadi kesalahan pada server",
  "error": "Isi pesan error dari database"
}
```

#### 5. Tabel Users

##### Request GET /users/

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request GET /users?q=novel&page=1&limit=2

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request GET /users/1

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request POST /users/

**Content-Type: application/json**

**Body**

```json

```

**Response Success (201) - Data Berhasil ditambahkan**

```json

```

**Response Error (400) - Field Kosong**

```json

```

**Response Error (400) - Data Duplikat**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request PUT /users/:id

**Content-Type: application/json**

**Body**

```json

```

**Response Success (200) - Data Berhasil diambil**

```json

```

**Response Error (400) - Field Kosong**

```json

```

**Response Error (404) - Data Tidak Ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request DELETE /users/1

**Response Success (200) - Data Berhasil dihapus**

```json

```

**Response Error (404) - Data Tidak ditemukan**

```json

```

**Response Error (500) - Server Error**

```json

```

##### Request DELETE /users/

**Response Success (200) - Data Berhasil dihapus**

```json

```

**Response Error (500) - Server Error**

```json

```
