# UniqueMusic

UniqueMusic is a cross-platform **React Native + Expo** powered music player app designed to deliver a seamless audio playback experience on **Android, Web, and PC (via APK emulators)**.

This project uses:

* **Expo Router** for navigation
* **EAS Build** for production APK
* **Google Authentication**
* **Custom Backend (Vercel)** for streaming songs & thumbnails
* **Advanced Music Player UI** using `react-native-reanimated`, `gesture-handler`, and custom components

---

## 🚀 Features

### 🎵 Music Streaming

* Fetches songs & thumbnails from your custom backend
* Smooth playback using `expo-av`
* Handles large music folders efficiently

### 🔊 Modern Music Player (MusicPlayer.js)

* Fully custom-designed player screen
* Capsule-shaped seek bar
* Bullet-style movable progress thumb
* Gesture-based bottom-sheet style controls
* Optimized for Android & Web

### 🖼️ UI/UX

* Edge-to-edge Android design
* Custom adaptive icons
* Dark/light mode support
* Smooth transitions with the new React Compiler enabled

### 🔐 Authentication

* Google OAuth login integrated via Expo

### 🌐 Backend

* Hosted on Vercel
* Songs streamed via `/api/music` endpoint
* CORS configured for Expo web

### 📦 Packaging

* Supports **EAS Production Builds** for Android
* Generates both `.apk` and `.aab`

---

## 📁 Project Structure

```
MusicAndroid/
│
├── app/
│   ├── index.js
│   ├── MusicPlayer.js      # ⬅️ replaced PlayerScreen.js
│   ├── MusicListScreen.js
│
├── components/
│   ├── PlayerControls.js
│   ├── SliderBar.js
│
├── assets/
│   ├── icon.png            # 1024×1024 Expo icon
│   ├── splash.png
│
├── server/                 # standalone backend (Vercel)
│
├── eas.json
├── app.json
├── package.json
```

---

## ⚙️ Setup

### 1️⃣ Install dependencies

```sh
yarn install
```

### 2️⃣ Start development

```sh
yarn start
```

### 3️⃣ Android build (APK/AAB)

```sh
eas build --platform android --profile production
```

---

## 🛠️ Build Requirements

* Expo icons: **1024×1024 PNG**, no transparency
* Adaptive icon: same PNG + background color
* Ensure `slug` and `projectId` follow Expo guidelines

---

## 🌍 Deployment

### Backend (Vercel)

* Place all songs in cloud storage
* Index with `/api/music` using folderId
* Supports streaming + metadata

---

## 💡 Notes

* `PlayerScreen.js` has been replaced with **`MusicPlayer.js`** everywhere in the app
* Expo Router uses typed routes (experimental)
* `newArchEnabled: true` enabled for performance

---

