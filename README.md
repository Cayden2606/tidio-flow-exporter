# tidio-flow-exporter

Export Tidio chatbot flows as high-resolution SVG or PDF files with selectable text. No more screenshots.

## ✨ Features

- 📄 **Multiple formats**: Export as SVG or PDF
- 🎨 **High resolution**: Crystal-clear vector quality
- ✏️ **Selectable text**: All text remains selectable and searchable
- 🎯 **Auto-naming**: Uses your flow name automatically
- 🔧 **Two methods**: Bookmarklet or Console
- 🎨 **Style preservation**: Maintains all colors, fonts, and visual elements
- 🚫 **No screenshots needed**: Proper document export instead of lossy images

## 🚀 Installation & Usage

### Method 1: Bookmarklet (Recommended)

1. **Create the bookmarklet:**
   - Create a new bookmark in your browser
   - Name it "Export Tidio Flow"
   - Copy the entire contents of [`tidio-flow-bookmarklet.txt`](tidio-flow-bookmarklet.txt)
   - Paste it as the URL/address of the bookmark

2. **Use it:**
   - Open any Tidio flow in the Flow Editor
   - Click the bookmarklet in your bookmarks bar
   - Choose format (1 for SVG, 2 for PDF)
   - Your flow will download automatically!

### Method 2: Developer Console

1. **Open the console:**
   - Press `F12` or `Ctrl+Shift+I` (Windows/Linux)
   - Press `Cmd+Option+I` (Mac)
   - Navigate to the "Console" tab

2. **Run the script:**
   - Open any Tidio flow in the Flow Editor
   - Copy the entire contents of [`tidio-flow-export.js`](tidio-flow-export.js)
   - Paste it into the console and press Enter
   - Choose format (1 for SVG, 2 for PDF)
   - Your flow will download automatically!

## 📋 How It Works

1. **Detects** the currently open Tidio flow in your browser
2. **Extracts** the flow name from the editor
3. **Clones** the SVG with all styles and content preserved
4. **Optimizes** the viewBox to fit your flow perfectly (with 10px padding)
5. **Exports** as your chosen format:
   - **SVG**: Direct download of the vector file
   - **PDF**: Opens print dialog for "Save as PDF"

## 🎯 Why Use This?

### Problems with screenshots:
- ❌ Low resolution and pixelation
- ❌ Non-selectable text
- ❌ Poor quality when zoomed or printed
- ❌ Manual stitching required for large flows
- ❌ Inconsistent colors and styling

### Benefits of this tool:
- ✅ Perfect vector quality at any size
- ✅ Text remains selectable and searchable
- ✅ Single click export
- ✅ Professional documentation quality
- ✅ Perfect for presentations and archiving

## 🔧 Technical Details

- Preserves all CSS styles and computed properties
- Handles Tidio's dynamic class names
- Replaces background images with inline SVG icons
- Removes temporary UI elements (drag indicators, etc.)
- Calculates precise bounding box for optimal sizing
- Automatically sanitizes flow names for filenames

## 📝 File Naming

The exported file will automatically use your flow name from the Tidio editor:
- Spaces converted to hyphens
- Special characters removed
- Lowercase formatting
- Example: "Customer Support Flow" → `customer-support-flow.svg`

If no flow name is detected, defaults to `tidio-flow.svg` or `tidio-flow.pdf`

## 🌐 Browser Compatibility

Works in all modern browsers:
- ✅ Chrome/Edge
- ✅ Firefox
- ✅ Safari
- ✅ Opera

**Note for PDF export:** Allow pop-ups when prompted for the print dialog to open.

## 🐛 Troubleshooting

### "Could not find the Tidio Flow"
- Make sure you're on the Flow Editor page
- The flow must be fully loaded before exporting

### "Unable to calculate bounding box"
- Try zooming in/out slightly on the canvas
- Move the canvas view slightly
- Refresh the page and try again

### PDF not downloading
- Ensure pop-ups are allowed for the Tidio domain
- Use "Save as PDF" in the print dialog
- If issues persist, choose SVG format instead

### Styles not preserved
- Make sure all flow elements are visible on screen before exporting
- Try scrolling through the flow once before exporting

## 📄 License

MIT License - feel free to use and modify!

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## ⭐ Support

If this tool helps you, consider giving it a star on GitHub!

---

**Made with ❤️ for better Tidio documentation**
