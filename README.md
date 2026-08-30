# MOLECOOL 🧪

A fun, colorful, and cute 3D molecule builder built with Flutter!!!
A fun, colorful, and cute 3D molecule builder built with Flutter!!!
A fun, colorful, and cute 3D molecule builder built with Flutter!!!
A fun, colorful, and cute 3D molecule builder built with Flutter!!!

## ✨ Features

### 🎬 **Splash Screen**
- 5-second animated intro with bouncing "MOLECOOL" title
- Spinning atom emoji ⚛️
- Gradient background with multiple colors
- Loading progress bar
- Smooth fade transition

### 🎮 **Two Main Modes**

#### 🔬 **FreeLab Mode**
- Build molecules freely using the periodic table
- 3D canvas with orbit controls (rotate, zoom, pan)
- Place atoms by selecting element and tapping
- Create bonds (single, double, triple) by selecting atoms
- Drag atoms to reposition them
- Real-time molecule info:
  - Molecular formula
  - Total mass (atomic mass units)
  - Atom & bond counts
  - Stability rating (⭐ Perfect / ✅ Stable / ⚠️ Fair / ❌ Unstable)
  - Predictions: state (gas/liquid/solid) and polarity

#### 📚 **Learning Mode**
- 5 interactive lessons teaching chemistry basics:
  1. Welcome to MOLECOOL!
  2. What are Atoms?
  3. The Periodic Table
  4. What are Molecules?
  5. Let's Build Together!
- Each lesson has emoji, colorful content, and friendly tone
- Progress indicators (dots)
- Automatic transition to FreeLab after completion

### 🎨 **Cute & Colorful Design**
- Rainbow gradient backgrounds
- Rounded UI elements with soft shadows
- Playful fonts and vibrant colors
- Smooth animations throughout
- Atom faces (^_^) that smile at you!
- Cute particle effects
- Responsive controls

### 🎯 **Interactive Features**
- Cute emojis everywhere
- Pop-up elements on hover
- Pulsing selections
- Floating animations
- Glassmorphism UI panels
- Smooth mode transitions

## 📱 Platforms

- 🖥️ Android
- 🍎 iOS
- 💻 Web
- 🪟 Windows (coming soon)
- 🐧 Linux (coming soon)
- 🍎 macOS (coming soon)

## 🚀 Getting Started

### Prerequisites

- Flutter SDK 3.0.0 or higher
- Dart SDK 3.0.0 or higher
- Android Studio / VS Code (recommended)
- Chrome (for web testing)

### Installation

1. Clone or download this repository
2. Install dependencies:
   ```bash
   flutter pub get
   ```

3. Run the app:
   ```bash
   # On connected device/emulator
   flutter run

   # Or for web
   flutter run -d chrome

   # Or for iOS
   flutter run -d ios

   # Or for Android
   flutter run -d android
   ```

4. Build for production:
   ```bash
   # APK for Android
   flutter build apk

   # App Bundle
   flutter build appbundle

   # Web
   flutter build web

   # iOS (requires Mac)
   flutter build ios
   ```

## 🎮 How to Use

### **Starting the App**

1. **Splash Screen** - Wait 5 seconds for animated intro
2. **Mode Selection** - Choose FreeLab or Learning mode

### **FreeLab Mode**

1. **Select an Element**
   - Click any element in the periodic table
   - The selected element appears in the top-left preview

2. **Place Atoms**
   - With element selected, tap on the 3D canvas
   - A cute atom with a face appears!
   - Atom floats gently up and down

3. **Create Bonds**
   - Tap an atom to select it (glowing highlight)
   - Tap another atom to create a bond
   - Choose bond type (single/double/triple) with buttons
   - See sparkle effect when bond forms!

4. **Move Atoms**
   - Tap and drag atoms to reposition
   - Connected bonds follow automatically

5. **Delete**
   - No delete mode currently (being developed)
   - Use Clear button to reset everything

6. **Explore Info**
   - See molecular formula with subscripts
   - Watch mass, atom/bond counts update
   - Check stability rating (based on octet rule)
   - View predicted properties

7. **Controls**
   - 🔄 Undo - Removes last atom or bond
   - 🗑️ Clear - Start fresh
   - Orbital camera: rotate (drag), zoom (scroll), pan (right drag)

### **Learning Mode**

1. Tap **📚 Learning** on mode selector
2. Read each lesson:
   - Big emoji illustration
   - Fun, friendly explanation
   - Chemistry concepts for beginners
3. Tap button to continue to next lesson
4. After lesson 5, automatically enters FreeLab to practice!
5. Progress dots show which lesson you're on

## 📊 Technical Details

