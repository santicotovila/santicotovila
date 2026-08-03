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






# Eventify — iOS App

A native app to discover, create, and manage events, with secure authentication and attendance tracking.

## ScreenShots

<img width="1919" height="2353" alt="Screenshots" src="https://github.com/user-attachments/assets/39b8af2d-0c8d-4ecf-8b19-f1a778b7c8ad" />

---

## Table of Contents
- [Key Advantages](#key-advantages)
- [Requirements](#requirements)
- [How to Run the Project](#how-to-run-the-project)
- [Navigation Structure](#navigation-structure)
- [Authentication](#authentication)
- [Attendance System](#attendance-system)
- [Roadmap](#roadmap)
- [Architecture (iOS)](#architecture-ios)
- [Quality & Testing](#quality--testing)
- [Performance & Accessibility](#performance--accessibility)
- [Backend (Technical Overview)](#backend-technical-overview)
- [Security & Compliance](#security--compliance)
- [Contact](#contact)

---

## Key Advantages
- Clear separation of responsibilities.  
- Easier unit testing.  
- Simpler maintenance and scaling.  

---

## Requirements
- iOS 18 or later.  

---

## How to Run the Project
1. Clone the repository.  
2. Open the project in Xcode.  
3. Adjust the **Bundle Identifier** and signing if needed.  
4. Run on a simulator or a physical device.  
5. Configure backend variables if you want to connect to the real server. (A `.env.example` is included)

> By default, the app can run fully with *mock* data.

---

## Navigation Structure
- **Events**: General list of events.  
- **New Event**: Creation via a modal view with date and time pickers.  
- **EventiBot**: Assistant with suggestions *(view in progress)*.  
- **Profile**: User info and settings.

---

## Authentication
- Sign in with **email** and **password**.  
- Real-time field validation.  
- Credentials securely stored in **Keychain**.  
- Global session state managed by `AppStateViewModel`.

---

## Attendance System
Each user can set their status for an event:
- *Going*  
- *Not going*  
- *Maybe*

The event detail screen shows the live count for each status.

---

## Roadmap
- [ ] Full **EventiBot** integration with AI (text and voice).  
- [ ] Push notifications for reminders.  
- [ ] Share events via WhatsApp, email, or calendar.  
- [ ] Biometric authentication (Face ID / Touch ID).  
- [ ] Geolocation and interactive maps.  
- [ ] Personal app customization.

---

## Architecture (iOS)
- **MVVM** with **SwiftUI**.  
- **Layers**:
  - **Presentation**: SwiftUI views and ViewModels (state and bindings).  
  - **Domain**: Use cases, entities, and protocols.  
  - **Data**: Repositories, data sources (remote/local), *mappers*, and *DTOs*.  
- **Principles**: dependency injection, low coupling, testability.
  
## Reactive Frameworks & Patterns
- **State management (SwiftUI):** `@State`, `@Binding`, `@ObservedObject`, `@Environment` for unidirectional data flow and reactive views.
  
## Quality & Testing
- **Unit Tests** for use cases and *ViewModels*.  
- **Mocks/Stubs** for repositories and data sources.  

## Performance & Accessibility

---

## Backend (Technical Overview)

**Goal:**  
Build a solid, secure, and scalable base to manage users, events, and interests within the app.

### Technology
- **Framework:** Vapor  
- **Tools:** Postman for endpoint testing  
- **Databases:** SQLite in local environment and PostgreSQL in production  

### Project Structure
Code is organized into well-defined modules:
- `Models`
- `Controllers`
- `DTOs`
- `Migrations`
- `Middleware`
- `JWT`
- `Jobs`
- `Tools/Constants`

### Core Models
- **User:** normalized emails and passwords encrypted with **BCrypt**.  
- **Interest / UserInterest:** optimized many-to-many relationship to manage user interests.  
- **Event:** includes name, date, category, location, and coordinates.  
- **EventAttendance:** defines the different attendance states for users per event.

### Authentication
Implemented via **JWT tokens** (access and refresh), with protected routes according to role and access level.

### Security
- Private keys are kept out of the repository.  
- No credentials are included in the source code.  
- A `.env.example` is provided to test the server.

### Migrations
Include entity creation, pivot relationships, and an initial *seed* for testing and development.

---

## Security & Compliance
*(Reserved section for future policies and compliance details.)*

---

## Contact
- Javier Gómez — [javiergomezdev@gmail.com](mailto:javiergomezdev@gmail.com)  
- Santiago Coto — [santiagocotovila@outlook.com](mailto:santiagocotovila@outlook.com)  
- Manuel Liébana — [manololiebana@gmail.com](mailto:manololiebana@gmail.com)

