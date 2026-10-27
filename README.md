# Cloud-Based Canteen Pre-Order System

A simple college canteen pre-order web application built with Flask and MySQL.

## Features

### Student
- Register/login
- View available food
- Add items to cart
- Place order
- Get unique order ID
- Track order status
- View previous orders

### Admin
- Dashboard
- View all orders
- Change order status
- Add food
- Toggle food availability

## Technology
- Python Flask
- MySQL
- HTML/CSS/Bootstrap/JavaScript
- AWS EC2 for application hosting
- AWS RDS for MySQL database

## Local setup

1. Install Python 3.11+ and MySQL.
2. Create database using `database/schema.sql`.
3. Create virtual environment:
   `python -m venv venv`
4. Activate it.
5. Install:
   `pip install -r requirements.txt`
6. Set environment variables from `.env.example`.
7. Run:
   `python app.py`
8. Open:
   `http://127.0.0.1:5000`

## Admin account

For the first admin, create a password hash with:

`python -c "from werkzeug.security import generate_password_hash; print(generate_password_hash('Admin@123'))"`

Then insert it into MySQL:

`INSERT INTO users(name,email,student_id,password_hash,role) VALUES ('Canteen Admin','admin@college.com',NULL,'PASTE_HASH_HERE','admin');`

Change the password before any real deployment.

## AWS
See `AWS_DEPLOYMENT.md`.
