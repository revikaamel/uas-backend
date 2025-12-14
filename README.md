# 🎓 Sistem Pelaporan Prestasi Mahasiswa (Backend REST API)

## 👤 Detail Proyek
| Kategori | Data |
| :--- | :--- |
| **Pengembang** | Revika Amelinda Feftyana |
| **NIM** | 434231012 |
| **Kelas** | C4 |
---

## 🎯 Ringkasan Proyek

Ini adalah implementasi *backend* berbasis **REST API** untuk Sistem Pelaporan Prestasi Mahasiswa. [cite_start]Aplikasi ini dirancang untuk memungkinkan mahasiswa melaporkan prestasi, dosen wali memverifikasi, dan admin mengelola sistem secara keseluruhan[cite: 6].

Sistem ini menggunakan arsitektur **Dual Database** untuk mengelola:
1.  [cite_start]**PostgreSQL**: Untuk data relasional, pengguna, dan Role-Based Access Control (RBAC)[cite: 34].
2.  [cite_start]**MongoDB**: Untuk detail prestasi dinamis (fleksibel *field*)[cite: 106].

### 🔒 Fitur Keamanan Kunci
* [cite_start]**Autentikasi & Otorisasi**: Menggunakan **JWT** dan **RBAC**[cite: 160].
* [cite_start]**Workflow Status**: Mendukung alur status `'draft'`, `'submitted'`, `'verified'`, dan `'rejected'`[cite: 96].

---

## 👥 Hak Akses Pengguna

| Role | Deskripsi | Hak Akses Utama |
| :--- | :--- | :--- |
| **Mahasiswa** | Pelapor prestasi | [cite_start]**Create**, *Read*, *Update* prestasi sendiri[cite: 30]. |
| **Dosen Wali** | Verifikator prestasi | [cite_start]*Read* dan **Verify** prestasi mahasiswa bimbingannya[cite: 30]. |
| **Admin** | Pengelola sistem | [cite_start]*Full access* ke semua fitur[cite: 30]. |

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
