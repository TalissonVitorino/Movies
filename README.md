# Movies

Kotlin Multiplatform application built with Compose Multiplatform.

The project explores shared UI, domain logic reuse, and clean separation between platform-specific and common layers.

---

## Overview

Movies is a multiplatform client application designed to:

- Share business logic across Android and iOS  
- Reuse UI via Compose Multiplatform  
- Maintain clear architectural boundaries  
- Demonstrate scalable project structure in KMP  

### Targets

- Android  
- iOS  
- Desktop JVM (optional)

---

## Architecture

The project follows a layered architecture with clear separation of concerns:


composeApp/
├── commonMain
│ ├── presentation
│ ├── domain
│ └── data
│
├── androidMain
├── iosMain
└── jvmMain


### Layers

#### Presentation
- Compose UI  
- ViewModels  
- UI state modeling  

#### Domain
- Use cases  
- Business rules  
- Platform-agnostic contracts  

#### Data
- Repository implementations  
- Remote API integration  
- Mapping between DTO and domain models  

---

## Tech Stack

- Kotlin Multiplatform  
- Compose Multiplatform  
- Kotlin Coroutines  
- Ktor (if applicable)  
- Kotlinx Serialization  
- Gradle Kotlin DSL  

---

## State Management

UI state is modeled explicitly to avoid implicit side effects.

Pattern used:

- Sealed UI state  
- Immutable data models  
- Structured concurrency with coroutines  
- Explicit error handling  

---

## Running the Project

### Android

macOS / Linux:

```bash
./gradlew :composeApp:assembleDebug

Windows:

.\gradlew.bat :composeApp:assembleDebug

Or run directly from Android Studio.

iOS

Open /iosApp in Xcode and run on a simulator.

API Configuration (If Applicable)

Create a local.properties file:

API_KEY=your_api_key

Secrets are not committed to the repository.

Design Decisions

UI is shared to reduce duplication between platforms

Platform-specific APIs are isolated in their respective source sets

Domain layer does not depend on platform implementations

Clear separation enables future expansion (e.g., Desktop or Web targets)

Roadmap

Add pagination

Introduce local caching

Expand test coverage

Improve error resilience

CI integration

Author

Talisson Vitorino
Android | Kotlin | Compose | Multiplatform
