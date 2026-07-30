# Santiago Coto Vila

## Mobile Developer (iOS & Android)

---
# 🌊 Nolana — iOS App & Water Sports Community

> **Nolana** es una aplicación nativa para iOS diseñada para la comunidad de deportes acuáticos, centrada en la localización de spots, eventos y consulta de condiciones meteorológicas en tiempo real.

---

##  Arquitectura y Decisiones de Diseño

El objetivo principal en el desarrollo de Nolana ha sido lograr un equilibrio entre **escalabilidad a largo plazo** y **rapidez en la entrega de valor**. 

```
┌─────────────────────────────────────────────────────────────────┐
│                          App Layer                              │
│                    (SwiftUI + MapKit)                           │
└─────────────────────────────────┬───────────────────────────────┘
                                  │
┌─────────────────────────────────▼───────────────────────────────┐
│                      Presentation Layer                         │
│                     (MVVM + Protocols)                          │
└─────────────────────────────────┬───────────────────────────────┘
                                  │
┌─────────────────────────────────▼───────────────────────────────┐
│                         Domain Layer                            │
│                 (Clean Architecture & Entities)                 │
└─────────────────┬───────────────────────────────┬───────────────┘
                  │                               │
┌─────────────────▼───────────────┐ ┌─────────────▼───────────────┐
│            Data Layer           │ │        External Services    │
│    (SwiftData Persistence /     │ │    (Firebase Auth & DB /     │
│        Offline Engine)          │ │     Weather APIs Integration)│
└─────────────────────────────────┘ └─────────────────────────────┘
```

### 1. Patrón de Arquitectura: MVVM + Clean Architecture
Se ha implementado una arquitectura **MVVM respaldada por principios de Clean Architecture**, utilizando **programación orientada a protocolos**. 
* **Ventajas:** Desacoplamiento total entre las vistas y la lógica de negocio, lo que facilita la escalabilidad del código y simplifica la inyección de dependencias para futuras pruebas unitarias (*Unit Testing*).

### 2. Backend & Infraestructura: Firebase vs. Custom Backend
Aunque inicialmente se sopesó el desarrollo de un backend a medida en **Vapor (Swift en servidor)** para un control total de la infraestructura, se optó de forma pragmática por **Firebase**:
* **Razones:** Permite implementar un sistema de autenticación de usuarios y base de datos en la nube seguro, funcional y escalable reduciendo drásticamente el tiempo de desarrollo.

### 3. Estrategia de Red y Persistencia Local (SwiftData)
* **Base de datos de Spots:** En lugar de recurrir a servicios de geocodificación inversa (con alto riesgo de imprecisión en nombres de playas), se integró un dataset estandarizado a nivel europeo como *Single Source of Truth*.
* **Integración de APIs Meteorológicas:** Se combinaron dos servicios REST distintos:
  * *API Principal:* Proporciona datos macro de pronóstico continuo.
  * *API Secundaria (Especializada):* Ofrece métricas avanzadas en detalle, pero con límites de peticiones (*rate-limiting*).
* **Caché con SwiftData:** Para optimizar las llamadas a la API secundaria y garantizar disponibilidad *offline*, se diseñó una capa de persistencia local utilizando **SwiftData** con una ventana de tiempo de validez de datos (*Time To Live - TTL*), asegurando pronósticos precisos sin agotar la cuota del servicio.

### 4. Interfaz de Usuario & Geolocalización
* **UI (SwiftUI):** Prototipado inicial en **Figma** y trasladado a código utilizando **SwiftUI**, aprovechando el motor de renderizado declarativo y animaciones nativas.
* **Geolocalización (MapKit):** Integración nativa con **MapKit** para la detección en tiempo real de eventos y spots cercanos al usuario.

---

##  Tech Stack

* **Lenguaje:** Swift 
* **Framework UI:** SwiftUI
* **Persistencia Local:** SwiftData
* **Mapas:** MapKit
* **Backend / BaaS:** Firebase (Auth, Firestore)
* **Arquitectura:** MVVM + Clean Architecture (Protocol-Driven)
```

---


| Login | Forecast | Spot Detail |
| :---: | :---: | :---: |
| <img src="https://github.com/user-attachments/assets/73036355-6f39-4dc8-805f-c543720aa473" width="250" alt="Inicio" /> | <img src="https://github.com/user-attachments/assets/acd6813f-f511-4b9d-aeba-4122cc7dc98a" width="250" alt="Forecast" /> | <img src="https://github.com/user-attachments/assets/5e94f772-cc9c-4539-bd56-09e7149e09a2" width="250" alt="Spot Detail" /> |

| Meetup | Events | Maps |
| :---: | :---: | :---: |
| <img src="https://github.com/user-attachments/assets/786fd235-dbfa-4af3-8a11-76f5ddbacf28" width="250" alt="Meetup" /> | <img src="https://github.com/user-attachments/assets/34e01781-ba86-4edf-8ef9-aef253ad5002" width="250" alt="Events" /> | <img src="https://github.com/user-attachments/assets/5db19932-b6c8-4ebe-bdb6-ca1958fbe23f" width="250" alt="Maps" /> |

---

### Eventify  
A native app to discover, create, and manage events.  
It includes secure authentication, attendance tracking, and an intuitive interface built with SwiftUI and MVVM architecture.

<img width="300" height="615" alt="Home" src="https://github.com/user-attachments/assets/99c4429c-cde1-4dd9-80f8-403ce24dee45" /><img width="300" height="615" alt="Register1" src="https://github.com/user-attachments/assets/9e64b237-9363-410b-80bf-a07ff6671cd8" />


---

> For more information about each project, please visit their respective repositories.

---

### Contact  
**Portfolio:** [github.com/santicotovila](https://santivila.es) 
**GitHub:** [github.com/santicotovila](https://github.com/santicotovila)  
**LinkedIn:** [linkedin.com/in/santiago-coto-vila-3433a6310](https://www.linkedin.com/in/santiago-coto-vila-3433a6310/)  
**Email:** santiagocotovila@outlook.com

**Curriculum:**  [ Currículum.pdf](https://github.com/user-attachments/files/23939456/Curriculum.pdf)




