# Lab 7: PHP CodeIgniter 4 & Vue.js

Proyek ini menghubungkan backend CodeIgniter 4 dengan frontend Vue.js untuk membuat aplikasi CRUD artikel.

## Struktur Proyek
```
lab7_php_ci/
├── app/                # CI4 App (versi 1)
├── ci4/                # CI4 App (versi 2, dengan frontend Vue)
│   ├── app/
│   ├── frontend VueJS/ # Frontend Vue.js
│   └── public/
└── ...
```

## Menjalankan Backend (CodeIgniter 4)
Pastikan XAMPP sudah berjalan, lalu akses backend di:
`http://localhost/lab7_php_ci/ci4/public`

## Menjalankan Frontend (Vue.js)
Buka file `ci4/frontend VueJS/index.html` di browser.

## API Endpoints
| Method | Endpoint        | Description               |
|--------|-----------------|---------------------------|
| GET    | /post           | Ambil semua artikel       |
| POST   | /post           | Tambah artikel baru       |
| PUT    | /post/:id       | Update artikel by ID      |
| DELETE | /post/:id       | Hapus artikel by ID       |
