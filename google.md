slidenumbers: true
build-lists: true

# What's new in the Google Developer World 

### 2018

---

# Most Important Topics
* Android 9 Security Enhancements
* Android App Bundle
* Kotlin
* Jetpack
* Flutter

<!--
---

# Android 9 Pie
* Gestures
* Wind down & Do Not disturb
* Digital Well Being - Beta
* Adaptive Battery, Brightness
* App Actions
* Slices

![right](android-9-pie.png)

^ Adaptive Battery: ML to prioritize access to resources 
  "App Standby buckets" "active" ... "rare".

-->

<!--
---

![](gestures.gif)

---

![](app-actions.gif)
-->

---

# Security Enhancements

* Android biometric prompt
* KeyStore Type `StrongBox`
* Import Keys ASN.1-encoded
* Encrypted Android Backups
* Privacy enhancements 

![right](biometric-prompt.png)

^ Trusted Execution Environment: CPU, Storage, RNG
^ Key never in device hosts memory
  https://developer.android.com/training/articles/keystore
^ Privacy: Access to sensors in background is restricted

---

# APK Key Rotation

* `APK Signature Scheme v3`
* Requires Android 9

^ Finally! Helps when signing key lost/stolen
^ Signature Scheme: v1 - sign JAR, v2 sign metadata (Android 7.0), v3 APK Signer Lineage
^ Proof-of-rotaton: history of signing certificates with each ancestor attesting to the validity of its descendant
  https://www.xda-developers.com/apk-signature-scheme-v3-key-rotation/

---

# Android Protected Confirmation

* Prompt user to confirm statement
  `ConfirmationPrompt`
* Runs in Trusted Execution Environment
* Requires Pixel 3 Device

^ TEE: CPU, Storage, True RNG, Tampering
^ Prompt user to confirm statement - signs statement cryptographically
^ Extra data - cryptographic nonce (replay attacks)
^ https://developer.android.com/training/articles/keystore

---

# Android App Bundle


![right fit](android-app-bundle.png)

^ APK - Android Package Format

---

# Android App Bundle
* Upload single artifact, download device specific APK
* Dynamic Delivery – On demand app features
* Smaller download size (~20% savings)


---

# App Bundle Details
* Manifest/Resources -> Protobuf
* Split APK per
  * CPU Architecture
  * Screen Density
  * Language

![right fit](aab-splits.png)

---

# App Bundle – Requirements
* Android Lollipop 5.0
* Android Studio 3.2
* App signing by Google Play

