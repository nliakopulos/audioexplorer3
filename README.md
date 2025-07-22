# AudioExplorer

A modern, accessible web application for AudioExplorer - an AI-powered travel companion that transforms journeys into meaningful, screen-free experiences through immersive audio storytelling.

## 🚀 Features

### Core Functionality
- **Full-Stack Application**: Complete React frontend with Supabase backend integration
- **User Authentication**: Email and SMS registration/login with verification
- **Interactive Dashboard**: Multi-tab interface with personalized content
- **Audio Player**: Built-in audio playback for storytelling content
- **GPS Location Detection**: Real-time location tracking with nearby POI discovery
- **Responsive Design**: Fully responsive layout optimized for all devices
- **Accessibility**: WCAG compliant with comprehensive keyboard and screen reader support

### Landing Page Sections
- **Hero Section**: Compelling value proposition with professional iPhone mockup
- **Features**: Four key capabilities with visual icons and descriptions
- **How It Works**: Step-by-step process explanation with numbered workflow
- **User Reviews**: Testimonials with star ratings and user photos
- **Mobile App Preview**: Realistic iPhone mockup showing bottom navigation
- **FAQ Section**: Expandable accordion with common questions
- **Download CTA**: App store links and call-to-action

### Dashboard Features
- **Bottom Navigation**: 4-tab interface (Home, Saved, Profile, Help)
- **Story Browser**: Browse and play audio stories by category
- **Interest Management**: Personalized content based on user preferences
- **Profile Management**: Account settings and user information
- **Bookmark System**: Save favorite stories for later listening
- **Help & Support**: FAQ and support resources
- **GPS Location Tracking**: Real-time location detection with movement monitoring
- **POI Discovery**: Automatic detection of nearby points of interest (500m radius)
- **Distance Calculation**: Precise distance measurements in meters/kilometers
- **Location Testing**: Manual location testing with specific coordinates

### Technical Features
- **Real-time Authentication**: Supabase Auth integration with email/SMS verification
- **Form Validation**: Comprehensive client-side validation with error handling
- **Progressive Web App**: PWA-ready with service worker capabilities
- **Performance Optimized**: Fast loading with code splitting and lazy loading
- **Smooth Scrolling**: Section navigation with smooth scroll behavior
- **Touch-Friendly**: Mobile-optimized with proper touch targets
- **Geolocation API**: Browser-based GPS tracking with high accuracy
- **Overpass API Integration**: OpenStreetMap POI data with Wikipedia/Wikidata links
- **Movement Detection**: Automatic POI refresh on 50m movement threshold
- **Distance Algorithms**: Optimized distance calculation for local areas

## 🛠️ Technology Stack

### Frontend
- **React 18** with TypeScript for type-safe development
- **Vite** for fast development and optimized builds
- **Tailwind CSS** for utility-first styling
- **Lucide React** for consistent iconography

### Backend & Database
- **Supabase** for authentication, database, and real-time features
- **PostgreSQL** database with custom schema for users and content
- **Row Level Security (RLS)** for secure data access

### Development Tools
- **ESLint** for code quality and consistency
- **PostCSS** for advanced CSS processing
- **TypeScript** for enhanced developer experience

## 📦 Installation & Setup

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Supabase account for backend services

### Getting Started

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd PE-AudioExplorer-lutz-dev
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   Create a `.env.local` file with your Supabase credentials:
   ```env
   VITE_SUPABASE_URL=your_supabase_url
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
   ```

4. **Database Setup**
   Run the migration scripts in the `supabase/migrations/` directory to set up your database schema.

5. **Start the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   Navigate to `http://localhost:3000`

### Available Scripts

- `npm run dev` - Start development server on port 3000
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint for code quality

## 📱 Mobile Preview

You can test the AudioExplorer app experience:

1. **Development**: Visit `http://localhost:3000` on your mobile device
2. **Responsive Testing**: Use browser dev tools to simulate different screen sizes
3. **Touch Testing**: Verify all interactive elements work with touch gestures
4. **GPS Testing**: Test location detection and POI discovery on real devices

## 🗺️ GPS Location Features

### Real-Time Location Tracking
- **Continuous GPS Monitoring**: Tracks user location with high accuracy
- **Movement Detection**: Automatically refreshes POIs when user moves 50m+
- **Accuracy Display**: Shows GPS accuracy in meters
- **Manual Controls**: Start/stop GPS tracking and manual POI refresh

