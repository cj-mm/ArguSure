# Development Set-up

## Prerequisites

- Google Chrome Browser (https://www.google.com/intl/en_uk/chrome/dr/download/?brand=CHBD&gad_source=1&gclid=EAIaIQobChMIp8LvjpXEhgMVIV8PAh0_DgaJEAAYASAAEgLZd_D_BwE&gclsrc=aw.ds)
- node.js / npm (https://nodejs.org/en/download/package-manager)
- MongoDB Project (https://www.mongodb.com/)
- Firebase Project (https://firebase.google.com/)
- Gemini API key (https://ai.google.dev/)
- Google OAuth Client ID (see 0:14 to 1:49 in https://www.youtube.com/watch?v=r5ff1_3WrPM&list=LL&index=5)

## Instructions

### Web Application

#### Backend

1. Go to `web_application` directory
2. Run the following command to install dependencies:

```
npm install
```

3. Create a .env file containing:

```
MONGO = <your mongodb connection string + "?directConnection=true">
JWT_SECRET = <your JWT secret key (can be anything)>
```

4. Run the server using the following command:

```
npm run dev
```

#### Frontend

1. Go to `web_application\client` directory
2. Run the following command to install dependencies:

```
npm install
```

3. Create a .env file containing:

```
VITE_GEMINI_API_KEY = <your Gemini API key>
VITE_GOOGLE_CLIENT_ID = <your OAuth client ID>
```

4. See `firebase.js` in `web_application\client\src`. Modify `firebaseConfig` accordingly using your Firebase Project credentials. You might add your Firebase API key in .env file.

5. Run the client locally on `http://localhost:5173/` (default port in Vite React app, make sure this is available) using the following command:

```
npm run dev
```

### Chrome Extension

1. Go to `chrome_extension` directory
2. Run the following command to install dependencies:

```
npm install
```

3. Create a .env file containing:

```
VITE_FIREBASE_API_KEY = <your Firebase API key>
VITE_GEMINI_API_KEY = <your Gemini API key>
```

4. Run the following build command to output the `dist` folder.

```
npm run build
```

5. Open Chrome and go to `chrome://extensions`, turn on `Developer mode`, then hit `Load Unpacked` and choose the newly made `dist` directory.
