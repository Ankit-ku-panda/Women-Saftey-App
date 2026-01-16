👩‍🦺 Women-Saftey-App 🚨

A mobile Women Safety Android Application built using modern Android development principles.
This app aims to help users feel more secure by providing essential safety tools such as emergency alerts, location sharing, and help-trigger mechanisms.

📌 About the Project

This application provides features such as:

✅ Emergency SOS alerts
✅ Sending distress information to trusted contacts
✅ Live location sharing
✅ Panic button activation
✅ Guardian management (optional)

The design and logic follow typical safety app implementations seen in other Women Safety applications available publicly.

📂 Expected Project Structure

Your Android project likely contains:

Women-Saftey-App/
├── WomenSafetyApp/            # Android application module
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/…         # Kotlin/Java source files
│   │   │   ├── res/…          # Layouts, drawables, strings
│   │   │   └── AndroidManifest.xml
├── build.gradle
├── gradlew
├── gradlew.bat
├── settings.gradle
├── local.properties
└── README.md

🔧 Key Features (Typical)

✔ Panic Button to send emergency alerts
✔ Real-time GPS location share via SMS or messaging
✔ Guardian contacts list
✔ Map view for location reference
✔ Optional Firebase/Auth features
✔ Navigation drawer user interface

(You can update this list with your actual features after inspecting your code.)

🚀 How to Run (Android)

Clone the repository

git clone https://github.com/Ankit-ku-panda/Women-Saftey-App.git


Open in Android Studio

File → Open → Select project root

Build the project

Wait for Gradle sync

Install missing SDKs if prompted

Run on device/emulator

Enable location & SMS permissions

Configure any API keys as needed

⚠️ Common Issues & Fixes

Below are typical problems encountered in women safety Android apps and solutions you can apply.

❌ 1. Compilation Errors

Cause: Missing dependencies, Gradle sync failures

Fix:

Open build.gradle and make sure all AndroidX and support libraries are consistent.

Update SDK and tools in Android Studio

❌ 2. Missing Permissions (Location/SMS)

Effect: App crashes or location doesn’t work

Required Permissions Example

<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>
<uses-permission android:name="android.permission.SEND_SMS"/>
<uses-permission android:name="android.permission.RECEIVE_SMS"/>


Fix:
Add these in AndroidManifest.xml and request them at runtime before using.

❌ 3. Location Not Working / Null Location

Cause: Using deprecated location APIs

Fix:
Use FusedLocationProviderClient (recommended modern approach)
Make sure location permissions are granted before fetching.

❌ 4. SMS Not Sent

Cause: Missing SEND_SMS permission at runtime
Fix:

ActivityCompat.requestPermissions(this, arrayOf(Manifest.permission.SEND_SMS), REQUEST_CODE)

❌ 5. Map Not Showing

Cause: Google Maps API key not configured

Fix:

Enable Google Maps API in Google Cloud Console

Add google_maps_api.xml with your API key

Ensure you have billing enabled for Maps API

🧠 Tips to Improve Your App

✔ Validate phone numbers before sending SMS
✔ Add Offline support — queue SMS/messages when network unavailable
✔ Protect API keys using secure storage
✔ Add shake detection or power button triggers for SOS
✔ Add Firebase authentication for user accounts

📌 Recommended Libraries
Purpose	Library
Location	FusedLocationProvider
Maps	Google Maps Android SDK
Local Database	Room
UI	Material Components
💡 Contribution & Next Steps

Want to contribute?

Fork the repo

Fix bugs or add features

Create a pull request

You can also:
✔ Add automated tests
✔ Publish on Play Store
✔ Add backend for alerts

🎓 Learnings

This project teaches:
✔ Handling runtime permissions
✔ Working with Google APIs
✔ Handling device sensors for SOS
✔ Designing intuitive UI/UX