### Points of Interest Discovery
- **500m Search Radius**: Finds POIs within 500 meters of current location
- **Multiple Categories**: Tourism, historic, amenity, leisure, and shop locations
- **Exact Distance Calculation**: Precise distance measurements in meters/kilometers
- **Smart Sorting**: POIs sorted by distance (closest first)
- **Duplicate Prevention**: Removes duplicate POIs automatically

### Information Links
- **Wikipedia Integration**: Direct links to Wikipedia articles when available
- **Wikidata Fallback**: Links to Wikidata pages for additional information
- **OpenStreetMap Links**: Map links for all POIs with exact coordinates
- **Smart Button Labels**: "Wiki" for Wikipedia, "Info" for Wikidata, "Map" for OSM

### Testing & Development
- **Location Testing**: Test button for specific coordinates (e.g., Rohsiepe area)
- **Debug Logging**: Console output for POI data and distance calculations
- **Error Handling**: Graceful fallbacks for GPS errors and API failures
- **Privacy Compliance**: GDPR-compliant location data handling

The app includes a realistic iPhone mockup showcasing:
- Dynamic Island and status bar
- "Now Playing" audio interface
- Album art and playback controls
- Bottom navigation with 4 tabs
- Professional mobile app appearance

## 🎨 Design System

### Color Palette
- **Primary**: Slate tones (`slate-600`, `slate-700`) for professional appearance
- **Accent**: Blue (`blue-600`) for active states and CTAs
- **Background**: Gray shades for subtle contrast
- **Text**: High contrast for optimal readability

### Typography
- **Headings**: Bold hierarchy with responsive sizing
- **Body Text**: Optimized for readability across devices
- **Interactive Elements**: Clear labels and descriptions

### Component Library
- **Buttons**: Consistent styling with hover/focus states
- **Forms**: Validated inputs with real-time feedback
- **Navigation**: Responsive with smooth transitions
- **Cards**: Modern design with subtle shadows
- **Modals**: Accessible overlays with proper focus management

## 🏗️ Architecture

### Component Structure
```
src/components/
├── Auth/                   # Authentication components
│   ├── AuthModal.tsx       # Main auth modal container
│   ├── LoginForm.tsx       # Login form with validation
│   ├── RegisterForm.tsx    # Registration form
│   ├── EmailRegistrationForm.tsx
│   ├── SMSRegistrationForm.tsx
│   ├── EmailVerification.tsx
│   ├── SMSVerification.tsx
│   └── OnboardingFlow.tsx  # User onboarding experience
├── UI/                     # Reusable UI components
│   ├── Button.tsx          # Standardized button component
│   ├── FormField.tsx       # Input field wrapper
│   ├── SimpleModal.tsx     # Modal container
│   ├── Stepper.tsx         # Multi-step indicator
│   └── OptimizedImage.tsx  # Performance-optimized images
├── Dashboard/              # Dashboard-specific components
│   ├── Navbar.tsx          # Top navigation bar
│   ├── InterestSelector.tsx # User preference management
│   ├── StorySelector.tsx   # Content browsing
│   ├── ProfileForm.tsx     # User profile editing
│   └── AudioPlayer.tsx     # Audio playback controls
├── Location/               # GPS and location components
│   └── GPSLocationDetector.tsx # Real-time GPS tracking and POI discovery
└── Utils/                  # Utility components
    ├── AuthDebugger.tsx    # Development debugging tools
    ├── TestButton.tsx      # Testing utilities
    └── various other debug components
```

### State Management
- **AuthContext**: Global authentication state
- **Local State**: Component-level state with React hooks
- **Supabase Realtime**: Live data synchronization

### Database Schema
```sql
-- Users table with authentication
users (
  id UUID PRIMARY KEY,
  email TEXT,
  phone TEXT,
  created_at TIMESTAMP,
  interests TEXT[]
)

-- Additional tables for stories, bookmarks, etc.
```

## ♿ Accessibility Features

### WCAG 2.1 AA Compliance
- **Keyboard Navigation**: Full keyboard accessibility with logical tab order
- **Screen Reader Support**: Comprehensive ARIA labels and semantic HTML
- **Color Contrast**: Minimum 4.5:1 contrast ratio throughout
- **Focus Management**: Clear visual indicators and proper focus flow
- **Alternative Text**: Descriptive alt text for all images and graphics

### Interactive Elements
- **Skip Links**: "Skip to main content" for keyboard users
- **Form Accessibility**: Proper labels, validation, and error messaging
- **Modal Management**: Proper focus trapping and escape handling
- **Touch Targets**: Minimum 44px for all interactive elements

## 📱 Responsive Design

