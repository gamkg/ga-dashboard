# GA Dashboard

A React application built with Vite and Firebase, designed for Google Analytics dashboard functionality.

## Project Overview

This project is a modern web application using React 19 with Vite as the build tool. It's configured to integrate with Firebase services for backend functionality and uses Chakra UI for the user interface.

## Tech Stack

- **React** 19.2.0 - UI library
- **Vite** 7.2.4 - Build tool and dev server
- **Firebase** 12.6.0 - Backend services (Authentication, Firestore, Storage, etc.)
- **Chakra UI** 3.30.0 - Component library
- **ESLint** 9.39.1 - Code linting

## Project Setup

### Prerequisites

- Node.js (v18 or higher recommended)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd software
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
   - Create a `.env` file in the root directory
   - Add your Firebase configuration:
```env
VITE_FIREBASE_API_KEY=your_api_key_here
VITE_FIREBASE_AUTH_DOMAIN=your_auth_domain_here
VITE_FIREBASE_PROJECT_ID=your_project_id_here
VITE_FIREBASE_STORAGE_BUCKET=your_storage_bucket_here
VITE_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id_here
VITE_FIREBASE_APP_ID=your_app_id_here
```

## Firebase Configuration

Firebase has been initialized and configured in `src/firebase.js`. The configuration uses environment variables to keep sensitive credentials secure.

### Current Firebase Setup

- Firebase app initialized and ready to use
- Configuration loaded from environment variables
- Ready to add Firebase services (Auth, Firestore, Storage, etc.)

### Adding Firebase Services

To use Firebase services in your components, import them from the Firebase SDK:

```javascript
import app from './firebase.js';
import { getAuth } from 'firebase/auth';
import { getFirestore } from 'firebase/firestore';
import { getStorage } from 'firebase/storage';

// Initialize services
const auth = getAuth(app);
const db = getFirestore(app);
const storage = getStorage(app);
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Project Structure

```
software/
├── public/           # Static assets
├── src/
│   ├── assets/      # Images and other assets
│   ├── App.jsx      # Main App component
│   ├── App.css      # App styles
│   ├── firebase.js  # Firebase configuration
│   ├── index.css    # Global styles
│   └── main.jsx     # Application entry point
├── .env             # Environment variables (gitignored)
├── .gitignore       # Git ignore rules
├── eslint.config.js # ESLint configuration
├── package.json     # Project dependencies
└── vite.config.js   # Vite configuration
```

## Security

- `.env` file is gitignored to prevent committing sensitive credentials
- Firebase configuration uses environment variables
- `.gitignore` includes patterns for environment files

## Development

The development server runs on `http://localhost:5173` by default (Vite's default port). Hot Module Replacement (HMR) is enabled for fast development.

## What's Been Done

### ✅ Completed

1. **Project Initialization**
   - Set up Vite + React project
   - Configured ESLint for code quality
   - Installed core dependencies

2. **Firebase Integration**
   - Installed Firebase SDK (v12.6.0)
   - Created Firebase initialization file (`src/firebase.js`)
   - Set up environment variable configuration
   - Created `.env` file with Firebase credentials

3. **UI Framework**
   - Installed Chakra UI and Emotion (required dependency)
   - Ready for component development

4. **Security & Configuration**
   - Updated `.gitignore` to exclude sensitive files
   - Environment variables properly configured for Vite

### 🚧 Next Steps

- [ ] Set up Firebase Authentication
- [ ] Configure Firestore database
- [ ] Implement Google Analytics data fetching
- [ ] Create dashboard components with Chakra UI
- [ ] Add routing (if needed)
- [ ] Set up state management (if needed)

## Notes

- All environment variables must be prefixed with `VITE_` to be accessible in client-side code (Vite requirement)
- The Firebase app instance is exported from `src/firebase.js` and can be imported wherever needed
- Restart the dev server after adding new environment variables

## License

[Add your license here]
