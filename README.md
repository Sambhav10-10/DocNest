# DocNest - Healthcare Appointment Booking System

A full-stack healthcare appointment booking application that connects patients with doctors seamlessly. DocNest provides an intuitive platform for booking appointments, managing health records, and streamlining healthcare access.

## 🌟 Features

### For Patients
- **Easy Registration & Login** - Quick account setup with email verification
- **Doctor Discovery** - Browse doctors by speciality with detailed profiles
- **Appointment Booking** - Real-time slot availability and easy scheduling
- **Online Payments** - Secure payment processing with Razorpay and Stripe
- **Profile Management** - Update personal information and health details
- **Appointment History** - Track all past and upcoming appointments
- **Cancellation** - Cancel appointments with instant refund processing

### For Doctors
- **Doctor Dashboard** - View all assigned appointments
- **Profile Management** - Manage availability and speciality details
- **Appointment Management** - Accept, complete, or cancel appointments
- **Earnings Tracking** - Monitor consultation earnings

### For Administrators
- **Admin Dashboard** - Comprehensive system overview
- **Doctor Management** - Add, edit, and manage doctor profiles
- **Appointment Overview** - Monitor all system appointments
- **Earnings Analytics** - Track platform revenue and doctor earnings
- **User Management** - Manage patient and doctor accounts

## 🏗️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication and authorization
- **Bcrypt** - Password hashing
- **Cloudinary** - Image storage and CDN
- **Razorpay** - Payment gateway (India)
- **Stripe** - Payment gateway (Global)
- **Multer** - File upload handling

### Frontend
- **React** - UI library
- **Vite** - Build tool
- **React Router** - Navigation
- **Axios** - HTTP client
- **Tailwind CSS** - Styling
- **React Toastify** - Notifications

### Admin Panel
- **React** - UI library
- **Vite** - Build tool
- **React Router** - Navigation
- **Tailwind CSS** - Styling
- **Axios** - HTTP client

## 📁 Project Structure

```
DocNest/
├── backend/                 # Node.js Express API
│   ├── config/             # Database & Cloudinary config
│   ├── controllers/        # Business logic
│   ├── middleware/         # Authentication & uploads
│   ├── models/             # MongoDB schemas
│   ├── routes/             # API endpoints
│   └── server.js           # Entry point
│
├── frontend/               # Patient React app
│   ├── src/
│   │   ├── assets/         # Images and icons
│   │   ├── components/     # Reusable components
│   │   ├── context/        # Global state management
│   │   ├── pages/          # Page components
│   │   └── App.jsx         # Main app component
│   └── package.json
│
├── admin/                  # Admin React app
│   ├── src/
│   │   ├── assets/         # Images and icons
│   │   ├── components/     # Dashboard components
│   │   ├── context/        # Global state management
│   │   └── pages/          # Admin pages
│   └── package.json
│
└── README.md              # This file
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- MongoDB account
- Cloudinary account
- Razorpay account (optional)
- Stripe account (optional)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/docnest.git
   cd docnest
   ```

2. **Setup Backend**
   ```bash
   cd backend
   npm install
   ```

3. **Setup Frontend**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Setup Admin Panel**
   ```bash
   cd ../admin
   npm install
   ```

### Environment Variables

Create a `.env` file in the `backend` directory:

```env
# MongoDB
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net

# JWT
JWT_SECRET=your_jwt_secret_key

# Cloudinary
CLOUDINARY_NAME=your_cloudinary_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

# Razorpay (Optional)
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

# Stripe (Optional)
STRIPE_SECRET_KEY=your_stripe_secret_key

# Frontend URLs
FRONTEND_URL=http://localhost:5173
ADMIN_URL=http://localhost:5174
```

Create a `.env.local` file in the `frontend` directory:

```env
VITE_BACKEND_URL=http://localhost:4000
```

Create a `.env.local` file in the `admin` directory:

```env
VITE_BACKEND_URL=http://localhost:4000
```

## 📱 Running the Application

### Start Backend Server
```bash
cd backend
npm run server
```
Backend runs on `http://localhost:4000`

### Start Frontend
```bash
cd frontend
npm run dev
```
Frontend runs on `http://localhost:5173`

### Start Admin Panel
```bash
cd admin
npm run dev
```
Admin panel runs on `http://localhost:5174`

## 🔐 Authentication

DocNest uses JWT (JSON Web Tokens) for secure authentication:

- **User Login** - Patients authenticate with email and password
- **Doctor Login** - Doctors authenticate with credentials
- **Admin Login** - Admins authenticate separately
- **Token Storage** - Tokens stored in localStorage for persistence

## 💳 Payment Integration

### Razorpay
- Integrated for Indian payments
- Supports multiple payment methods
- Instant payment verification

### Stripe
- Global payment processing
- Credit/debit card support
- Secure payment handling

## 📚 API Endpoints

### User Routes (`/api/user`)
- `POST /register` - User registration
- `POST /login` - User login
- `GET /get-profile` - Fetch user profile
- `POST /update-profile` - Update user information
- `POST /book-appointment` - Book an appointment
- `GET /appointments` - Get user appointments

### Doctor Routes (`/api/doctor`)
- `POST /login` - Doctor login
- `GET /appointments` - Get doctor appointments
- `POST /complete-appointment` - Mark appointment as complete
- `GET /profile` - Get doctor profile

### Admin Routes (`/api/admin`)
- `POST /login` - Admin login
- `POST /add-doctor` - Add new doctor
- `GET /all-doctors` - Get all doctors
- `GET /appointments` - Get all appointments
- `GET /dashboard-data` - Dashboard analytics

## 📝 Database Schema

### Collections
- **Users** - Patient information
- **Doctors** - Doctor profiles and availability
- **Appointments** - Booking records
- **Admins** - Administrator accounts

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Contact & Support

For support, email us at support@docnest.com or create an issue in the repository.

- **Email**: greatstackdev@gmail.com
- **Website**: [Your Website]
- **GitHub**: [Your GitHub Profile]

## 🎯 Future Enhancements

- [ ] Video consultation feature
- [ ] Prescription management
- [ ] Telemedicine capabilities
- [ ] Mobile app (React Native)
- [ ] AI-powered doctor recommendations
- [ ] Insurance integration
- [ ] Multi-language support
- [ ] Advanced analytics dashboard

## 📊 Performance

- Fast appointment booking with real-time updates
- Optimized database queries
- Image compression via Cloudinary
- Responsive design for all devices
- SEO-friendly frontend

---

**Built with ❤️ using React, Node.js, and MongoDB**

Made by [Sambhav Koshta]
