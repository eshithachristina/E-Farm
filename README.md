# eFarm - Farming Equipment Rental App

A comprehensive mobile application for renting farming equipment, connecting farmers with equipment owners/suppliers.

## Features

### User Roles
- **Farmer (Customer)**: Search and rent farm equipment
- **Equipment Owner/Supplier**: List and manage equipment for rent
- **Admin**: Manage users, equipment, bookings, and platform settings

### Core Features

#### 1. User Registration & Authentication
- Registration using phone number, email, or social login
- OTP verification for mobile numbers
- Profile management (name, address, village, state, pincode)

#### 2. Equipment Browsing & Search
- Browse equipment by category (Tractors, Harvesters, Sprayers, etc.)
- Search by name, location, or availability dates
- Filter by price, brand, capacity, distance, delivery availability
- View detailed equipment information with images, pricing, and owner details

#### 3. Equipment Listing (Supplier Side)
- Upload equipment with images and descriptions
- Set rent rates (hourly/day/week based)
- Add location (GPS or manual)
- Manage availability calendar
- Add pickup/delivery instructions
- Edit, pause, or delete listings

#### 4. Booking & Rental Management
- Request bookings for selected dates/times
- Owner approval/rejection system
- Booking status tracking (Pending/Approved/Rejected/In-Use/Completed)
- Doorstep delivery option
- Rental period tracking and reminders

#### 5. Payments
- Multiple payment options: UPI, Wallet, Net Banking, Cash on Delivery
- Price breakdown: rental cost + delivery + service fee
- Payment receipt generation
- Refund rules for booking cancellations

#### 6. Ratings & Reviews
- Rate equipment and owner after rental
- Supplier can rate the renter (optional trust system)

#### 7. Notifications
- Push notifications for:
  - Booking requests
  - Approvals/Rejections
  - Payment reminders
  - Rental completion reminders

#### 8. Admin Panel
- View and manage users
- Manage equipment listings
- View booking data and payments
- Approve/review reported issues
- Analytics dashboard

### Additional Features (Optional)
- GPS-based nearby equipment finder
- In-app chat between Farmer and Owner
- KYC Verification for equipment owners
- Insurance option (damage protection add-on)
- Seasonal demand price adjustment

## Tech Stack

- **Framework**: React Native with Expo
- **Navigation**: Expo Router
- **State Management**: React Context API
- **Storage**: AsyncStorage & Expo SecureStore
- **API**: Axios
- **Forms**: React Hook Form
- **Validation**: Zod
- **Maps**: React Native Maps
- **Image Picker**: Expo Image Picker
- **Notifications**: Expo Notifications
- **Date Picker**: @react-native-community/datetimepicker

## Project Structure

```
efarm/
├── app/                    # App screens (Expo Router)
│   ├── (auth)/            # Authentication screens
│   ├── (tabs)/            # Main app tabs
│   └── _layout.tsx        # Root layout
├── components/            # Reusable components
├── contexts/              # React Context providers
├── services/              # API and service layer
├── types/                 # TypeScript type definitions
├── constants/             # App constants
└── hooks/                 # Custom React hooks
```

## Installation

1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm start
```

3. Run on your preferred platform:
```bash
npm run android  # For Android
npm run ios      # For iOS
npm run web      # For Web
```

## Environment Setup

Create a `.env` file in the root directory:
```
API_BASE_URL=http://localhost:3000/api
```

## API Integration

The app is designed to work with a backend API. Update the `API_BASE_URL` in `constants/index.ts` to point to your backend server.

Expected API endpoints:
- `/auth/*` - Authentication endpoints
- `/equipment/*` - Equipment management
- `/bookings/*` - Booking management
- `/payments/*` - Payment processing
- `/reviews/*` - Reviews and ratings
- `/notifications/*` - Notifications
- `/admin/*` - Admin panel endpoints

## Features Implementation Status

- ✅ Project structure setup
- ✅ Authentication system (Login, Register, OTP)
- ✅ Equipment browsing and search
- ✅ Equipment listing for suppliers
- ✅ Booking management
- ✅ Payment integration UI
- ✅ Reviews and ratings UI
- ✅ Admin panel UI
- ⏳ Backend API integration (requires backend server)
- ⏳ Push notifications setup
- ⏳ GPS location services
- ⏳ Chat functionality
- ⏳ KYC verification
- ⏳ Insurance features

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License.

## Support

For support, email support@efarm.com or open an issue in the repository.