### Breakpoint Strategy
- **Mobile First**: Base styles for 320px+ devices
- **Tablet**: 768px+ with adapted layouts
- **Desktop**: 1024px+ with full feature set
- **Large Desktop**: 1440px+ with optimized spacing

### Mobile Optimizations
- **Bottom Navigation**: Easy thumb navigation on mobile
- **Swipe Gestures**: Natural mobile interaction patterns
- **Touch-Friendly**: Properly sized interactive elements
- **Performance**: Optimized for mobile network conditions

## 🔧 Project Structure

```
PE-AudioExplorer-lutz-dev/
├── public/                 # Static assets
│   ├── audio/             # Demo audio files
│   ├── AudioExplorer Logo_Color-3 - compatible with website + only 1 tagline.png
│   ├── AudioExplorer_QR.png
│   ├── explore.jpg        # Landing page images
│   ├── player.jpg
│   ├── profile.jpg
│   └── expo_go_barcode_for_mobile_preview.PNG
├── src/
│   ├── components/        # All React components (30+ files)
│   ├── contexts/         # React context providers
│   │   └── AuthContext.tsx
│   ├── hooks/            # Custom React hooks
│   │   ├── useAuth.ts
│   │   └── usePerformance.ts
│   ├── lib/              # External service integrations
│   │   └── supabase.ts
│   ├── types/            # TypeScript type definitions
│   │   └── supabase.ts
│   ├── utils/            # Utility functions
│   │   └── validation.ts
│   ├── data/             # Static data and configurations
│   │   └── demoStories.ts
│   ├── App.tsx           # Main application component
│   ├── main.tsx          # Application entry point
│   └── index.css         # Global styles and Tailwind imports
├── supabase/             # Database migrations and config
│   └── migrations/       # SQL migration files
├── scripts/              # Development and build scripts
├── package.json          # Dependencies and scripts
├── tailwind.config.js    # Tailwind CSS configuration
├── vite.config.ts        # Vite build configuration
├── tsconfig.json         # TypeScript configuration
└── README.md             # Project documentation
```

## 🧪 Testing

### Manual Testing Checklist
- [ ] **Authentication Flow**: Registration, login, email/SMS verification
- [ ] **Dashboard Navigation**: All 4 tabs function correctly
- [ ] **Audio Playback**: Stories play without issues
- [ ] **GPS Location Detection**: Location tracking and POI discovery
- [ ] **Distance Calculations**: Accurate distance measurements
- [ ] **POI Links**: Wikipedia/Wikidata/OpenStreetMap links work
- [ ] **Responsive Design**: All breakpoints work properly
- [ ] **Keyboard Navigation**: Full keyboard accessibility
- [ ] **Form Validation**: All forms validate correctly
- [ ] **Error Handling**: Proper error states and messaging
- [ ] **Performance**: Fast loading and smooth interactions

### Browser Compatibility
- Chrome (latest) ✅
- Firefox (latest) ✅
- Safari (latest) ✅
- Edge (latest) ✅
- Mobile browsers (iOS Safari, Chrome Mobile) ✅

## 🚀 Deployment

### Production Build
```bash
npm run build
```

### Environment Variables
Ensure production environment has:
- `VITE_SUPABASE_URL`
- `VITE_SUPABASE_ANON_KEY`

### Hosting Recommendations
- **Vercel**: Optimized for React/Vite applications
- **Netlify**: Great for static sites with form handling
- **Supabase Hosting**: Integrated with backend services

## 🔒 Security

### Data Protection
- **Row Level Security**: Database-level access controls
- **Input Validation**: Client and server-side validation
- **Authentication**: Secure token-based auth with Supabase
- **HTTPS**: All production traffic encrypted

### Privacy Compliance
- **GDPR Ready**: User data handling compliant
- **Data Minimization**: Only collect necessary information
- **User Control**: Clear privacy settings and data management

## 📈 Performance

### Optimization Features
- **Code Splitting**: Lazy loading for better initial load times
- **Image Optimization**: Responsive images with proper sizing
- **Caching**: Browser caching for static assets
- **Bundle Size**: Optimized build with tree shaking

### Performance Metrics
- **First Contentful Paint**: < 1.5s
- **Largest Contentful Paint**: < 2.5s
- **Cumulative Layout Shift**: < 0.1
- **First Input Delay**: < 100ms

## 📄 License

This project is proprietary software. All rights reserved.

## 🤝 Contributing

This is a private project. For questions or issues, please contact the development team.

---

**AudioExplorer** - Transforming journeys through immersive audio storytelling.

*Built with modern web technologies for exceptional user experience across all devices.*