### **Architecture**
- **State Management**: Provider pattern
- **UI Framework**: Flutter Material 3
- **Rendering**: CustomPaint for 2D molecule visualization
- **Animations**: Implicit and explicit animations with TweenAnimationBuilder

### **Project Structure**
```
lib/
├── main.dart                    # App entry point
├── models/
│   ├── atom.dart               # Atom data model
│   ├── bond.dart               # Bond data model
│   └── element.dart            # Element data model
├── providers/
│   └── molecule_provider.dart  # State management
├── screens/
│   ├── splash_screen.dart      # 5-sec animated splash
│   ├── mode_selector.dart      # Choose FreeLab/Learning
│   ├── freelab_screen.dart     # Main builder interface
│   └── learning_screen.dart    # Tutorial lessons
├── utils/
│   └── elements_data.dart      # Periodic table data
└── widgets/
    ├── periodic_table.dart     # Interactive periodic table grid
    ├── molecule_viewer.dart    # Canvas for building molecules
    ├── molecule_info.dart      # Info panel showing molecule stats
    └── control_buttons.dart    # Add/Bond/Undo/Clear buttons
```

### **Key Components**

**MoleculeProvider** (State Management)
- Manages atoms, bonds, selected element/atom
- Calculates molecular formula, mass, stability
- Handles add/delete/bond operations
- Provides atom lookup by ID

**MoleculeViewer** (Canvas)
- CustomPaint widget for drawing
- Converts 2D canvas coordinates to centered system
- Handles tap detection for atom selection
- Draws bonds (single/double/triple) as cylindrical lines
- Draws atoms with colors and cute faces

**PeriodicTableWidget**
- Grid layout (18 columns)
- Color-coded element categories
- Hover/select animations
- Displays atomic number, symbol, mass

### **Chemistry Engine**

**Stability Calculation**
- Checks octet rule compliance
- Compares actual bonds vs valence
- Score: 0-100% based on deviation
- Categories: Perfect (≥90%), Stable (≥70%), Fair (≥40%), Unstable (<40%)

**Polarity Prediction**
- Based on average electronegativity
  - <1.7: Nonpolar
  - 1.7-2.5: Slightly Polar
  - ≥2.5: Polar

**State Prediction**
- Based on total molecular mass:
  - <20 u: Gas
  - 20-100 u: Liquid
  - >100 u: Solid

## 🎨 Design System

- **Primary Colors**: Purple/indigo (#667eea to #764ba2)
- **Secondary Colors**: Teal/cyan (#4ecdc4 to #44a08d)
- **Accent Colors**: Rainbow gradients for backgrounds
- **Neutral**: Whites, greys, soft shadows
- **Typography**: Comic Sans MS (playful/bubble font)
- **Border Radius**: 20-30px (soft rounded)
- **Shadows**: Multi-layer with blur and spread
- **Animations**: Elastic, bounce, ease-out curves

## 📦 Dependencies

```yaml
dependencies:
  flutter:
    sdk: flutter
  provider: ^6.0.0        # State management
  animations: ^2.0.0      # Additional animations
  cupertino_icons: ^1.0.0 # iOS-style icons
  vector_math: ^2.1.4     # Math utilities

dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^3.0.0   # Linting rules
```

## 🧪 Future Enhancements

- [ ] 3D rendering with `flutter_3d_obj` or `three_dart`
- [ ] Save/Load molecule files
- [ ] Share molecules as images
- [ ] More interactive tutorials
- [ ] Challenge mode with quiz and levels
- [ ] Bond validation (correct connectivity)
- [ ] Molecule rotation in 3D space
- [ ] More elements (expand periodic table)
- [ ] Sound effects and music
- [ ] Achievement badges
- [ ] Leaderboard for challenge mode
- [ ] Dark mode toggle
- [ ] Multi-language support

## 🐛 Known Limitations

- Only has a subset of elements (common ones)
- Drag-to-move atoms not fully implemented yet
- No delete individual atom button (use Clear)
- Canvas is 2D (not true 3D, though positions are 2D offsets)
- Bond validation is simple (no chemistry rules)
- Stability calculation simplified

## 📖 Educational Value

Perfect for:
- Middle school chemistry
- High school science
- Homeschooling
- Chemistry hobbyists
- Anyone who wants to learn molecular structure

Teaches:
- Periodic table navigation
- Element symbols and properties
- Chemical bonding basics
- Molecular geometry concepts
- Octet rule
- Valence electrons
- Molecular formula notation

## 🎉 Credits

Built with ❤️ using Flutter!

Inspired by the joy of chemistry and the curiosity of young scientists everywhere.

## 📄 License

MIT License - feel free to use, modify, and share!

---

**Enjoy building molecules!** 🧪✨

Made with Flutter 🦋
