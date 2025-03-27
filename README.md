# Laravel Auth & Products API - Laravel 12

This is a simple Laravel 12 API project that implements user authentication and product management using Laravel Sanctum.

## Features

- User registration & login (Auth API)
- Secure authentication using Laravel Sanctum
- CRUD operations for products
- Middleware-protected routes for secure access

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/sylvancart/laravel-auth-products-api.git
   cd laravel-auth-products-api
   ```
2. Install dependencies:
   ```sh
   composer install
   ```
3. Set up environment:
   ```sh
   cp .env.example .env
   php artisan key:generate
   ```
4. Configure database in `.env` file and run migrations:
   ```sh
   php artisan migrate
   ```
5. Serve the application:
   ```sh
   php artisan serve
   ```

## API Endpoints

### Auth Routes:
- `POST /api/auth/register` – Register a new user
- `POST /api/auth/login` – Login user & get token
- `POST /api/auth/logout` – Logout (Requires authentication)

### Product Routes:
- `GET /api/products` – List all products (Requires authentication)
- `POST /api/product/add` – Add a new product
- `GET /api/products/{id}` – Get details of a specific product
- `PUT /api/products/{id}` – Update product details
- `DELETE /api/products/delete/{id}` – Delete a product
