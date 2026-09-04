# Course List App (Android / Jetpack Compose)

A modern Android application built with **Kotlin** and **Jetpack Compose** showcasing declarative UI patterns, Material 3 design, custom spring animations, and state preservation across configuration changes.

---

## 📱 Project Overview

The **Course List App** displays an interactive, scrollable list of academic courses. Each course card allows users to dynamically expand and collapse detailed information—including course descriptions and prerequisite requirements—with smooth spring physics animation.

### Key Features

- **Declarative UI with Jetpack Compose**: Built completely with Compose using `LazyColumn` for high-performance list rendering.
- **Interactive Expandable Cards**: Dynamic card states allowing users to inspect course details and prerequisites.
- **Physics-Based Spring Animation**: Uses `animateContentSize` paired with `Spring.DampingRatioMediumBouncy` and `Spring.StiffnessLow` for fluid visual feedback.
- **State Preservation**: Retains expansion state across configuration changes (such as screen rotations) using `rememberSaveable`.
- **Material 3 Design System**: Custom theme integration (`CourseListTheme`) supporting Material 3 color schemes, typography, and card containers.
- **Compose Previews**: Supports light and dark mode design inspection directly within Android Studio previews.

---

## 🛠 Tech Stack

- **Language**: [Kotlin](https://kotlinlang.org/)
- **UI Framework**: [Jetpack Compose](https://developer.android.com/jetpack/compose) (Material 3)
- **Architecture/Components**:
  - `ComponentActivity` & Compose `setContent`
  - `LazyColumn` & Compose State Management (`rememberSaveable`)
  - Compose Animation APIs (`animateContentSize`, `spring`)
- **Build System**: Gradle (Kotlin DSL - `.gradle.kts`)

---

## 📁 Repository Structure

```text
android-courselist-app/
├── courselist/
│   ├── app/
│   │   ├── build.gradle.kts           # Module build configuration & dependencies
│   │   └── src/
│   │       ├── main/
│   │       │   ├── java/com/example/courselist/
│   │       │   │   ├── MainActivity.kt # Core Compose UI, Data Models & Sample Data
│   │       │   │   └── ui/theme/      # Color, Type, and Material3 Theme definitions
│   │       │   ├── res/               # Vector drawables, icons, and strings
│   │       │   └── AndroidManifest.xml
│   │       └── test/                  # Unit testing suite
│   ├── build.gradle.kts               # Root build configuration
│   ├── settings.gradle.kts            # Project settings & repositories
│   └── gradlew                        # Gradle Wrapper script
└── README.md                          # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites

- **Android Studio**: Jellyfish / Koala or newer recommended.
- **JDK**: Java 17 or Java 21 compatible SDK.
- **Android SDK**: API Level 34 (Android 14) or target API supported by project gradle settings.

### Building & Running

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Bedru-Mekiyu/android-courselist-app.git
   cd android-courselist-app/courselist
   ```

2. **Make Gradle wrapper executable (Linux/macOS):**
   ```bash
   chmod +x gradlew
   ```

3. **Build the project:**
   ```bash
   ./gradlew assembleDebug
   ```

4. **Run Unit Tests:**
   ```bash
   ./gradlew test
   ```

5. **Open in Android Studio:**
   - Open Android Studio, select **Open**, and navigate to the `courselist/` directory.
   - Sync Gradle and run on an Android Virtual Device (AVD) or physical device.

---

## 🧪 Testing & Quality Assurance

- **Unit Tests**: Executed via Gradle `./gradlew test`.
- **Compose Previews**: Test `CourseCardPreview`, `CourseCardDarkPreview`, and `CourseListPreview` directly in Android Studio.

---

## 📄 License

This project is open-source and available under standard repository terms.
