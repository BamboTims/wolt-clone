# React Native Wolt Clone

A feature-rich React Native clone of the Wolt food delivery app, showcasing modern mobile development practices with React Native, Expo, and TypeScript.

## Features

- **User Authentication**: Apple and Google sign-in integration
- **Restaurant Discovery**: Browse restaurants and stores with beautiful UI
- **Search & Filter**: Find exactly what you're looking for with advanced filters
- **Interactive Map**: Explore restaurants and delivery zones on an interactive map
- **Menu Navigation**: Browse detailed menus with categories and items
- **Shopping Cart**: Add items, manage quantities, and see real-time totals
- **Checkout Flow**: Complete order flow with delivery scheduling
- **Location Selection**: Choose delivery locations with address management
- **Smooth Animations**: Fluid transitions and gestures powered by Reanimated
- **Tab Navigation**: Bottom tabs for easy navigation between sections

## Tech Stack

- [Expo Router](https://docs.expo.dev/routing/introduction/) - File-based routing and navigation
- [React Native Reanimated](https://docs.swmansion.com/react-native-reanimated/) - Smooth animations and transitions
- [React Native Gesture Handler](https://docs.swmansion.com/react-native-gesture-handler/) - Touch interactions
- [Expo Maps](https://docs.expo.dev/versions/latest/sdk/maps/) - Interactive maps integration
- [Expo Linear Gradient](https://docs.expo.dev/versions/latest/sdk/linear-gradient/) - Beautiful gradient effects
- [Zustand](https://zustand-demo.pmnd.rs/) - State management for cart and user data
- [MMKV](https://github.com/mrousavy/react-native-mmkv/tree/main) - The fastest key/value storage for React Native
- [Sentry](https://dub.sh/trysentry) - Error tracking and performance monitoring

## Getting Started

### Prerequisites

Make sure you have the [Expo CLI](https://docs.expo.dev/get-started/set-up-your-environment/) installed.

For the best development experience, install:

- [Android Studio](https://developer.android.com/studio) for Android development
- [Xcode](https://developer.apple.com/xcode/) (Mac only) for iOS development

### Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd wolt
   ```

2. **Install dependencies**

   ```bash
   bun install
   # or npm install
   ```

3. **Prebuild the native code**

   ```bash
   bunx expo prebuild
   ```

4. **Run the app**

   ```bash
   # iOS
   bunx expo run:ios

   # Android
   bunx expo run:android
   ```

### Sentry Setup

1. Create a project on [Sentry](https://sentry.io/)
2. Run the setup wizard:

   ```bash
   bunx @sentry/wizard@latest -s -i reactNative
   ```

3. Follow the prompts to configure Sentry for your project

## Project Structure

```
app/
├── (app)/
│   ├── (public)/          # Public routes (authentication)
│   └── (auth)/            # Protected routes
│       ├── (tabs)/        # Bottom tab navigation
│       │   ├── restaurants/  # Restaurant browsing
│       │   ├── stores/       # Store browsing
│       │   ├── search/       # Search functionality
│       │   ├── discovery/    # Discovery feed
│       │   └── profile/      # User profile
│       ├── (modal)/       # Modal screens
│       │   ├── location/     # Location picker
│       │   ├── filter/       # Filter options
│       │   ├── map/          # Map view
│       │   └── [id]/         # Restaurant/menu details
│       └── order/         # Order flow
│           ├── index/        # Cart view
│           ├── schedule/     # Delivery scheduling
│           └── checkout/     # Checkout
components/              # Reusable components
constants/              # Theme, colors, fonts
assets/                 # Images and static files
```

## Features Breakdown

### Authentication Flow

- Beautiful animated welcome screen with infinite scroll
- Apple and Google OAuth integration
- Alternative login options

### Discovery & Browse

- Categorized restaurant and store listings
- Horizontal scrolling sections
- Restaurant cards with ratings and delivery info
- Filter by cuisine, price range, and dietary preferences

### Restaurant & Menu

- Detailed restaurant information
- Menu organized by categories
- Item customization options
- Add to cart with quantity selection

### Cart & Checkout

- Persistent cart state with Zustand
- Item quantity management
- Real-time price calculations
- Delivery scheduling options
- Order summary and confirmation

### Additional Features

- Location-based restaurant discovery
- Interactive map with restaurant markers
- Search with autocomplete
- User profile management
- Smooth page transitions and animations
