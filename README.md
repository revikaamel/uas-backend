# 🎓 Sistem Pelaporan Prestasi Mahasiswa (Backend REST API)

## 👤 Detail Proyek
| Kategori | Data |
| :--- | :--- |
| **Pengembang** | Revika Amelinda Feftyana |
| **NIM** | 434231012 |
| **Kelas** | C4 |
---

## 🎯 Ringkasan Proyek

Ini adalah implementasi *backend* berbasis **REST API** untuk Sistem Pelaporan Prestasi Mahasiswa. Aplikasi ini dirancang untuk memungkinkan mahasiswa melaporkan prestasi, dosen wali memverifikasi, dan admin mengelola sistem secara keseluruhan.

Sistem ini menggunakan arsitektur **Dual Database** untuk mengelola:
1.  **PostgreSQL**: Untuk data relasional, pengguna, dan Role-Based Access Control (RBAC).
2.  **MongoDB**: Untuk detail prestasi dinamis (fleksibel *field*).

### 🔒 Fitur Keamanan Kunci
* **Autentikasi & Otorisasi**: Menggunakan **JWT** dan **RBAC**.
* **Workflow Status**: Mendukung alur status `'draft'`, `'submitted'`, `'verified'`, dan `'rejected'`.

---

## 👥 Hak Akses Pengguna

| Role | Deskripsi | Hak Akses Utama |
| :--- | :--- | :--- |
| **Mahasiswa** | Pelapor prestasi | **Create**, *Read*, *Update* prestasi sendiri. |
| **Dosen Wali** | Verifikator prestasi | *Read* dan **Verify** prestasi mahasiswa bimbingannya. |
| **Admin** | Pengelola sistem | *Full access* ke semua fitur. |

---

## ⚙️ Panduan Setup Lokal

### Prasyarat
Pastikan Anda telah menginstal komponen berikut:
1.  **Go** (Versi 1.18+)
2.  **PostgreSQL**
3.  **MongoDB**

### Langkah-Langkah

#### 1. Kloning Repository

Buka Terminal Anda dan *clone* proyek:

```bash
git clone [URL_REPOSITORY_ANDA]
cd nama-repository-anda
