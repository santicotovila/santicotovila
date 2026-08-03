# Santiago Coto Vila

## Mobile Developer (iOS & Android)

### About me
Developer focused on the native mobile ecosystem, proficient in both Android and iOS. Specializing in iOS development: from UIKit to the cutting edge of SwiftUI. My experience covers the end-to-end workflow, from frontend to backend.

<p align="left">
  <img src="https://img.shields.io/badge/Swift-F05138?style=for-the-badge&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/SwiftUI-007ACC?style=for-the-badge&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/UIKit-007ACC?style=for-the-badge&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" />
  <img src="https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white" />
  <img src="https://img.shields.io/badge/SwiftData-F05138?style=for-the-badge&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/Vapor-F3507B?style=for-the-badge&logo=vapor&logoColor=white" />
  <img src="https://img.shields.io/badge/Firebase-DD2C00?style=for-the-badge&logo=firebase&logoColor=white" />
</p>

**Santiago Coto Vila** — *Mobile Developer (iOS & Android)*

---

### Projects:

# Nolana — iOS App & Water Sports Community
🔗 [App Store Link](https://apps.apple.com/es/app/nolana/id6774668817)

**Nolana** is a native app designed for the water sports community. It enables spot discovery, community event management, and real-time advanced weather forecast tracking.

---

## Screenshots

<div align="center">
  <table>
    <tr>
      <td align="center"><b>Login</b></td>
      <td align="center"><b>Forecast</b></td>
      <td align="center"><b>Spot Detail</b></td>
    </tr>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/73036355-6f39-4dc8-805f-c543720aa473" height="450" alt="Login" /></td>
      <td><img src="https://github.com/user-attachments/assets/acd6813f-f511-4b9d-aeba-4122cc7dc98a" height="450" alt="Forecast" /></td>
      <td><img src="https://github.com/user-attachments/assets/5e94f772-cc9c-4539-bd56-09e7149e09a2" height="450" alt="Spot Detail" /></td>
    </tr>
    <tr>
      <td align="center"><b>Meetup</b></td>
      <td align="center"><b>Events</b></td>
      <td align="center"><b>Maps</b></td>
    </tr>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/786fd235-dbfa-4af3-8a11-76f5ddbacf28" height="450" alt="Meetup" /></td>
      <td><img src="https://github.com/user-attachments/assets/34e01781-ba86-4edf-8ef9-aef253ad5002" height="450" alt="Events" /></td>
      <td><img src="https://github.com/user-attachments/assets/5db19932-b6c8-4ebe-bdb6-ca1958fbe23f" height="450" alt="Maps" /></td>
    </tr>
  </table>
</div>

---

## Architecture and Design Decisions

The main goal was to achieve a balance between **long-term scalability** and optimal UX.

```text
┌─────────────────────────────────────────────────────────┐
│                   Presentation Layer                    │
│             (SwiftUI + MapKit + ViewModels)             │
└────────────────────────────┬────────────────────────────┘
                             │
                             ▼
┌─────────────────────────────────────────────────────────┐
│                      Domain Layer                       │
│            (Use Cases, Entities & Protocols)            │
└────────────────────────────▲────────────────────────────┘
                             │ 
┌────────────────────────────┴────────────────────────────┐
│                        Data Layer                       │
│  ┌────────────────────────┐  ┌───────────────────────┐  │
│  │    Local Data Source   │  │ External Data Source  │  │
│  │ (SwiftData / Offline   │  │  (Firebase Auth & DB /│  │
│  │        Engine)         │  │ Weather APIs Integr.) │  │
│  └────────────────────────┘  └───────────────────────┘  │
└─────────────────────────────────────────────────────────┘
