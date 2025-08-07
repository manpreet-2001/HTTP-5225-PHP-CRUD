# FakeStudent - Laravel CRUD Application

This is a simple Laravel-based student management web app. It allows you to create, read, update, and delete (CRUD) student records using Laravel Resource Controllers.

## Features

- Add new students
- View student details
- Edit existing student info
- Delete students
- Simple and clean UI using Blade
- Soft delete & restore feature 


## 🛠️ Setup Instructions

Follow these steps to run the project locally on your system:

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/manpreet-2001/HTTP-5225-PHP-CRUD.git
cd HTTP-5225-PHP-CRUD
```

### 2️⃣ Install Dependencies

```bash
composer install
```

### 3️⃣ Create Environment File

```bash
cp .env.example .env
```

> ✅ Open `.env` file and update the following for your local MySQL:

```
DB_DATABASE=your_db_name
DB_USERNAME=root
DB_PASSWORD=
```

### 4️⃣ Generate Application Key

```bash
php artisan key:generate
```

### 5️⃣ Run Migrations

```bash
php artisan migrate
```

> ⚠️ If you see an error about `deleted_at` column, make sure your `students` table includes soft deletes:

```php
$table->softDeletes(); // in your migration file
```

Then re-run:

```bash
php artisan migrate:fresh
```

### 6️⃣ Serve the Application

```bash
php artisan serve
```

Open your browser and visit: [http://127.0.0.1:8000](http://127.0.0.1:8000)

---

