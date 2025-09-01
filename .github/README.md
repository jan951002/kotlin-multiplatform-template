# Kotlin Multiplatform Project Template

## 📱 Business Description
This template provides a solid foundation for building cross-platform mobile applications using Kotlin Multiplatform Mobile (KMM). It enables code sharing between Android and iOS platforms while maintaining native performance and user experience.

## 🔧 Technical Description
A production-ready Kotlin Multiplatform project template that shares:
- Business Logic
- Data Layer & Repository Pattern
- Networking Layer
- Domain Models
- Use Cases & Interactors

### Supported Platforms
- ✅ Android (API 24+)
- ✅ iOS (iOS 14+)
- ⏳ Desktop (Compose Desktop) - Future support
- ⏳ Web (Kotlin/JS) - Future support

## 🏗️ Architecture
- **Architecture Pattern**: Clean Architecture + MVVM
- **Dependency Injection**: Koin
- **Networking**: Ktor Client
- **Serialization**: Kotlinx Serialization
- **Database**: SQLDelight
- **UI Framework**: 
  - Android: Jetpack Compose
  - iOS: SwiftUI (with shared ViewModels)

## 🚀 Getting Started

### Prerequisites
- Android Studio Giraffe+ or IntelliJ IDEA 2023.1+
- Xcode 14+ (for iOS development)
- JDK 17+
- Kotlin 1.9.20+

### Setup
1. Click "Use this template" button
2. Clone your new repository
3. Open the project in Android Studio
4. Sync Gradle files
5. Run Android app: `./gradlew :androidApp:installDebug`
6. Run iOS app: Open `iosApp/iosApp.xcodeproj` in Xcode

## 📦 Module Structure
```
├── shared/                 # Shared Kotlin code
│   ├── commonMain/        # Common code for all platforms
│   ├── commonTest/        # Common unit tests
│   ├── androidMain/       # Android-specific implementations
│   └── iosMain/          # iOS-specific implementations
├── androidApp/            # Android application
├── iosApp/               # iOS application
└── buildSrc/             # Build logic and dependencies
```

## 🔄 Branching Strategy

### Branch Types
- `feature/description` - New features and functionality
- `fix/description` - Bug fixes and hotfixes
- `backport/description` - Automated backport changes
- `release/x.y.z` - Release preparation branches

### Automated Workflows
- **Hotfix Flow**: `fix/*` → Auto-creates `backport/*` → Auto-PR to master
- **Feature Flow**: `feature/*` → PR to develop
- **Release Flow**: `release/*` → Full validation → Master merge + Tag

## 🧪 Testing
```bash
# Run all tests
./gradlew check

# Run common tests only
./gradlew :shared:testDebugUnitTest

# Run Android tests
./gradlew :androidApp:testDebugUnitTest

# iOS tests (run in Xcode)
```

## 📊 Code Quality
- **Linting**: Ktlint + Detekt
- **Coverage**: JaCoCo reports
- **Static Analysis**: Detekt rules
- **Pre-commit Hooks**: Automated formatting and validation

## 🚀 CI/CD
- ✅ Automated testing on PR
- ✅ Code quality checks
- ✅ Branch naming enforcement
- ✅ Automated changelog updates
- ✅ Release automation
- ⏳ Google Play deployment (future)
- ⏳ Maven Central publishing (future)

## 📝 Contributing
1. Follow the branching strategy
2. Ensure all tests pass
3. Update changelog if needed
4. Add appropriate documentation
5. Follow code style guidelines

## 📄 License
[Your License Here]

## 🔗 Useful Links
- [Kotlin Multiplatform Documentation](https://kotlinlang.org/docs/multiplatform.html)
- [Compose Multiplatform](https://www.jetbrains.com/lp/compose-multiplatform/)
- [SQLDelight Documentation](https://sqldelight.github.io/sqldelight/)
- [Ktor Documentation](https://ktor.io/docs/)
