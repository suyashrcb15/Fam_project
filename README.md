# EdgeDetectExpo-ExpoGo

An Expo Go compatible demo that *simulates* real-time edge detection by:
- letting you take or pick a photo using Expo ImagePicker,
- sending the image (base64) into a WebView,
- running OpenCV.js inside the WebView to perform Canny edge detection and display the processed image.

**Important:** This is a WebView-based approach (OpenCV.js) so **no native NDK / C++** code is used — it runs in the browser context inside the WebView. This makes the project compatible with Expo Go (no native build required).

## How to run

1. Install dependencies:
```bash
npm install
# or
yarn
```

2. Start Expo:
```bash
npm start
```

3. Open the project in **Expo Go** on your phone or use an emulator.

4. Tap "Pick or Take Photo" and allow permissions. After selecting/taking a photo the WebView will process it and show edges.

## Files of interest
- `App.js` — main Expo app (uses expo-image-picker, expo-file-system, react-native-webview)
- `assets/web/opencv_viewer.html` — web page loaded into the WebView that runs OpenCV.js and performs Canny

## Web viewer
A minimal TypeScript web viewer is included under `/web` which demonstrates displaying a static processed frame (for desktop browsers).

## ScreenShot

![UI](https://github.com/user-attachments/assets/7c6e6b98-6f57-4084-bf96-0819ecfa6217)

