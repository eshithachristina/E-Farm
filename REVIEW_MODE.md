# App Review Mode - Authentication Disabled

## Current Status
Authentication has been **temporarily disabled** to allow reviewing the app's internal structure.

## What's Changed

1. **No Login Required**: The app now starts directly at the home screen (tabs)
2. **Mock User**: A demo user is automatically created:
   - Name: "Demo User"
   - Role: "farmer"
   - Phone: "9876543210"
3. **API Calls Disabled**: API calls are commented out to prevent errors
4. **Direct Navigation**: You can navigate through all screens without authentication

## Screens You Can Review

- ✅ **Home Screen** - Categories, featured equipment
- ✅ **Equipment List** - Browse and search equipment
- ✅ **Equipment Details** - View equipment information
- ✅ **Bookings** - View booking management
- ✅ **Profile** - User profile and settings
- ✅ **Add Equipment** - Equipment listing form (for suppliers)
- ✅ **New Booking** - Booking creation form
- ✅ **Payment** - Payment screen
- ✅ **Reviews** - Review submission
- ✅ **Admin Panel** - Admin dashboard (if role is admin)

## To Re-enable Authentication

1. **In `efarm/app/(tabs)/index.tsx`**:
   - Uncomment the auth check in `useEffect`

2. **In `efarm/contexts/AuthContext.tsx`**:
   - Remove the mock user creation in `loadUser()`

3. **In `efarm/app/_layout.tsx`**:
   - Remove `initialRouteName="(tabs)"` from Stack

4. **In `efarm/app/(tabs)/bookings.tsx`**:
   - Uncomment the auth check and API call

5. **In `efarm/app/(tabs)/equipment.tsx`**:
   - Uncomment the API call

6. **In `efarm/app/(tabs)/index.tsx`**:
   - Uncomment the API call in `loadEquipment()`

## Testing Different User Roles

To test as different roles, you can modify the mock user in `AuthContext.tsx`:

```typescript
// For Farmer
role: 'farmer'

// For Supplier
role: 'supplier'

// For Admin
role: 'admin'
```

## Note
This is a temporary setup for app review. Remember to re-enable authentication before production deployment.

