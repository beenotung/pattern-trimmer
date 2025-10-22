# Trim String

A simple web tool for removing prefixes and suffixes from text strings. Built with vanilla HTML, CSS, and JavaScript - no dependencies required.

## Features

- **Real-time Processing**: See results instantly as you type
- **Prefix & Suffix Removal**: Remove unwanted text from the beginning and end of strings
- **Copy to Clipboard**: One-click copying with visual feedback
- **Character Statistics**: Track original, processed, and removed character counts
- **No Dependencies**: Pure HTML, CSS, and JavaScript - works offline

## Live Demo

Simply open `index.html` in your web browser to use the application.

## Usage

1. **Enter your text** in the main textarea
2. **Specify prefix/suffix** to remove in the respective input fields
3. **View the processed result** in the output area
4. **Copy to clipboard** with the copy button
5. **Monitor statistics** to see how much text was removed

### Examples

**Basic Text Processing:**

- **Input Text**: `"Hello World!"`
- **Prefix to remove**: `"Hello "`
- **Suffix to remove**: `"!"`
- **Result**: `"World"`

**Extracting Video Title from Filename:**

- **Input Text**: `"/home/user/videos/2023-12-25_Christmas_Vacation_Family_Reunion.mp4"`
- **Prefix to remove**: `"/home/user/videos/2023-12-25_"`
- **Suffix to remove**: `".mp4"`
- **Result**: `"Christmas_Vacation_Family_Reunion"`

**Removing File Path and Extension:**

- **Input Text**: `"C:\Users\John\Downloads\document_final_version.pdf"`
- **Prefix to remove**: `"C:\Users\John\Downloads\"`
- **Suffix to remove**: `".pdf"`
- **Result**: `"document_final_version"`

## How It Works

The application uses JavaScript's `startsWith()` and `endsWith()` methods to safely remove prefixes and suffixes:

- Only removes prefix if it exists at the very beginning of the text
- Only removes suffix if it exists at the very end of the text
- Preserves the original text if prefix/suffix don't match exactly

## Browser Compatibility

- Modern browsers with ES6+ support
- Uses `navigator.clipboard` API with fallback for older browsers

## File Structure

```
trim-string/
├── index.html          # Main application file
├── README.md          # This file
└── LICENSE            # BSD-2-Clause license
```

## Development

This is a single-file application. To modify or extend:

1. Edit `index.html` directly
2. All styles are in the `<style>` section
3. All JavaScript is in the `<script>` section
4. No build process required

## License

This project is licensed with [BSD-2-Clause](./LICENSE)

This is free, libre, and open-source software. It comes down to four essential freedoms [[ref]](https://seirdy.one/2021/01/27/whatsapp-and-the-domestication-of-users.html#fnref:2):

- The freedom to run the program as you wish, for any purpose
- The freedom to study how the program works, and change it so it does your computing as you wish
- The freedom to redistribute copies so you can help others
- The freedom to distribute copies of your modified versions to others
