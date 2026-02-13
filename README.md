# Клонируем проект
git clone https://github.com/HasmikManucharyan/api_test.git
cd api_test

# Установка зависимостей (если нужно)
composer install

# Создать .env
# Windows
copy .env.example .env
# Linux / Mac
cp .env.example .env
php artisan key:generate

# Создать SQLite базу
# Windows
New-Item -ItemType File -Path "database\database.sqlite"
# Linux / Mac
touch database/database.sqlite

# Настроить .env
# DB_CONNECTION=sqlite
# DB_DATABASE=database/database.sqlite

# Применить миграции
php artisan migrate

# Запустить сервер
php artisan serve


| Действие        | Метод  | URL             |
| --------------- | ------ | --------------- |
| Все задачи      | GET    | /api/tasks      |
| Создать задачу  | POST   | /api/tasks      |
| Задача по ID    | GET    | /api/tasks/{id} |
| Обновить задачу | PUT    | /api/tasks/{id} |
| Удалить задачу  | DELETE | /api/tasks/{id} |
