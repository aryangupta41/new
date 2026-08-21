# 🚀 Quick Start Guide - MOLECOOL Flutter

## Installation & Running (Step by Step)

### 1. Check Flutter Installation
```bash
flutter --version
```

If not installed, go to: https://flutter.dev/docs/get-started/install

### 2. Navigate to Project
```bash
cd /path/to/MOLECOOL_FLUTTER
```

### 3. Install Dependencies
```bash
flutter pub get
```

### 4. Check Connected Devices
```bash
flutter devices
```
- Should show Chrome, Android emulator, or iOS simulator

### 5. Run the App

**Option A - Chrome (Web):**
```bash
flutter run -d chrome
```

**Option B - Android:**
```bash
flutter run -d android
# or
flutter run
# (if only one device connected)
```

**Option C - iOS (Mac only):**
```bash
flutter run -d ios
```

### 6. Hot Reload
While app is running, make code changes and press:
- `r` in terminal
- Or click hot reload button in IDE

## 📱 Expected Experience

1. **5-second splash** with animated MOLECOOL title and spinning atom
2. **Mode selector** appears with two big colorful buttons:
   - 🔬 FreeLab (red/orange)
   - 📚 Learning (teal/green)
3. **Learning Mode**:
   - 5 colorful lessons with big emojis
   - Progress dots at bottom
   - After lesson 5, automatically goes to FreeLab
4. **FreeLab Mode**:
   - Left: Periodic table (scrollable, color-coded)
   - Center: 3D canvas (just 2D for now)
   - Right: Molecule info panel
   - Bottom: Control buttons
5. **Try it**:
   - Click Hydrogen (H) in periodic table
   - Tap canvas twice to add 2 H atoms
   - Click Oxygen (O) in table
   - Tap canvas to add O atom
   - Tap a H atom, then tap O atom
   - Bond appears! Check info panel for formula H₂O

## 🐛 Troubleshooting

### Issue: `flutter` command not found
**Fix**: Add Flutter to PATH or restart terminal

### Issue: No devices available
**Fix**:
- Chrome: Make sure Chrome browser is installed
- Android: Start Android Studio > AVD Manager > Create Virtual Device
- iOS: Open Xcode > Window > Devices and Simulators

### Issue: `pub get` fails
**Fix**:
```bash
flutter clean
flutter pub get
```

### Issue: App crashes on start
**Fix**:
- Check Flutter doctor: `flutter doctor`
- Ensure Dart SDK is compatible (≥3.0.0)
- Make sure all dependencies are correctly listed

### Issue: Hot reload not working
**Fix**:
- Make sure app is running in debug mode (not release)
- Use `flutter run` not `flutter run --release`

## 🎯 Testing Checklist

- [ ] Splash screen shows and lasts 5 seconds
- [ ] Mode selector displays both buttons
- [ ] Learning mode shows all 5 lessons
- [ ] Can navigate through lessons
- [ ] After lesson 5, enters FreeLab
- [ ] Periodic table displays and is scrollable
- [ ] Can select element by tapping
- [ ] Atom appears on canvas when element selected and tapped
- [ ] Atom has cute face (^_^)
- [ ] Can select one atom, then another to bond
- [ ] Bonds draw correctly (single/double/triple)
- [ ] Info panel updates in real-time
- [ ] Formula shows subscripts (H₂O)
- [ ] Stability rating shows
- [ ] Undo button works
- [ ] Clear button removes all atoms/bonds
- [ ] Back button returns to mode selector

## 🎨 Customization Tips

### Change colors:
Edit `lib/screens/splash_screen.dart` and other screens' Container decorations

### Add more elements:
Edit `lib/utils/elements_data.dart` and add to `getElements()` list

### Change splash duration:
In `lib/screens/splash_screen.dart`, line 30:
```dart
Future.delayed(const Duration(seconds: 5), () {
```
Change `5` to desired seconds

### Add more lessons:
In `lib/screens/learning_screen.dart`, add to `lessons` list

### Change gemini rate:
In `lib/providers/molecule_provider.dart`, adjust stability calculation

## 📦 Building for Release

### Android APK:
```bash
flutter build apk --release
```
APK located at: `build/app/outputs/flutter-apk/app-release.apk`

### Android App Bundle (for Play Store):
```bash
flutter build appbundle --release
```

### Web:
```bash
flutter build web --release
```
Files in `build/web/` - host on any web server

### iOS (Mac only):
```bash
flutter build ios --release
```
Then use Xcode to archive and upload to App Store

## 📊 Project Stats

- **Total Files**: ~20 Dart files
- **Lines of Code**: ~2,500+
- **Widgets**: 15+ custom widgets
- **Screens**: 4 main screens
- **Animations**: 10+ animated elements
- **Dependencies**: 4 packages
- **Estimated Size**: ~15 MB (APK)

## 🤝 Contributing

Want to improve MOLECOOL? Here are ideas:

1. Implement true 3D with `three_dart` or `flutter_3d_obj`
2. Add drag-to-move atoms feature
3. Create delete mode button
4. Expand periodic table to all 118 elements
5. Add bond validation (only allow valid bonds)
6. Create challenge/quiz mode
7. Add particle effects on bond creation
8. Implement save/load functionality
9. Add sound effects
10. Create molecule rotation controls

---

**Happy building!** 🧪✨

Need help? Check README.md for detailed documentation.