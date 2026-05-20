
# 🚌 BusTicket Pro - Bus Ticketing System

A comprehensive, fully-functional bus ticketing system built with HTML, CSS, and JavaScript. Users can register, login, search for buses, select seats, make payments, and manage their bookings.

## 🌟 Features

### User Authentication
- **User Registration**: New users can create accounts with email verification
- **Secure Login**: Users can login with registered credentials
- **Session Management**: Persistent login using localStorage

### Dashboard
- **Welcome Dashboard**: Displays user statistics and quick actions
- **Booking Statistics**: Shows total bookings, completed trips, and upcoming trips
- **Quick Access**: Easy navigation to booking and ticket viewing

### Bus Search & Selection
- **Advanced Search**: Filter buses by departure city, destination, and travel date
- **Bus Details**: View bus information including:
  - Bus name and type
  - Departure and arrival times
  - Travel duration
  - Available seats
  - Ratings
  - Price per seat

### Seat Selection
- **Visual Seat Layout**: Interactive bus layout with 40 seats arranged in a grid
- **Real-time Updates**: Dynamically shows available and booked seats
- **Seat Status**:
  - Green: Available seats
  - Blue: Selected seats
  - Red/Pink: Already booked seats
- **Seat Legend**: Visual guide for seat status

### Payment Processing
- **Booking Summary**: Review all booking details before payment
- **Secure Payment Form**:
  - Cardholder name
  - Card number (with formatting)
  - Expiry date (MM/YY format)
  - CVV security code
- **Input Validation**: Ensures all required fields are filled
- **Formatted Input**: Automatic formatting for card details

### Ticket Management
- **View All Tickets**: See all booked tickets with status
- **Ticket Details**:
  - Ticket ID
  - Bus name
  - Route information
  - Travel date
  - Selected seats
  - Total amount
  - Booking status (Completed/Upcoming)
- **Ticket Actions**: Download and view detailed information

### Responsive Design
- **Mobile-Friendly**: Fully responsive design works on all devices
- **Adaptive Layout**: Optimized for desktop, tablet, and mobile screens
- **Touch-Friendly**: Easy-to-use interface for touch devices

## 🎨 Technology Stack

- **HTML5**: Semantic markup and structure
- **CSS3**: Modern styling with flexbox and grid
- **JavaScript (Vanilla)**: No dependencies, pure JavaScript functionality
- **LocalStorage**: Client-side data persistence

## 📁 File Structure

```
bus-ticketing-system/
├── index.html          # Main HTML file with all page structures
├── style.css           # Complete styling with responsive design
├── script.js           # JavaScript functionality and logic
└── README.md           # Documentation
```

## 🚀 Getting Started

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Superdanger6/hardy.git
cd hardy
```

2. Open the application:
```bash
# Option 1: Open index.html directly in your browser
open index.html

# Option 2: Use a local server
python -m http.server 8000
# or
npx http-server
```

3. Access the application at `http://localhost:8000`

## 💻 Usage Guide

### Registration
1. On the registration page, fill in your details:
   - Full Name
   - Email Address
   - Phone Number
   - Password (must match confirmation)
2. Click "Register"
3. After successful registration, you'll be prompted to login

### Login
1. Enter your registered email and password
2. Click "Login"
3. You'll be redirected to your dashboard

### Booking a Ticket
1. Click "Book Ticket" from the dashboard
2. Select departure city, destination, and travel date
3. Click "Search Buses"
4. Choose a bus from the results
5. Select your preferred seats (green available seats)
6. Click "Proceed to Payment"
7. Enter your card details
8. Click "Complete Payment"
9. Receive confirmation with your ticket ID

### Managing Tickets
1. Click "My Tickets" to view all your bookings
2. View ticket details or download your ticket
3. See upcoming and completed trips

## 📊 Data Structure

### User Object
```javascript
{
  id: number,
  fullname: string,
  email: string,
  phone: string,
  password: string
}
```

### Booking Object
```javascript
{
  id: string,
  userId: number,
  busId: string,
  busName: string,
  from: string,
  to: string,
  date: string,
  seats: array,
  totalAmount: number,
  bookingDate: string,
  status: string
}
```

## 🎯 Key Features Explained

### Seat Selection
- The bus layout shows 40 seats in a 6-column grid
- Booked seats cannot be selected
- Multiple seats can be selected at once
- Real-time price calculation based on selected seats

### Payment Processing
- Uses localStorage to simulate payment processing
- Card formatting for better user experience
- No actual payment processing (demonstration only)

### Data Persistence
- All user data stored in localStorage
- Bookings persist across sessions
- User session maintained after login

## 🔐 Security Notes

**Important**: This is a demonstration project. In a production environment:
- Use HTTPS for secure communication
- Never store passwords in plain text
- Implement server-side authentication
- Use secure payment gateways (Stripe, PayPal, etc.)
- Implement proper data validation and sanitization
- Add rate limiting and CSRF protection

## 📱 Responsive Breakpoints

- **Desktop**: 1024px and above
- **Tablet**: 768px to 1023px
- **Mobile**: Below 768px
- **Small Mobile**: Below 480px

## 🎨 Color Scheme

- **Primary**: #2563eb (Blue)
- **Secondary**: #f59e0b (Amber)
- **Success**: #10b981 (Green)
- **Danger**: #ef4444 (Red)
- **Dark**: #1f2937 (Dark Gray)
- **Light**: #f3f4f6 (Light Gray)

## 🧪 Test Credentials

You can test the application with these credentials after registration:

```
Email: test@example.com
Password: password123
```

Or simply create a new account with any email and password.

## 🐛 Known Limitations

- No actual payment processing
- Limited to 6 sample bus routes
- No real email notifications
- Data stored only in localStorage (lost on browser cache clear)
- No user profile editing

## 🔮 Future Enhancements

- [ ] Backend API integration
- [ ] Real payment gateway integration
- [ ] Email notifications
- [ ] Advanced filters (price range, bus type, rating)
- [ ] User profile management
- [ ] Cancellation and refund system
- [ ] Seat class upgrades
- [ ] Passenger details collection
- [ ] Promo code system
- [ ] Admin dashboard

## 📝 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

## 🎉 Enjoy Your Bus Ticketing Experience!

Thank you for using BusTicket Pro. Have a great trip! 🚌✨

---

**Note**: This is a frontend demonstration project. For production use, please integrate with a real backend server and payment gateway.
