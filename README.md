# Santiago Coto Vila

## Mobile Developer (iOS & Android)

# Nolana — iOS App & Water Sports Community

<p align="left">
  <img src="https://img.shields.io/badge/Swift-F05138?style=for-the-badge&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/SwiftUI-007ACC?style=for-the-badge&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/SwiftData-000000?style=for-the-badge&logo=apple&logoColor=white" />
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" />
</p>

**Santiago Coto Vila** — *Mobile Developer (iOS & Android)*

---

## Sobre el Proyecto

**Nolana** es una aplicación nativa para iOS diseñada para la comunidad de deportes acuáticos. Permite la localización de *spots*, gestión de eventos comunitarios y la consulta de condiciones meteorológicas avanzadas en tiempo real.

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
      <td><img src="https://github.com/user-attachments/assets/73036355-6f39-4dc8-805f-c543720aa473" height="450" alt="Inicio" /></td>
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

## Arquitectura y Decisiones de Diseño

El objetivo principal ha sido lograr un equilibrio entre **escalabilidad a largo plazo** y **rapidez en la entrega de valor**.

```text
┌─────────────────────────────────────────────────────────────────┐
│                           App Layer                             │
│                      (SwiftUI + MapKit)                         │
└─────────────────────────────────┬───────────────────────────────┘
                                  │
┌─────────────────────────────────▼───────────────────────────────┐
│                       Presentation Layer                        │
│                      (MVVM + Protocols)                         │
└─────────────────────────────────┬───────────────────────────────┘
                                  │
┌─────────────────────────────────▼───────────────────────────────┐
│                          Domain Layer                           │
│                 (Clean Architecture & Entities)                 │
└─────────────────┬───────────────────────────────┬───────────────┘
                  │                               │
┌─────────────────▼───────────────┐ ┌─────────────▼───────────────┐
│            Data Layer           │ │       External Services     │
│    (SwiftData Persistence /     │ │    (Firebase Auth & DB /    │
│         Offline Engine)         │ │ Weather APIs Integration)   │
└─────────────────────────────────┘ └─────────────────────────────┘
