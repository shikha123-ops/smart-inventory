# 🚀 Smart Inventory

<div align="center">

![GitHub forks](https://img.shields.io/github/forks/USERNAME/smart-inventory?style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/USERNAME/smart-inventory?style=for-the-badge)
![License](https://img.shields.io/github/license/USERNAME/smart-inventory?style=for-the-badge)

### Intelligent Inventory Management Made Simple

A modern full-stack inventory management system designed to help businesses efficiently track products, manage stock levels, and streamline inventory operations.

</div>

---

## 📚 Table of Contents

- Overview
- Features
- Tech Stack
- Project Structure
- Getting Started
- Environment Variables
- API Documentation
- Screenshots
- Contributing
- Future Enhancements
- License

## 📖 Overview

Smart Inventory is a comprehensive inventory management platform that enables users to monitor stock levels, manage products, and maintain accurate inventory records through an intuitive web interface.


### ✨ Key Features

- 📦 Product Inventory Management
- ➕ Add New Products
- ✏️ Update Existing Products
- 🗑️ Delete Products
- 📊 Real-Time Stock Tracking
- 💰 Sales Recording System
- 🔄 Automatic Inventory Updates After Sales
- 🌐 RESTful API Architecture
- 📱 Responsive User Interface 

---

## 🛠️ Tech Stack

### Frontend

| Technology | Purpose |
|------------|---------|
| React.js | User Interface |
| Vite | Frontend Build Tool |
| JavaScript | Application Logic |
| CSS | Styling |

### Backend

| Technology | Purpose |
|------------|---------|
| Node.js | Runtime Environment |
| Express.js | REST API Framework |
| MongoDB | Database |
| Mongoose | MongoDB Object Modeling |
| CORS | Cross-Origin Resource Sharing |
| dotenv | Environment Variable Management |
| Nodemon | Development Server Reloading |

---

## 🏗️ Project Structure

```text
smart-inventory/
│
├── backend/
│   ├── models/
│   ├── routes/
│   │   ├── productRoutes.js
│   │   └── saleRoutes.js
│   ├── server.js
│   ├── seed.js
│   ├── package.json
│   └── package-lock.json
│
├── frontend/
│   ├── public/
│   ├── src/
│   ├── package.json
│   ├── package-lock.json
│   └── vite.config.js
│
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed:

* Node.js (v18+ recommended)
* npm or yarn
* MongoDB

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/USERNAME/smart-inventory.git
cd smart-inventory
```

#### 2. Install Frontend Dependencies

```bash
cd frontend
npm install
```

#### 3. Install Backend Dependencies

```bash
cd ../backend
npm install
```

---

## ⚙️ Environment Variables

Create a `.env` file inside the `backend` directory and add the following variables:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
```

| Variable | Description |
|----------|-------------|
| PORT | Port on which the backend server runs |
| MONGO_URI | MongoDB connection string used by the application |

> Ensure MongoDB is running locally or provide a valid MongoDB Atlas connection string before starting the server.


## ▶️ Running the Application

### Start Backend Server

```bash
cd backend
npm run dev
```

### Start Frontend Application

```bash
cd frontend
npm start
```

Frontend:

```text
http://localhost:3000
```

Backend:

```text
http://localhost:5000
```

---

## 📡 API Documentation

The Smart Inventory backend provides RESTful APIs for managing products and recording sales transactions.

### Product Endpoints

| Method | Endpoint            | Description                                 |
| ------ | ------------------- | ------------------------------------------- |
| GET    | `/api/products`     | Retrieve all products sorted alphabetically |
| POST   | `/api/products`     | Create a new product                        |
| PUT    | `/api/products/:id` | Update an existing product                  |
| DELETE | `/api/products/:id` | Delete a product                            |

#### Product Request Body

```json
{
  "name": "Laptop",
  "stock": 25,
  "price": 999.99,
  "category": "Electronics",
  "threshold": 5
}
```

---

### Sales Endpoints

| Method | Endpoint     | Description                                  |
| ------ | ------------ | -------------------------------------------- |
| GET    | `/api/sales` | Retrieve all sales records                   |
| POST   | `/api/sales` | Record a new sale and update inventory stock |

#### Sales Request Body

```json
{
  "productId": "64abc123xyz",
  "quantity": 2
}
```

#### Sales Processing Logic

When a sale is recorded:

1. The selected product is retrieved from the database.
2. Product availability is verified.
3. Total sale value is calculated automatically.
4. A sales record is created.
5. Product stock is reduced accordingly.
6. Updated inventory data is saved.

---

### Response Codes

| Status Code | Meaning                               |
| ----------- | ------------------------------------- |
| 200         | Request completed successfully        |
| 201         | Resource created successfully         |
| 400         | Invalid request or insufficient stock |
| 404         | Product not found                     |
| 500         | Internal server error                 |

---

## 📸 Screenshots

### Dashboard

```text
Add dashboard screenshot here
```

### Product Management

```text
Add product management screenshot here
```

### Inventory Overview

```text
Add inventory overview screenshot here
```

---

## 🤝 Contributing

Contributions are welcome and greatly appreciated.

### Contribution Workflow

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature/amazing-feature
```

3. Commit your changes

```bash
git commit -m "feat: add amazing feature"
```

4. Push your branch

```bash
git push origin feature/amazing-feature
```

5. Open a Pull Request

### Commit Convention

* `feat:` New features
* `fix:` Bug fixes
* `docs:` Documentation changes
* `refactor:` Code improvements
* `style:` Formatting updates

---

## 🌟 Future Enhancements

* User Authentication & Authorization
* Role-Based Access Control
* Inventory Analytics Dashboard
* Export Reports (CSV/PDF)
* Barcode & QR Code Integration
* Low Stock Notifications

---

## 📄 License

This project is licensed under the ISC License.

See the LICENSE file for complete details.

---

<div align="center">

### ⭐ If you find this project useful, consider giving it a star!

Made with ❤️ by the Smart Inventory Contributors

</div>
