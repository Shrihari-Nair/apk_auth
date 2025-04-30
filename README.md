# YouTube OAuth Android App

A simple Android application that demonstrates YouTube OAuth authentication with full account access capabilities.

## Features

- Single-button interface for easy authentication
- Full YouTube account access including:
  - Channel subscriptions
  - Video uploads
  - Playlist management
  - Channel memberships
  - Comment interactions
  - And other YouTube account actions

## Prerequisites

- Android Studio (latest version recommended)
- Android device running Android 5.0 (API level 21) or higher
- Google account with YouTube access
- Google Cloud Project with YouTube Data API v3 enabled

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone [repository-url]
   ```

2. **Set up Google Cloud Project**
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project
   - Enable YouTube Data API v3
   - Create OAuth 2.0 Client ID for Android
   - Add your app's SHA-1 fingerprint
   - Download `google-services.json` and place it in `app/` directory

3. **Get SHA-1 Fingerprint**
   ```bash
   keytool -list -v -keystore ~/.android/debug.keystore -alias androiddebugkey -storepass android -keypass android
   ```

4. **Build the Project**
   - Open the project in Android Studio
   - Wait for Gradle sync to complete
   - Click Build > Build Bundle(s) / APK(s) > Build APK(s)

## Installation

1. **Enable Developer Options on your Android device**
   - Go to Settings > About phone
   - Tap "Build number" 7 times
   - Go back to Settings > System > Developer options
   - Enable "USB debugging"

2. **Install the APK**
   - Connect your device to your computer
   - Copy the APK from `app/build/outputs/apk/debug/app-debug.apk` to your device
   - Install the APK on your device

## Usage

1. Launch the app
2. Tap the "Connect to YouTube" button
3. Sign in with your Google account
4. Grant the requested permissions
5. You're now authenticated and can perform YouTube actions

## Project Structure

```
app/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/example/youtubeoauth/
│   │   │       └── MainActivity.kt
│   │   ├── res/
│   │   │   └── layout/
│   │   │       └── activity_main.xml
│   │   └── AndroidManifest.xml
│   └── build.gradle
└── google-services.json
```

## Dependencies

- AndroidX Core
- AndroidX AppCompat
- Material Design
- Google Play Services Auth
- Google API Client
- YouTube Data API v3

## Troubleshooting

1. **Authentication Failed**
   - Check your internet connection
   - Verify SHA-1 fingerprint in Google Cloud Console
   - Ensure YouTube API is enabled
   - Check package name matches exactly

2. **Build Errors**
   - Clean and rebuild project
   - Check Android Studio version compatibility
   - Verify all dependencies are properly synced

## Contributing

Feel free to submit issues and enhancement requests.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Google YouTube Data API
- Android OAuth implementation
- Google Sign-In for Android 