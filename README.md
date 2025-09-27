# Map App (Flutter + MapLibre GL)

A minimal Flutter application that renders a MapLibre GL map centered on Tokyo Station using an OpenStreetMap Japan style.

## Features

- Map rendering with MapLibre GL
- Initial camera position centered on Tokyo Station (Tokyo, Japan)
- Pre-configured map style from OpenStreetMap Japan

## Tech Stack

- Flutter (Dart SDK constraint: ^3.6.0)
- `maplibre_gl` Flutter plugin (^0.20.0)

## Prerequisites

- Flutter SDK installed and configured
- Xcode with CocoaPods for iOS builds
- Android Studio / Android SDK for Android builds

> Note: Platform support primarily targets iOS and Android via `maplibre_gl`.

## Getting Started

1. Install dependencies:
   ```bash
   flutter pub get
   ```
2. (iOS only) Install CocoaPods dependencies:
   ```bash
   cd ios && pod install && cd -
   ```
3. Run on a device or simulator/emulator:
   ```bash
   flutter run -d ios      # iOS
   flutter run -d android  # Android
   ```

## Configuration

You can adjust the initial camera and style URL in `lib/main.dart`.

- Initial camera: latitude 35.681236, longitude 139.767125, zoom 14
- Style URL: `https://tile.openstreetmap.jp/styles/maptiler-basic-ja/style.json`

Example snippet:
```dart
MapLibreMap(
  initialCameraPosition: const CameraPosition(
    target: LatLng(35.681236, 139.767125),
    zoom: 14,
  ),
  styleString: 'https://tile.openstreetmap.jp/styles/maptiler-basic-ja/style.json',
)
```

Replace the `styleString` with your own MapLibre style URL as needed.

## Troubleshooting

- iOS build issues: ensure you have run `pod install` inside the `ios` directory.
- If using location features later, remember to add the appropriate iOS/Android permissions. (This template does not request location permissions by default.)

## Acknowledgements

- Map data and styles courtesy of the OpenStreetMap community and related providers.
- Built with the Flutter `maplibre_gl` plugin.

## License

This repository does not currently include a license file. Add one if you plan to distribute or open-source the project.