^ [](https://developer.android.com/guide/app-bundle/)
^ [](https://developer.android.com/platform/technology/app-bundle/)
^ [](https://medium.com/google-developer-experts/exploring-the-android-app-bundle-ca16846fa3d7)
^ [](https://support.google.com/googleplay/android-developer/answer/7384423?hl=en)

---

# Kotlin
## No news

* Video Tipp - Jake Wharton


![right fit](https://www.youtube.com/watch?v=st1XVfkDWqk)

---

# Android KTX
## Extensions for Kotlin

* API Kotlinification
* No __code golf__ API

^ Mostly Syntactical Sugar. Kotlinfication.
  https://www.youtube.com/watch?v=st1XVfkDWqk
^ Part of Jetpack

---

# Android Jetpack

*Rebranded Support Library*

* __Foundation__: Android KTX
* __Architecture__: Data Binding, Room, ViewModel, Navigation ...
* __Behaviour__: Notifications, Slices, ...
* __UI__: Animations, Emoji, Layouts, ...

^ [Jetpack](http://developer.android.com/jetpack)
^ [Architecture Components](https://developer.android.com/topic/libraries/architecture/)
^ Rebranding of existing tools: Support Library. New Namespace androidx

^ Foundation: Android KTX
^ Architecture: Data Binding, Lifecycles, Paging, Room, ViewModel, WorkManager
^ Behaviour: Notifications, Permissions, Slices
^ UI: Animations, Emoji, Layout

---

# Jetpack Navigation

* Managed Navigation
  * Pass data type-safe
  * Transition Animations
* Visual navigation editor

![right](navigation-editor.png)

^ The Navigation Architecture simplifies the implementation of navigation between destinations in an app.
^ Types: Fragments, Activities, Navigation graphs
^ Principles: Start, Stack, Up Button never exits, up == back, deep linking
^ https://developer.android.com/topic/libraries/architecture/navigation/navigation-implementing#Create-transition
^ Android Studio 3.2

---

<!--
# Jetpack – Announcements

  * App Actions
  * Slices
--->

# Flutter
## Release Preview 2

^ Release Preview 2 - 19. Sep 2018
  Live December 4th 2018
^ Googles new Hybrid App Platform

![right](flutter.png)

---

# Flutter

* Efficient, Native UI, Native Performance
* Stateful Hot Reload
* Widget Library
* Dart 2, compiles to native code
* Access native SDKs and Services
* Navigation, Testing, State Management

[](https://www.youtube.com/watch?v=fq4N0hgOWzU&vl=en)
[](https://medium.com/dartlang/dart-2-stable-and-the-dart-web-platform-3775d5f8eac7)
[](https://flutter.io/widgets/)

^ Mobile App SDK for Android & iOS
^ Not based on web technologies. Single codebase, two platforms.
^ Reloads like React Native! Highly productive!
^ CSS style UI
^ Built-in iOS/Material Design & Widgets, State Management
^ More Features than React Native! Complete Set for App. No Third Party Libs necessary.
^ gemischte Erfahrungen: Hackathon-Team: Orlando, Fabian, Jonas, Yves
  IDE, Hot Reloading, Widgets


<!--
---

![fit](flutter-hot-reload.gif)
--->


---

# Announcements

* Google Duplex - Demo
* Wi-Fi RTT Indoor positioning - Demo
* Android Things
* ML on Android

^ Wi-Fi RTT

---

# Google Duplex – Demo

AI driven phone-calls

![inline](https://youtu.be/TO6E-qTk1w4)

^ Technology for natural conversations to carry out “real world” tasks over the phone
^ Google I/O Demo https://youtu.be/bd1mEm2Fy08?t=1m9s
^ Available on Pixel 3 in 2018
	
---

# Wi-Fi RTT – Demo

Indoor Positioning: Distance to Access Point

![inline](https://youtu.be/vywGgSrGODU?list=PLWz5rJ2EKKc9Gq6FEnSXClhYkWAStbwlC&t=340)

^ measure distance to supporting Access Points and peer devices.
^ play until 6:15
^ https://developer.android.com/reference/android/net/wifi/rtt/WifiRttManager
^ https://medium.com/@rafaelmiguel.ortega/android-p-first-taste-of-rtt-support-febefb679775

---

# Android Things

* IoT optimized Android OS 
* Fully Managed Device
* Certified Managed Hardware
* Google Services

![right](android-things.png)

^ IoT: Internet of Things
^ 50% smaller android distribution
^ Management Console
^ Automatic Updates
^ https://androidthings.withgoogle.com
^ https://www.youtube.com/watch?v=e_PI_Npb3-U

---

<!--

# Android Go Edition

* Runs on 8GB ROM
* Data Saver
* Peer-to-Peer Sharing

^ https://www.android.com/versions/go-edition/

---
-->

# ML on Android

* Neural Networks API
  C API
* TensorFlowLite
  C++ API, Java Wrapper
* ML Kit (Firebase)
  On-device & Cloud Features
* Google Cloud ML Services $$$

![right](mlkit.png)

^ Neural Networks API - Part of NDK
  https://developer.android.com/ndk/guides/neuralnetworks/
^ TFLite: Mobile & IoT. Run trained models with low latency on device
  https://www.tensorflow.org/lite/
^ ML Kit
  https://developers.google.com/ml-kit/
  Image Labeling, Text Recognitition (OCR), Face Detection, Barcode Scanning, Landmark detection

<!--
---

# TensorFlowLite

* Android, iOS, IoT Devices
* Requires Android NDK
* Convert models

![right fit](tflite.png)

^ https://www.tensorflow.org/lite/
^ TF->CoreML Converter
  https://github.com/tf-coreml/tf-coreml
---
-->

<!--
# Google AR Core

https://developers.google.com/ar/discover/
https://developers.google.com/ar/develop/
---
-->

<!--
# Google Cloud ML Services $$$

* Vision API
* Speech-to-Text
* Text-to-Speech

  Many more...

^ https://cloud.google.com/products/ai/
-->

---

# The Google Ecosystem

* Android, Android Go, Android Auto, Android Things
* Chrome OS
* Wear OS
* TV OS
* Google Cloud Services

![right fit](google-world.png)

---

# Questions?
## `else goto Pieter`
