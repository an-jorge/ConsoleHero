#  Shelltint

ShellTint is your friend and will help you and your script be more beautifull.
Do you want to make your scripts more professional? ShellTint is easy to use. You will love use it come and check it

## Overview
ShellTint provides a simple way to add colored and stylized text to the terminal output in Dart. It includes a `Colours` class that allows you to define and use various text styles, colors, and background colors. The library also includes predefined color sets (`tint`) for common colors.

**Example Usage:**
- The example at the end demonstrates how to use the `tint` object to print colored text and styled messages, clear the screen, add newlines, and indent text.
- `${tint.red[0]}This is red text${tint.end()}`: Prints red text.
- `${tint.success("Operation successful")}`: Generates a success message with a specific background color.
- `${tint.clear()}`: Clears the terminal screen.
- `${tint.line(2)}`: Prints two newline characters.
- `${tint.tab(2, 'Indented Text')}`: Prints text indented with two tabs.

```dart
void main() {
  final tint = Colours(
    red: ['\x1B[31m', '\x1B[41m'],
    // ... (define other color sets)
  );

  print('${tint.red[0]}This is red text${tint.end()}');
  print('${tint.success("Operation successful")}');
  print('${tint.warning("Warning: Something went wrong")}');
  tint.clear();
  tint.line(2);
  tint.tab(2, 'Indented
```

### ANSI Escape Codes:
- **ANSI escape codes** are special sequences of characters that, when printed to a terminal, control various text formatting and color options.
- In the provided Dart code, escape codes are used for changing text color, background color, and applying styles (bold, italic, etc.).

#####  Examples:
- `\x1b[31m`: Sets text color to red.
- `\x1b[41m`: Sets background color to red.
- `\x1b[0m`: Resets all styles and colors.

### Properties
- `red`: List containing color and background color codes for red.
- `black`: List containing color and background color codes for black.
- `white`: List containing color and background color codes for white.
- `green`: List containing color and background color codes for green.
- `yellow`: List containing color and background color codes for yellow.
- `blue`: List containing color and background color codes for blue.
- `magenta`: List containing color and background color codes for magenta.
- `cyan`: List containing color and background color codes for cyan.

```dart
Colours({
  required this.red,
  required this.black,
  required this.white,
  required this.green,
  required this.yellow,
  required this.blue,
  required this.magenta,
  required this.cyan,
});

```

### Text Style Methods
- `end()`: Resets all colors and styles.
- `bold()`: Makes text bold.
- `italic()`: Renders text in italic.
- `underline()`: Underlines text.
- `strikerthrough()`: Strikes through text.

### Text Style Methods
- `end()`: Resets all colors and styles.
- `bold()`: Makes text bold.
- `italic()`: Renders text in italic.
- `underline()`: Underlines text.
- `strikerthrough()`: Strikes through text.

### Warning/Info/Success/Error Messages

- `success(String text)`: Generates a success message with a background color.
- `error(String text)`: Generates an error message with a background color.
- `warning(String text)`: Generates a warning message with a background color.
- `information(String text)`: Generates an information message with a background color.

### Screen Manipulation Methods
- `clear()`: Clears the terminal screen.
- `line(int lines)`: Outputs a specified number of newline characters.
- `tab(int tabs, String text)`: Outputs text with a specified number of leading tabs.

This library provides a convenient way to enhance terminal output with colored and stylized text. Feel free to customize the color sets and styles according to your preferences.
