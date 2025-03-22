# Backend for Vendor Dashboard

This repository contains the backend code for a Vendor Dashboard application. The backend is built using Node.js, Express.js, and MongoDB. It provides APIs for managing vendors, firms, and products. The backend also handles user authentication and file uploads.

## Features

- **Vendor Management**: Register and log in vendors.
- **Firm Management**: Add and manage firms associated with vendors.
- **Product Management**: Add, retrieve, and delete products associated with firms.
- **Authentication**: Secure endpoints using JWT (JSON Web Tokens).
- **File Uploads**: Handle image uploads for firms and products.

## Project Structure

The project is structured as follows:

```
BACKEND
├── Controllers
│   ├── firmController.js
│   ├── productController.js
│   ├── vendorController.js
├── middlewares
│   └── verifyToken.js
├── models
│   ├── Firm.js
│   ├── Product.js
│   └── Vendor.js
├── node_modules
├── routes
│   ├── firmRoutes.js
│   ├── productRoutes.js
│   └── vendorRoutes.js
├── uploads
├── .env
├── .gitignore
├── classes.json
├── data.json
├── index.js
├── package-lock.json
└── package.json
```

## Key Components

### Controllers
- **firmController.js**: Handles firm-related operations such as adding and deleting firms.
- **productController.js**: Manages product-related operations including adding, retrieving, and deleting products.
- **vendorController.js**: Manages vendor registration, login, and retrieval of vendor details.

### Middlewares
- **verifyToken.js**: Middleware to verify JWT tokens for protected routes.

### Models
- **Firm.js**: Mongoose model for firms.
- **Product.js**: Mongoose model for products.
- **Vendor.js**: Mongoose model for vendors.

### Routes
- **firmRoutes.js**: Routes for firm-related operations.
- **productRoutes.js**: Routes for product-related operations.
- **vendorRoutes.js**: Routes for vendor-related operations.

### Uploads
- Directory for storing uploaded images.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/backend-vendor-dashboard.git
   ```
2. Navigate to the project directory:
   ```bash
   cd backend-vendor-dashboard
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Create a `.env` file in the root directory and add the following environment variables:
   ```env
   WhatIsYourName=your_secret_key
   MONGO_URI=your_mongodb_connection_string
   ```
5. Start the server:
   ```bash
   npm start
   ```

## API Endpoints

### Vendor Routes
- **POST /register**: Register a new vendor.
- **POST /login**: Log in a vendor.
- **GET /all-vendors**: Retrieve all vendors.
- **GET /single-vendor/:apple**: Retrieve a single vendor by ID.

### Firm Routes
- **POST /add-firm**: Add a new firm (protected route).
- **DELETE /:firmId**: Delete a firm by ID.

### Product Routes
- **POST /add-product/:firmId**: Add a new product to a firm.
- **GET /:firmId/products**: Retrieve all products for a firm.
- **DELETE /:productId**: Delete a product by ID.

## Usage

- **Vendor Registration**: Use the `/register` endpoint to register a new vendor.
- **Vendor Login**: Use the `/login` endpoint to log in a vendor and receive a JWT token.
- **Add Firm**: Use the `/add-firm` endpoint to add a new firm (requires authentication).
- **Add Product**: Use the `/add-product/:firmId` endpoint to add a new product to a firm.
- **Retrieve Products**: Use the `/:firmId/products` endpoint to retrieve all products for a firm.
- **Delete Product**: Use the `/:productId` endpoint to delete a product by ID.

## Dependencies

- **Express.js**: Web framework for Node.js.
- **Mongoose**: MongoDB object modeling for Node.js.
- **Multer**: Middleware for handling file uploads.
- **Bcryptjs**: Library for hashing passwords.
- **Jsonwebtoken**: Library for generating and verifying JWT tokens.
- **Dotenv**: Loads environment variables from a `.env` file.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments

- Node.js
- Express.js
- MongoDB
- Mongoose
- Multer
- Bcryptjs
- Jsonwebtoken

---

This README provides an overview of the backend structure, features, and instructions for installation and usage. Adjustments can be made based on specific project requirements or additional features.
