# 🚌 Vidyarthi-Bus

> **Crowdsourced Bus Alert App for College Students in Mangaluru**

A real-time Android application that shows college students the crowd level of their bus **before it arrives** at their stop — helping them decide whether to wait or find an alternative.

---

## 📽️ Demo Video

[https://github.com/user-attachments/assets/7de92215-0f5f-4047-be15-d7b3cd5e1c8b](https://github.com/user-attachments/assets/885e3cd0-0fae-4476-8e8b-42da4ab52cf2)


---

## 📌 Problem Statement

Students in remote areas around Mangaluru depend entirely on college buses for their daily commute. When a bus is already full or cancelled, students waiting at the stop have **no way of knowing** until it physically arrives — by which time it is too late. This results in students missing lectures, tests, and examinations.

---

## 💡 Solution

Vidyarthi-Bus turns every student on the bus into a **real-time data contributor**. Students already on the bus report crowd status with one tap. Students waiting at the stop instantly see it through a **color-coded Crowd Meter** and decide whether to wait or find a shared auto.

---

## ✨ Features

- 🏫 **College Selection** — Choose from SIT, SCEM, Sahyadri, or Canara College
- 🚌 **Route List** — View all bus routes for your college with live status tags
- 📊 **Crowd Meter** — Real-time horizontal progress bar (Green / Amber / Red)
- 📍 **One-Tap Reporting** — Report crowd status with GPS validation
- ⏱️ **Auto-Expiry** — Reports expire after 15 minutes to keep data fresh
- 🛺 **Alternatives** — View shared auto contacts with one-tap calling
- ⚠️ **Empty State** — "No recent updates — Be the first to report!" when no data

---

## 🎨 Crowd Status Colors

| Status | Color | Meaning |
|---|---|---|
| EMPTY | 🟢 Green | Seats available — safe to wait |
| FILLING | 🟡 Amber | Filling up — board soon |
| FULL | 🔴 Red | No seats — find alternative |
| NO DATA | ⚪ Grey | No report in last 15 minutes |

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Kotlin | Primary Android development language |
| Android Studio | IDE used to build the app |
| Firebase Realtime DB | Real-time crowd status sync across devices |
| FusedLocationProviderClient | GPS validation (500m proximity check) |
| Material Design Components | Buttons, cards, progress bars |
| RecyclerView + CardView | Route list and alternatives UI |
| XML Layouts | Screen UI structure |
| MVVM Architecture | Clean code separation |

---

## 📁 Project Structure

```
app/
└── src/main/
    ├── java/com/example/vidyarthibus/
    │   ├── model/
    │   │   ├── BusRoute.kt
    │   │   └── Alternative.kt
    │   ├── adapter/
    │   │   ├── RouteAdapter.kt
    │   │   └── AlternativeAdapter.kt
    │   ├── SplashActivity.kt
    │   ├── RouteListActivity.kt
    │   ├── CrowdMeterActivity.kt
    │   └── AlternativesActivity.kt
    └── res/
        ├── layout/
        │   ├── activity_splash.xml
        │   ├── activity_route_list.xml
        │   ├── activity_crowd_meter.xml
        │   ├── activity_alternatives.xml
        │   ├── item_route.xml
        │   └── item_alternative.xml
        └── values/
            ├── colors.xml
            └── strings.xml
```

---

## 🔥 Firebase Database Structure

```
vidyarthibus-default-rtdb/
├── routes/
│   ├── route_1/
│   │   ├── routeName: "Vamanjoor to SIT"
│   │   ├── crowdStatus: "EMPTY" | "FILLING" | "FULL"
│   │   ├── lastUpdated: 1746316800000
│   │   ├── reporterLat: 12.8734
│   │   ├── reporterLng: 74.8412
│   │   └── college: "SIT, Mangaluru"
└── alternatives/
    ├── alt_1/
    │   ├── name: "Raju Auto Stand"
    │   ├── area: "Kankanady Junction"
    │   └── phone: "9845123456"
```

---

## 🚀 Getting Started

### Prerequisites
- Android Studio (Hedgehog or later)
- Android device or emulator (API 26+)
- Firebase account

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/VidyarthiBus.git
   cd VidyarthiBus
   ```

2. **Set up Firebase**
   - Go to [Firebase Console](https://console.firebase.google.com)
   - Create a new project called `VidyarthiBus`
   - Add an Android app with package name `com.example.vidyarthibus`
   - Download `google-services.json` and place it in the `app/` folder

3. **Enable Realtime Database**
   - In Firebase Console → Build → Realtime Database
   - Set rules to allow read/write (for development)

4. **Add test data**
   - Import the sample JSON from the Firebase section above

5. **Build and run**
   - Open project in Android Studio
   - Click **Sync Now** after Gradle loads
   - Run on emulator or real device

---

## 📋 Permissions Required

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```

---

## 🏫 Supported Colleges

| College | Routes |
|---|---|
| SIT, Mangaluru | Vamanjoor, Kankanady, Mangaluru Central, Surathkal |
| Sahyadri College of Engineering and Management, Mangaluru | Mangaluru Central, Kankanady, Hampankatta, Surathkal, Bajpe, Puttur, Bantwal, Ullal |
| Canara College, Mangaluru | Mangaluru Central, Kankanady, Bejai, Surathkal, Ullal, Bajpe |

---

## ✅ Success Criteria

- [x] Crowd Meter updates instantly for all users on the same route
- [x] App blocks reports from users not near the bus route (GPS check)
- [x] UI is lightweight and fast on low-end Android devices
- [x] Reports auto-expire after 15 minutes
- [x] Routes filtered per college — no cross-college data shown

---

## 👩‍💻 Developer

**Adwaidh K Nambiar**
Srinivas Institute of Technology, Mangaluru
MindMatrix VTU Internship Programme — April 2026

---

## 📄 License

This project was built as part of the **MindMatrix VTU Internship Programme**.
Project Title: 21 | Category: Infrastructure | Platform: Android (Kotlin)

---

> *"Vidyarthi-Bus proves that students can build technology that serves students — turning a daily frustration into a smart, connected, community solution."*
