# Hermesdorid

A simple Flutter app that displays the current time.

## Screenshot

Displays the current date and time in real-time, updating every second.

## Getting Started

This project is a starting point for a Flutter application.

### Prerequisites

- **Flutter SDK** (see [flutter.dev](https://flutter.dev))
- **Android SDK** (for Android builds)
- **Java 17+** (for Android builds)
- **Git** (to clone the repository)

### Setup

```bash
# Clone the repository
git clone https://github.com/Sulaiman507/Hermesdorid.git
cd Hermesdorid

# Get dependencies
flutter pub get
```

### Run on Android device or emulator

```bash
flutter run
```

Make sure you have an Android device connected (with USB debugging enabled) or an Android emulator running.

### Build APK

```bash
# Debug APK (for testing)
flutter build apk --debug

# Release APK (for distribution)
flutter build apk --release
```

The APK will be located at:
```
build/app/outputs/flutter-apk/app-debug.apk
# or
build/app/outputs/flutter-apk/app-release.apk
```

### Build App Bundle (recommended for Play Store)

```bash
flutter build appbundle --release
```

The bundle will be at:
```
build/app/outputs/bundle/release/app-release.aab
```

### Build for other platforms

```bash
# Web
flutter build web

# iOS (macOS only)
flutter build ios

# Linux
flutter build linux

# Windows
flutter build windows

# macOS
flutter build macos
```

## Project Structure

```
lib/
  main.dart          # App entry point (MyApp widget)
  time_display.dart  # Time display widget (updates every second)
test/
  widget_test.dart   # Basic widget test
```

## How it works

- `main.dart` creates a `MaterialApp` with Material 3 theming (deep purple color scheme)
- `TimeDisplay` is a `StatefulWidget` that uses a `Timer.periodic` to update the time every second
- The time is displayed in `YYYY-MM-DD HH:MM:SS` format using a monospace font

## Troubleshooting

### Flutter not found
Make sure Flutter is in your PATH:
```bash
export PATH="$PATH:$HOME/flutter/bin"
```

### No devices found
- For Android: enable USB debugging on your device and connect it via USB
- For emulator: start an Android emulator from Android Studio or command line

### Build fails with SDK errors
Run `flutter doctor` to check your setup and fix any issues:
```bash
flutter doctor -v
```

### Missing Java
Install Java 17 or later. On Ubuntu/Debian:
```bash
sudo apt install openjdk-17-jdk
```

## License

MIT
