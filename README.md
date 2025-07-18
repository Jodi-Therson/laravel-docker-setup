# 🚀 Laravel + Docker Starter Project

This project is a Laravel application fully containerized using Docker, with MySQL and Nginx out of the box. Compatible with Windows, Linux, and macOS.

---

## 🧰 Stack

- Laravel 10
- PHP 8.2 (or custom version)
- MySQL 8
- Nginx
- Docker & Docker Compose

---

## 🧪 Getting Started

### 1. Clone the Repository

```
git clone https://github.com/yourusername/your-laravel-project.git
cd your-laravel-project
```

### 2. Copy the .env file
```
cp .env.example .env
```
Edit it if needed (e.g. database name/password).

### 3. Build and Run Containers
```
docker-compose up -d
```

### 4. Enter the App Container
```
docker exec -it laravel-app bash
```
Inside the container:
```
composer install
php artisan key:generate
php artisan migrate
```

## 📂 Folder Structure
```
├── app/                # Laravel source code
├── nginx/              # Nginx config
│   └── default.conf
├── Dockerfile          # PHP app container
├── docker-compose.yml  # Docker services
├── .env.example        # Laravel config (no secrets)
└── README.md           # Setup guide
```

## ✅ Tips

To stop containers: docker-compose down

Laravel logs: storage/logs/laravel.log

Permissions: chown -R www-data:www-data storage bootstrap/cache