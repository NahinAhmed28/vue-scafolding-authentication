# Vue Scafolding Authentication

Vue Scafolding Authentication is an authentication-focused scaffold using Laravel/Vue project structure.

## Features

- Authentication workflow starter
- Laravel backend foundation
- Vue/front-end integration path
- Database-backed users and sessions when configured

## Modules

- Auth module: login, registration, guards, and sessions
- User module: user records, roles, and profile data
- Frontend module: Vue components and auth screens
- Backend module: controllers, routes, and validation
- Data module: migrations, models, and seeders

## System Architecture

The system follows a Laravel full-stack architecture. Laravel handles authentication, validation, and persistence. Vue components can render interactive auth screens. Database tables store users, sessions, and related permissions. Environment variables configure app and database values.

## Getting Started

```bash
git clone https://github.com/NahinAhmed28/vue-scafolding-authentication.git
cd vue-scafolding-authentication
composer install
cp .env.example .env
php artisan key:generate
npm install
npm run dev
php artisan serve
```
