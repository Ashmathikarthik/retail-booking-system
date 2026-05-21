# Retail Booking System

A complete full-stack retail booking application with user authentication, product management, shopping cart, and order tracking.

## 🎯 Features

### User Features
- ✅ User Registration & Login with JWT Authentication
- ✅ Browse Products
- ✅ Add/Remove Items to Cart
- ✅ Place Orders
- ✅ Track Order Status
- ✅ View Order History

### Shop Owner Features
- ✅ Dashboard with Sales Analytics
- ✅ Product Management (Create, Read, Update, Delete)
- ✅ Inventory Management
- ✅ Order Management
- ✅ View Customer Orders

### Admin Features
- ✅ Admin Panel
- ✅ User Management
- ✅ All Orders Overview
- ✅ System Statistics

## 🛠 Tech Stack

### Backend
- **Framework**: FastAPI
- **Database**: SQLite with SQLAlchemy ORM
- **Authentication**: JWT (JSON Web Tokens)
- **Validation**: Pydantic

### Frontend
- **Framework**: React 18
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **Routing**: React Router v6
- **HTTP Client**: Axios
- **Notifications**: React Toastify

## 📁 Project Structure

```
retail-booking-system/
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   ├── config.py
│   ├── database.py
│   ├── models.py
│   ├── schemas.py
│   ├── routers/
│   │   ├── auth.py
│   │   ├── users.py
│   │   ├── products.py
│   │   ├── cart.py
│   │   ├── orders.py
│   │   └── admin.py
│   ├── utils/
│   │   ├── jwt_utils.py
│   │   └── security.py
│   └── sample_data.py
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── context/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── public/
│   ├── vite.config.js
│   ├── tailwind.config.js
│   ├── package.json
│   └── .env.example
└── README.md
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Node.js 14+
- npm or yarn

### Backend Setup

1. Navigate to backend directory:
```bash
cd backend
```

2. Create virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the server:
```bash
uvicorn main:app --reload
```

The backend will be available at `http://localhost:8000`

### Frontend Setup

1. Navigate to frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file:
```bash
cp .env.example .env
```

4. Run the development server:
```bash
npm run dev
```

The frontend will be available at `http://localhost:5173`

## 📚 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/refresh` - Refresh token

### Products
- `GET /api/products` - Get all products
- `GET /api/products/{id}` - Get product details
- `POST /api/products` - Create product (Owner only)
- `PUT /api/products/{id}` - Update product (Owner only)
- `DELETE /api/products/{id}` - Delete product (Owner only)

### Cart
- `GET /api/cart` - Get cart items
- `POST /api/cart` - Add to cart
- `PUT /api/cart/{item_id}` - Update cart item
- `DELETE /api/cart/{item_id}` - Remove from cart

### Orders
- `POST /api/orders` - Place order
- `GET /api/orders` - Get user orders
- `GET /api/orders/{id}` - Get order details
- `PUT /api/orders/{id}/status` - Update order status (Admin/Owner)

### Admin
- `GET /api/admin/users` - Get all users
- `GET /api/admin/stats` - Get statistics

## 🔐 Default Credentials

After running sample data:
- **Admin**: `admin@retail.com` / `admin123`
- **Owner**: `owner@retail.com` / `owner123`
- **Customer**: `customer@retail.com` / `customer123`

## 📝 Environment Variables

### Backend (.env)
```
DATABASE_URL=sqlite:///./retail_booking.db
SECRET_KEY=your-secret-key-here
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
```

### Frontend (.env)
```
VITE_API_BASE_URL=http://localhost:8000/api
```

## 🧪 Testing

### Test Login
```bash
# Use any default credentials provided after sample data setup
```

### Test API
Use Swagger UI available at `http://localhost:8000/docs`

## 📦 Deployment

### Backend (Gunicorn + Uvicorn)
```bash
pip install gunicorn
gunicorn -w 4 -k uvicorn.workers.UvicornWorker main:app
```

### Frontend (Build & Deploy)
```bash
npm run build
# Deploy dist/ folder to any static hosting
```

## 🤝 Contributing

Feel free to submit issues and enhancement requests!

## 📄 License

MIT License - feel free to use this project for learning and commercial purposes.

## 📞 Support

For issues and questions, please create an issue in the repository.

---

**Happy Coding! 🚀**
