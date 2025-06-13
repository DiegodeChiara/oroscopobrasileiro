# Universo Místico - Complete Astrology Platform

A comprehensive full-stack astrology and spiritual guidance platform combining Western astrological practices with rich Afro-Brazilian cultural elements, featuring both web and mobile applications with advanced geolocation and notification capabilities.

## 🌟 Platform Overview

### Complete Ecosystem
- **Web Application**: React-based responsive web platform
- **Mobile Application**: React Native cross-platform mobile app  
- **Backend API**: Express.js with PostgreSQL database
- **Geolocation Services**: Location-based spiritual content delivery
- **Push Notifications**: Intelligent notification system for mobile users

### Key Features Implemented
- **Spiritual Profile System**: Complete zodiac calculation and Orixá selection
- **Daily Horoscope**: Personalized astrological predictions
- **Interactive Tarot Readings**: Multiple reading types with card animations
- **Location-Based Services**: Nearby spiritual venues and celestial events
- **Cross-Platform Synchronization**: Seamless data sharing between web and mobile

## 🏗 Technical Architecture

### Frontend Technologies
- **Web**: React 18 with TypeScript, Vite build system
- **Mobile**: React Native with Expo, TypeScript
- **UI Framework**: Tailwind CSS (web) + React Native Paper (mobile)
- **State Management**: React Context API with custom hooks
- **Navigation**: Wouter (web) + React Navigation (mobile)

### Backend Infrastructure
- **API Server**: Express.js with TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **Authentication**: JWT-based auth with bcrypt password hashing
- **Data Validation**: Zod schemas for type-safe API endpoints
- **Session Management**: Express sessions with PostgreSQL store

### Mobile-Specific Services
- **Geolocation**: Expo Location for GPS and location tracking
- **Push Notifications**: Expo Notifications with scheduled alerts
- **Local Storage**: AsyncStorage for offline data persistence
- **Maps Integration**: React Native Maps with spiritual venue markers

## 📱 Application Features

### Web Platform Features
- **Responsive Design**: Mobile-first design with desktop optimization
- **Spiritual Profile Management**: Zodiac and Orixá configuration
- **Daily Horoscope**: Personalized predictions with cultural elements
- **Tarot Card Readings**: Interactive card selection and interpretation
- **Premium Features**: Advanced consultations and content

### Mobile App Enhancements
- **Real-Time Location**: GPS-based personalized content
- **Interactive Maps**: Spiritual venues with distance calculations
- **Push Notifications**: Daily reminders and celestial event alerts
- **Offline Capability**: Local data storage for core features
- **Native Animations**: Smooth card flips and spiritual transitions

### Shared Backend Services
- **User Authentication**: Secure login across platforms
- **Profile Synchronization**: Real-time data sync between web and mobile
- **Content Management**: Centralized horoscope and tarot data
- **Analytics Integration**: User interaction tracking

## 🔮 Spiritual Content Integration

### Astrological Systems
- **Western Astrology**: Complete zodiac sign calculations
- **Afro-Brazilian Traditions**: Orixá selection and spiritual guidance
- **Cultural Authenticity**: Respectful integration of Brazilian spiritual practices
- **Personalization**: User-specific content based on birth data and preferences

### Content Types
- **Daily Horoscopes**: Zodiac-based predictions with Orixá influences
- **Tarot Readings**: Multiple spread types with cultural interpretations
- **Spiritual Messages**: Daily guidance from selected Orixá protectors
- **Celestial Events**: Moon phases, eclipses, and astrological transits

## 🌍 Geolocation Features

### Location-Based Services
- **Spiritual Venue Discovery**: Nearby temples, centers, and esoteric stores
- **Celestial Event Calculations**: Location-specific astronomical events
- **Regional Content**: Localized spiritual practices and traditions
- **Distance-Based Filtering**: Customizable search radius for venues

### Map Integration
- **Interactive Venue Map**: Detailed information about spiritual locations
- **Directions Integration**: Navigation to selected venues
- **Visit Reminders**: Scheduled notifications for planned visits
- **Review System**: Community ratings for spiritual venues

## 🔔 Notification System

### Smart Notifications
- **Daily Horoscope Alerts**: Morning astrological guidance (8:00 AM)
- **Evening Spiritual Messages**: Orixá-based evening wisdom (8:00 PM)
- **Celestial Event Notifications**: Real-time alerts for astronomical events
- **Personalized Reminders**: Custom spiritual practice reminders

### Notification Types
- **Scheduled**: Regular daily content delivery
- **Event-Based**: Triggered by celestial occurrences
- **Location-Based**: Proximity alerts for spiritual venues
- **Interactive**: Actionable notifications with deep linking

## 💾 Data Architecture

### Database Schema
```sql
-- Users with spiritual profile data
users (id, email, name, birth_date, birth_time, birth_location, zodiac_sign, custom_orixa)

-- Daily horoscope content
horoscopes (id, zodiac_sign, content, orixa_influence, love_rating, work_rating, health_rating, date)

-- Tarot card database
tarot_cards (id, name, suit, meaning, description, image_url)
tarot_readings (id, user_id, cards, interpretation, reading_type, created_at)

-- Orixá information
orixas (id, name, description, attributes, colors, offerings, zodiac_associations)

-- User subscriptions and premium features
subscriptions (id, user_id, plan_type, status, created_at, expires_at)

-- User interaction tracking
user_interactions (id, user_id, action_type, details, timestamp)
```

