# Ibnu Faisal -- Backend Engineering Portfolio

Selamat datang di portfolio saya. Saya adalah seorang **Backend
Engineer** yang berfokus pada **NestJS**, **Golang**, **Database
Design**, dan **microservices architecture**.\
Di bawah ini adalah daftar proyek-proyek yang pernah saya kerjakan,
lengkap dengan deskripsi singkat, teknologi utama, serta arsitektur yang
digunakan.

## 🚀 Daftar Proyek

## 1. Warehouse Core API (NestJS)

API utama yang menangani seluruh proses bisnis warehouse, meliputi
pengelolaan stok, barang masuk/keluar, dan sinkronisasi data antar
layanan.

### ✦ Deskripsi

-   Membangun REST API terstruktur menggunakan **NestJS**.
-   Mengimplementasikan autentikasi & otorisasi JWT.
-   Menyusun service modular agar mudah diskalakan.
-   Dibuat agar bisa digunakan oleh banyak client internal maupun
    external.

### ✦ Fitur Utama

-   Manajemen stok
-   Manajemen warehouse / lokasi penyimpanan
-   Barang masuk (inbound) / keluar (outbound)
-   Audit & log aktivitas
-   Rate limiting untuk keamanan API

### ✦ Tech Stack

-   NestJS
-   PostgreSQL
-   TypeORM / Sequelize
-   Redis
-   Docker

## 2. Integration API for Multi-Client

API middleware yang bertugas menjembatani berbagai konfigurasi client
dengan Core API.

### ✦ Deskripsi

-   Membuat "Integration Service" agar client dapat menggunakan API
    warehouse dengan konfigurasi berbeda.
-   Menyediakan mapping data, transformasi payload, dan adapter per
    client.
-   Menjaga agar Core API tetap bersih dan generik.

### ✦ Fitur Utama

-   Adapter berbasis client
-   Payload transformation
-   Auth bridging (API key → JWT)
-   Logging per client
-   Rate limiting per client

### ✦ Tech Stack

-   NestJS / Express
-   PostgreSQL
-   Redis
-   RabbitMQ / Kafka

## 3. Golang CLI for CSV Migration to PostgreSQL

CLI tool berbasis Go untuk memigrasikan data CSV ke tabel blogs atau
tabel lain dengan filtering & mapping yang fleksibel.

### ✦ Deskripsi

-   Membaca file CSV besar.
-   Filter berdasarkan post_type = post dan post_status = publish.
-   Mapping kolom CSV ke database.
-   Pekerjaan paralel menggunakan goroutine.

### ✦ Fitur Utama

-   CLI command: import, validate
-   Parallel processing
-   Logging progress & error
-   Konfigurasi via YAML atau flags

### ✦ Tech Stack

-   Golang
-   pgx / GORM
-   Cobra CLI
-   YAML

## 4. Database Design for Inventory & Stock Management

### ✦ Deskripsi

-   Mendesain ERD untuk alur inventory.
-   Memastikan konsistensi data.
-   Optimasi query menggunakan index.

### ✦ Fitur Utama

-   Tabel master dan transaksi
-   Soft delete & audit fields
-   UUID primary key
-   Constraint untuk mencegah invalid stock

### ✦ Tech Stack

-   PostgreSQL
-   pgModeler / DrawSQL
-   Sequelize

## 5. Microservices: Core vs Integration Architecture

### ✦ Deskripsi

Desain arsitektur untuk memisahkan Core Service dan Integration Service
agar aplikasi modular.

### ✦ Diagram Konsep

    ┌──────────────────────┐
    │   Client A / B / C   │
    └──────────┬───────────┘
               │
               ▼
    ┌──────────────────────┐
    │  Integration Service │
    └──────────┬───────────┘
               │
               ▼
    ┌──────────────────────┐
    │      Core Service    │
    └──────────────────────┘

### ✦ Manfaat

-   Core stabil & bersih\
-   Integration fleksibel\
-   Menghindari technical debt

## 📫 Kontak

-   GitHub: https://github.com/ibnufaisal
