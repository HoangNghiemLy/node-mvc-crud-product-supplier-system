# Product & Supplier Management System

A web application for managing products and suppliers with full CRUD features, user authentication, and session security.

## Features

- **Product Management**: Add, edit, delete, and view product list
- **Supplier Management**: Add, edit, delete, and view supplier list
- **Search & Filter**: Search products by name, filter by supplier
- **User Authentication**: Register, login, logout
- **Security**: All CRUD functions require login
- **Forgot Password**: Reset password via email

## Technologies

- **Backend**: Node.js, Express.js
- **Database**: MongoDB with Mongoose ODM
- **Template Engine**: EJS
- **UI Framework**: Bootstrap 5
- **Authentication**: bcryptjs, express-session
- **Email**: nodemailer

## Setup

1. **Clone the repository**

```bash
git clone <repository-url>
cd node-mvc-crud-product-supplier-system
```

2. **Install dependencies**

```bash
npm install
```

3. **Create .env file**

```env
MONGO_URI=mongodb://localhost:27017/product_supplier_db
SESSION_SECRET=your-secret-key
```

4. **Seed sample data**

```bash
npm run seed
```

5. **Start the application**

```bash
npm start
```

Visit: http://localhost:3000

## Demo Account

- **Username**: admin
- **Password**: 123456
- **Email**: admin@example.com

## Folder Structure

```
├── app.js              # Main application entry point
├── package.json        # Project dependencies and scripts
├── seed.js             # Sample data seeding script
├── .env                # Environment variables
├── config/             # Configuration files
├── controllers/        # Route handlers (controllers)
├── middleware/         # Custom middleware functions
├── models/             # Mongoose data models
├── routes/             # Express route definitions
├── views/              # EJS template files
└── public/             # Static assets (CSS, JS, images)
```

## API Routes

### Authentication

- `GET /auth/login` - Login page
- `POST /auth/login` - Handle login
- `GET /auth/register` - Register page
- `POST /auth/register` - Handle registration
- `GET /auth/logout` - Logout

### Products (Require login)

- `GET /products` - Product list
- `GET /products/new` - Create product form
- `POST /products` - Create new product
- `GET /products/:id/edit` - Edit product form
- `PUT /products/:id` - Update product
- `DELETE /products/:id` - Delete product

### Suppliers (Require login)

- `GET /suppliers` - Supplier list
- `GET /suppliers/new` - Create supplier form
- `POST /suppliers` - Create new supplier
- `GET /suppliers/:id/edit` - Edit supplier form
- `PUT /suppliers/:id` - Update supplier
- `DELETE /suppliers/:id` - Delete supplier

---

_This application is developed for learning and practice purposes._
