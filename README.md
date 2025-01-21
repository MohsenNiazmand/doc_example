# Kitchen Display System (KDS) App

A robust Kitchen Display System (KDS) application built with Flutter, utilizing Clean Architecture principles and various modern libraries for state management, routing, and localization.

## Table of Contents

- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Features](#features)
- [Testing and Debugging](#testing-and-debugging)
- [API Documentation](#api-documentation)
- [Future Development](#future-development)
- [Resources](#resources)
- [Conclusion](#conclusion)

## Introduction

The KDS app is designed to streamline kitchen operations by displaying orders in real-time. It leverages Clean Architecture for maintainability and scalability, ensuring a smooth user experience.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Flutter SDK installed on your machine. Follow the [official installation guide](https://flutter.dev/docs/get-started/install).
- Android Studio or Xcode for running the application on emulators or physical devices.
- Basic knowledge of Dart and Flutter.

## Installation

To install and run this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://gitlab.sunshineteam.ca/fusion-food-tech/mobile-apps/kitchen-display-system.git
   ```
2. Navigate to the project directory:
   ```bash
   cd kds_app
   ```
3. Install the required packages:
   ```bash
   flutter pub get
   ```
4. Run the application:
   ```bash
   flutter run
   ```

## Project Structure

The project structure is organized as follows:

```
kds_app/
├── android/                # Android-specific files
├── ios/                    # iOS-specific files
├── lib/                    # Main Dart code
│   ├── main_common.dart    # Entry point of the application
│   ├── util/               # Several functional elements in the app
│   ├── shared/	            # Reusable components
│   ├── resources/          # Resources for the application
│   ├── mains/ 	            # All flavors entries
│   ├── features/           # Feature modules
│   ├── core/               # core modules
│   └── config/             # Including APIs, extensions, localization, routes and theme
├── assets/                 # Images and GIFs
├── test/                   # Unit and widget tests
└── pubspec.yaml            # Project configuration and dependencies
```

## Features

- **Real-time Order Display**: View and manage kitchen orders in real-time.
  ![Order Display](https://raw.githubusercontent.com/MohsenNiazmand/doc_example/master/doc/order_display.gif)

- **User -Friendly Interface**: Intuitive UI for easy navigation.
  ![User  Interface](https://raw.githubusercontent.com/MohsenNiazmand/doc_example/master/doc/user_interface.gif)

- **State Management**: Utilize Riverpod for efficient state management.

- **Routing**: Navigate seamlessly using Go Router.

- **Localization**: Support multiple languages for diverse user bases.

- **Dependency Injection**: Use GetIt for managing dependencies.

- **Network Requests**: Handle API calls with Dio Retrofit.

## Testing and Debugging

To run the tests for this project, use the following command:

```bash
flutter test
```

For debugging, leverage the built-in debugging tools in Android Studio or Visual Studio Code.

## API Documentation

This project uses a RESTful API for order management. The API endpoints are documented in the `api_documentation.md` file located in the root directory.

## Future Development

- Implement push notifications for order updates.
- Enhance user interface based on user feedback.
- Add analytics for kitchen performance tracking.

## Resources

- [Flutter Documentation](https://flutter.dev/docs)
- [Dart Language](https://dart.dev/)
- [GitHub Repository](https://gitlab.sunshineteam.ca/fusion-food-tech/mobile-apps/kitchen-display-system)

## Conclusion

Thank you for exploring the Kitchen Display System app! We hope it enhances your kitchen operations. Feel free to contribute or reach out with any questions or suggestions.

---

**Author**: Mohsen Niazmand  
[LinkedIn](https://ir.linkedin.com/in/mohsen-niazmand-6b5b12201)  
[GitHub](https://github.com/MohsenNiazmand)

---
