# MultiSim: Modern eSIM Profile Manager for Android

![MultiSim App Logo](app_logo.png)

## Project Overview

MultiSim is an Android application designed to manage eSIM profiles on programmable/removable SIM cards, functioning as a Local Profile Assistant (LPA) application. The primary goal is to provide a fast, modern, and user-friendly alternative to existing LPA apps, leveraging the latest Android features (12-15) to deliver superior performance and user experience.

## Key Requirements

### 1. Core Functionality

*   **Download and Install Profiles**: Acquire and install eSIM profiles from SM-DP+ servers using activation codes.
*   **Profile Management**: Enable, disable, and delete eSIM profiles stored on the programmable SIM card.
*   **Customization**: Rename profiles for easy identification.
*   **Profile Details**: View comprehensive profile information (ICCID, provider name, status, etc.).
*   **Activation Methods**: Support both QR code scanning and manual activation code entry.

### 2. Technical Specifications

*   **Rootless Operation**: Must function without root access, utilizing standard Android TelephonyManager APIs.
*   **SIM Communication**: Communicate with programmable SIM cards via APDU commands.
*   **eSIM Standard Compliance**: Implement GSMA SGP.22 specification for eSIM remote provisioning.
*   **Authentication**: Support ARA-M (Access Rule Applet) authentication.
*   **Asynchronous Operations**: Efficiently handle asynchronous SIM operations.

### 3. Performance Priorities (Critical)

*   **Fast Profile Switching**: Achieve profile switching times under 2 seconds.
*   **Optimized APDU Commands**: Implement optimized APDU command batching.
*   **Efficient Caching**: Utilize efficient caching mechanisms for profile metadata.
*   **Smooth UI**: Ensure a smooth user interface with no blocking operations.
*   **Background Processing**: All SIM operations must run on background threads.
*   **Minimized I/O**: Minimize unnecessary SIM card reads/writes.

### 4. User Interface

*   **Modern Design**: Adhere to Material Design 3 (Material You) guidelines with dynamic theming.
*   **Intuitive Experience**: Provide a clean and intuitive interface.
*   **Profile List View**: Display all stored eSIM profiles with clear status indicators.
*   **Quick Actions**: Implement swipe gestures for quick enable/disable/delete actions.
*   **Dark Mode**: Full support for system-wide dark mode.
*   **Search/Filter**: Functionality to search and filter profiles.
*   **Home Screen Widget**: Quick-switch widget for the home screen.
*   **Predictive Back**: Support for predictive back gestures (Android 13+).
*   **Edge-to-Edge Display**: Optimized for edge-to-edge display.

### 5. Additional Features

*   **Usage Statistics**: (If available) Display profile usage statistics (data used, calls, etc.).
*   **Favorites/Pinning**: Option to mark favorite or pin profiles.
*   **Import/Export**: Functionality to import and export profile configurations.
*   **Notifications**: Notifications for profile status changes.
*   **Multi-language Support**: Comprehensive multi-language support.
*   **Per-app Language**: Per-app language preferences (Android 13+).

### 6. Compatibility

*   **Target SDK**: Android 15 (API 35).
*   **Minimum SDK**: Android 12 (API 31).
*   **SIM Card Support**: Support for various programmable SIM cards (e9sim, 5ber eSIM, etc.).
*   **Robustness**: Gracefully handle different SIM card implementations.

## Technical Stack

*   **Language**: Kotlin (latest stable version)
*   **Architecture**: MVVM with Clean Architecture principles
*   **UI**: Jetpack Compose (modern declarative UI framework)
*   **Database**: Room (for persistent caching of profile data)
*   **Asynchronous Operations**: Kotlin Coroutines + Flow
*   **Dependency Injection**: Hilt
*   **Card Communication**: OMAPI (Open Mobile API)
*   **Navigation**: Jetpack Compose Navigation
*   **Permissions**: Android 12+ runtime permission handling

## Modern Android Features Leveraged

*   **Material You**: Dynamic color theming for a personalized user experience.
*   **Splash Screen API**: Enhanced splash screen experience (Android 12+).
*   **Predictive Back Animations**: Improved navigation fluidity (Android 13+).
*   **Notification Runtime Permissions**: Granular control over notifications (Android 13+).
*   **Photo Picker**: Secure and modern way to pick QR code images (Android 13+).
*   **Foreground Service Types**: Proper categorization and management of background SIM operations (Android 14+).
*   **Edge-to-Edge Display**: Maximizing screen real estate with proper insets handling.

## Reference Projects

For inspiration and understanding of APDU implementation and SGP.22 compliance, the following projects are noted:

*   [EasyEUICC/OpenEUICC](https://github.com/estkme-group/openeuicc)

## Repository Structure and Output

This repository is structured to facilitate a clean, well-documented, and maintainable Android project. The output includes:

*   A clear GitHub repository structure.
*   Clean, well-documented code following best practices.
*   A comprehensive `README.md` with setup instructions.
*   Modern Gradle build configuration using Kotlin DSL and Version Catalogs.
*   Basic unit tests for critical functions.
*   (Optional) GitHub Actions CI/CD workflow for automated builds and tests.

## Getting Started

To set up the project locally, clone the repository and open it in Android Studio. Ensure you have the latest Android SDKs and Gradle version installed.

```bash
git clone https://github.com/KotlinJS5/MultiSim.git
cd MultiSim
```

Further setup instructions and development guidelines will be detailed as the project progresses.
