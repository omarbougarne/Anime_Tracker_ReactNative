## 📱 Mobile Application

This project has a companion mobile application built with React Native/Expo.

- **Repository**: [Anime Tracker Mobile](https://github.com/omarbougarne/anime-tracker-mobile)
- **Tech Stack**: React Native, Expo, Redux, TypeScript
- **Features**: Authentication, anime browsing, watchlist management

The mobile app connects to the same API endpoints as the web client.

📱 Features
User authentication (login/register)
Browse and search anime series
Track watching progress
Add series to personal list
User profile management
🛠️ Tech Stack
Framework: React Native with Expo
State Management: Redux with Redux Toolkit
API Client: Axios
Navigation: React Navigation (Stack & Tab)
Storage: AsyncStorage for token persistence
Styling: React Native StyleSheet
Authentication: JWT token-based auth
Package Manager: pnpm
🚀 Getting Started
Prerequisites
Node.js (v16+)
pnpm
Expo CLI
Android Studio/Xcode (for emulators)
Backend API running (see main project README)

```
# Clone the repository (if not already done)
git clone https://github.com/yourusername/anime-tracker-mobile.git
cd anime-tracker-mobile

# Install dependencies
pnpm install

# Create and configure .env file
echo "API_URL=http://your-backend-url:3000" > .env

# Start the development server
pnpm start
```

🔑 Authentication Flow
User registers or logs in through the auth screens
App stores JWT token in AsyncStorage
Subsequent API requests include the token in Authorization header
Protected routes check for valid authentication
Auto-login on app start if valid token exists
📱 Navigation Structure
Auth Stack: Login and Register screens
Main Tab Navigator:
Home Tab: Latest anime and recommendations
Search Tab: Find anime by title, genre, etc.
My List Tab: User's tracked anime
Profile Tab: User information and settings
💾 State Management
Redux Toolkit is used for state management with the following slices:

auth: Authentication state, user info
anime: Anime listing and details
myList: User's tracked anime list

🔄 API Integration
The app connects to the NestJS backend API with standardized response handling:

```
// Response format from API
interface ApiResponse<T> {
  success: boolean;
  data?: T | null;
  error?: string;
  message: string;
}
```

🧪 Testing
```
# Run tests
pnpm test
```
📦 Building for Production
```
# Build for Android
pnpm build:android

# Build for iOS
pnpm build:ios
```

🔗 Connecting to Backend
By default, the app connects to the backend API specified in your .env file. Make sure your backend is running and accessible from your device/emulator.

👤 Author
Omar Bougarne - [My Profile](https://github.com/omarbougarne)