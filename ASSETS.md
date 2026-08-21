# Assets Directory Structure

This directory would contain image assets, data files, and fonts for MOLECOOL.

## Current Assets (Not Yet Added)

- `data/elements.json` - Full 118-element database (currently hardcoded in `lib/utils/elements_data.dart`)
- `images/` - Additional illustrations
  - Splash screen background variations
  - Atom/chemistry icons
  - Lesson illustrations
- `fonts/` - Custom cute fonts
  - `CuteFont-Regular.ttf`
  - `BubbleGum.ttf`

## To Add Assets

1. Place files in the `assets/` directory
2. Update `pubspec.yaml`:
   ```yaml
   flutter:
     assets:
       - assets/data/elements.json
       - assets/images/
       - assets/fonts/
   ```
3. Load assets in code:
   ```dart
   // For JSON
   final data = await rootBundle.loadString('assets/data/elements.json');

   // For images
   final image = Image.asset('assets/images/atom.png');

   // For fonts
   ThemeData(fontFamily: 'CuteFont')
   ```

## Optional: SVG Icons

Consider adding vector icons:
- `atom.svg`
- `molecule.svg`
- `periodic_table.svg`
- `flask.svg`

Use `flutter_svg` package to render SVGs.