### API Endpoints
```typescript
// Authentication
POST /api/auth/register - User registration
POST /api/auth/login - User authentication
GET /api/auth/me - Current user profile
PATCH /api/auth/profile - Update user profile

// Spiritual Content
GET /api/horoscope/daily/:sign - Daily horoscope by sign
GET /api/horoscope/user - User's personalized horoscope
GET /api/tarot/cards - Available tarot cards
POST /api/tarot/reading - Create new tarot reading
GET /api/orixas - List all Orixás
GET /api/orixas/:name - Specific Orixá information

// Premium Features
GET /api/subscription/user - User subscription status
POST /api/subscription/create - Create new subscription
```

## 🔧 Development Setup

### Prerequisites
- Node.js 18+ with npm
- PostgreSQL 14+
- Expo CLI (for mobile development)
- Git for version control

### Quick Start
```bash
# Clone repository
git clone <repository-url>
cd universo-mistico

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Configure DATABASE_URL and other secrets

# Initialize database
npm run db:push

# Start development servers
npm run dev  # Web and API
cd mobile-app && expo start  # Mobile app
```

### Environment Configuration
```env
# Database
DATABASE_URL=postgresql://user:password@localhost:5432/universo_mistico

# Authentication
JWT_SECRET=your-secret-key
SESSION_SECRET=your-session-secret

# Firebase (for web auth)
VITE_FIREBASE_API_KEY=your-firebase-api-key
VITE_FIREBASE_PROJECT_ID=your-project-id
VITE_FIREBASE_APP_ID=your-app-id

# Mobile notifications
EXPO_PROJECT_ID=your-expo-project-id
```

## 🚀 Deployment

### Web Platform
- **Production Build**: Vite optimized build with asset optimization
- **Server Deployment**: Express.js on Node.js runtime
- **Database**: PostgreSQL with connection pooling
- **CDN Integration**: Static asset delivery optimization

### Mobile Application
- **Expo Build Service**: EAS Build for iOS and Android
- **App Store Deployment**: Ready for iOS App Store and Google Play
- **OTA Updates**: Expo Updates for instant feature deployments
- **Push Notification**: Firebase Cloud Messaging integration

## 📊 Analytics & Monitoring

### User Analytics
- **Feature Usage**: Tracking of horoscope views, tarot readings, and spiritual profile interactions
- **Engagement Metrics**: Session duration, return frequency, and content preferences
- **Location Analytics**: Popular spiritual venues and regional usage patterns
- **Notification Performance**: Open rates and engagement with push notifications

### Technical Monitoring
- **API Performance**: Response times and error rates
- **Database Metrics**: Query performance and connection health
- **Mobile App Crashes**: Automatic crash reporting and performance monitoring
- **Geolocation Accuracy**: Location service reliability and precision

## 🔐 Security & Privacy

### Data Protection
- **Password Security**: bcrypt hashing with salt rounds
- **API Authentication**: JWT tokens with secure expiration
- **Database Security**: Prepared statements preventing SQL injection
- **Location Privacy**: User-controlled location sharing with opt-out options

### Privacy Compliance
- **Data Minimization**: Collection of only essential user information
- **User Consent**: Clear opt-in for location and notification services
- **Data Retention**: Automatic cleanup of old interaction data
- **Export/Delete**: User rights to data portability and deletion

## 🎯 Future Roadmap

### Enhanced Features
- **Voice Interactions**: Audio horoscope readings and guided meditations
- **Astral Chart Visualization**: Complete birth chart calculations and interpretations
- **Social Features**: Spiritual community forums and shared experiences
- **Machine Learning**: Personalized content recommendations based on usage patterns

### Technical Improvements
- **Real-Time Sync**: WebSocket connections for instant cross-platform updates
- **Offline Mode**: Complete offline functionality for core features
- **Performance Optimization**: Advanced caching and lazy loading
- **Accessibility**: WCAG 2.1 AA compliance across all platforms

### Market Expansion
- **Internationalization**: Support for Spanish and English markets
- **Regional Customization**: Adaptation for different spiritual traditions
- **Premium Tiers**: Advanced features and personal consultations
- **Partner Integration**: Collaboration with spiritual centers and practitioners

## 📈 Business Value

### Target Audience
- **Primary**: Brazilian users interested in astrology and spirituality (18-45 years)
- **Secondary**: International users exploring Afro-Brazilian spiritual traditions
- **Premium**: Users seeking personalized spiritual guidance and advanced features

### Revenue Models
- **Freemium**: Basic features free with premium subscriptions
- **Location Services**: Partnerships with spiritual venues and events
- **Content Licensing**: White-label spiritual content for other platforms
- **Consultation Services**: Connection to verified spiritual advisors

---

*Universo Místico represents a complete digital transformation of traditional spiritual practices, bringing authentic astrological and cultural wisdom to modern users through cutting-edge technology and respectful cultural integration.*