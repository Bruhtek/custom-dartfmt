# Custom dartfmt / dart format / flutter format
A quick and (relatively) easy tutorial on how to use a customised dart formatter in your dart/flutter project!

**Currently works only in VSCode**

## What you'll need:
- VSCode editor
- A dart/flutter project
- [This extension](https://marketplace.visualstudio.com/items?itemName=emeraldwalk.RunOnSave), or if it's no longer available, any kind of Run-On-Save extension will do, you'll just have to customize the [.vscode/settings.json](.vscode/settings.json) file for it.

## What you need to do:
- Clone the https://github.com/dart-lang/dart_style to your pc
- Make edits to whatever you need. (A good idea is to search commits, since then you will just need to revert the changes)
- Compile it using `dart compile exe bin/format.dart` - it will produce an `format.exe` file in the `bin` folder.
- Move the `format.exe` file to your project directory in the `.vscode` folder, and rename it to `dartfmt.exe`
- Copy the settings from [.vscode/settings.json](.vscode/settings.json) to your files, and edit it to your preferences. **(Remember: the number after `-l` in the 7th line is the max line length)**
- Check whether the Dart SDK compiler is disabled in VSCode settings!
- You're ready to go!

## Additional notes:
- I needed it to stop forcing a blank line after functions, so I went and found [this](https://github.com/dart-lang/dart_style/commit/8b5aa7e9d090def190d4ae44a21c9d689928935f) commit, and forced the needsDouble variables to false. 
- Yes, I know the current method is a bit janky, but simply writing to the same file creates endless problems, and I couldn't find any better method. If you find one, feel free to share it!
