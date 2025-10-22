# Pattern Trimmer

A simple web tool for removing prefixes and suffixes from text. Built with vanilla HTML, CSS, and JavaScript - no dependencies required.

## Features

- **Real-time Processing**: See results instantly as you type
- **Prefix & Suffix Removal**: Remove unwanted text from the beginning and end of input text
- **Copy to Clipboard**: One-click copying with visual feedback
- **Character Statistics**: Track original, processed, and removed character counts
- **No Dependencies**: Pure HTML, CSS, and JavaScript - works offline

## Use Pattern Trimmer

🌐 **[Use Pattern Trimmer](https://pattern-trimmer.surge.sh)** - Online version ready to use, no installation required, no data stored in server

Alternatively, download and open `index.html` in your web browser to use the application offline.

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

**Extracting Title from Filename:**

- **Input Text**: `se-024-Class 5 Recording - Introduction to Data Flow Diagram.mp4`
- **Prefix to remove**: `se-024-` (exact match) or `se-*-` (wildcard matches any number)
- **Suffix to remove**: `.mp4`
- **Result**: `Class 5 Recording - Introduction to Data Flow Diagram`

**Batch Processing with Wildcards:**

- **Input Text**:
  ```
  se-024-Class 5 Recording - Introduction to Data Flow Diagram (Lecture).mp4
  se-025-Class 5 Recording - Data Flow Diagram Creation (Demo).mp4
  se-026-Class 5 Recording - Common Mistakes in Flow Diagrams (Lecture).mp4
  ```
- **Prefix to remove**: `se-*-` (matches `se-024-`, `se-025-`, `se-026-`)
- **Suffix to remove**: `.mp4`
- **Result**:
  ```
  Class 5 Recording - Introduction to Data Flow Diagram (Lecture)
  Class 5 Recording - Data Flow Diagram Creation (Demo)
  Class 5 Recording - Common Mistakes in Flow Diagrams (Lecture)
  ```

**Removing File Path and Extension:**

- **Input Text**: `"C:\Users\John\Downloads\document_final_version.pdf"`
- **Prefix to remove**: `"C:\Users\John\Downloads\"`
- **Suffix to remove**: `".pdf"`
- **Result**: `"document_final_version"`

## How It Works

The application supports both exact matching and wildcard patterns:

**Exact Matching:**

- Uses JavaScript's `startsWith()` and `endsWith()` methods for precise text removal
- Only removes prefix if it exists at the very beginning of the text
- Only removes suffix if it exists at the very end of the text

**Wildcard Patterns:**

- Use `*` to match any characters in your prefix or suffix patterns
- Converts wildcard patterns to regex for flexible matching
- Non-greedy matching ensures predictable results
- Preserves the original text if patterns don't match

## Browser Compatibility

- Modern browsers with ES6+ support
- Uses `navigator.clipboard` API with fallback for older browsers

## File Structure

```
.
├── index.html         # Main application file
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
