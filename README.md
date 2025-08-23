# 👁️ GazeGuard

**GazeGuard** is an advanced Android application designed to help monitor and manage screen time using eye-tracking system. By leveraging real-time eye-tracking and app usage analytics, GazeGuard empowers families to promote healthier digital habits and ensure responsible device use.

---

## 🚀 Features

- 🔍 **AI-Powered Gaze Detection**  
  Uses a YOLOv5-based model to detect if the user is looking at the screen, not looking, or has eyes closed.

- ⏱️ **Screen Time Measurement**  
  Tracks *active* screen time based on gaze, not just device usage.

- 📊 **Parental Dashboard**  
  View detailed daily screen time, app usage breakdowns, and historical trends for each child.

- ⛔ **Screen Time Limits & Auto-Lock**  
  Set daily screen time limits and unlock schedules. Devices auto-lock when limits are reached.

- 📱 **App Usage Analytics**  
  Visualize most-used apps with per-app time and usage charts.

- 🔔 **Realtime Notifications**  
  Parents receive alerts when screen time limits are exceeded and the device locks.

- 🔐 **Secure Authentication**  
  Email/password and Google sign-in via Firebase Authentication.

- 📄 **End-User License Agreement (EULA)**  
  Displayed and enforced on first launch for compliance and transparency.

- 🎨 **Modern UI**  
  Clean Material Design with tooltips and dialogs for a smooth user experience.

---
![GazeGuard Demo](https://github.com/JNico07/nico-portfolio/blob/main/public/gazeguard.gif)
---

## 🛠️ Getting Started

### 📋 Prerequisites

- Android Studio (Giraffe or newer recommended)  
- Android SDK: `minSdkVersion 26`, `targetSdkVersion 34`  
- Java 17  
- Google Firebase Project (for Auth, Firestore, Realtime DB, Messaging, AppCheck)  
- Internet connection (for Firebase and model download)

### ⚙️ Build & Run Instructions

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/GazeGuard.git
   cd GazeGuard

2. **Open in Android Studio**
- Select **"Open an existing project"**.
- Choose the `GazeGuard` directory.

3. **Configure Firebase**
- Add your `google-services.json` file to the `/app` folder.
- Ensure your Firebase project has the following services enabled:
  - Firebase **Authentication**
  - **Realtime Database**
  - **Firestore**

4. **Build the Project**
- Allow **Gradle** to sync and download dependencies.
- Build the project using the **Build** menu or click the ▶️ **Run** button.

5. **Run on a Device**
- Use a **real Android device** (camera required) with minimum Android **8.0 (API 26)**.
- Grant all requested permissions:
  - 📷 Camera
  - 📊 Usage Stats
  - 🔔 Notifications
  - ⚙️ Others as requested

6. **First Launch**
- Accept the **EULA** on startup.
- **Register** or **log in** using Firebase Auth.
- Set up **profiles** and begin monitoring screen time.

---

## 📦 Dependencies

The project uses the following key libraries and frameworks:

- **AndroidX** – AppCompat, CameraX, Lifecycle, Navigation, RecyclerView, etc.
- **Firebase** – Auth, Realtime Database, Firestore, Messaging, AppCheck
- **PyTorch Mobile** – For on-device gaze detection
- **MPAndroidChart** – Data visualization
- **Glide** – Efficient image loading
- **Material Components** – Modern UI styling
- **FirebaseUI** – Pre-built Auth and DB UI
- **Others** – NiceSpinner, CircleImageView, TargetTooltip (UI enhancements)

👉 Full list available in [`app/build.gradle`](./app/build.gradle)

---

## 🔐 Permissions Required

The app requests the following Android permissions:

- 📷 **Camera** – For gaze detection
- 📊 **Usage Stats** – To track app usage accurately
- 🔄 **Foreground Service** – For continuous background monitoring
- 🔔 **Notifications** – For alerts and parental updates
- 🔒 **Device Admin** – Enables screen auto-lock
- 🌐 **Internet, Network State, Storage** – Firebase & analytics functionality
