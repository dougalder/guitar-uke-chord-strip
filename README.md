# Guitar and Ukulele Chord Strip

A powerful web application for adding chord diagrams to PDF sheet music and creating formatted chord charts for both guitar and ukulele.

## Overview

Guitar and Ukulele Chord Strip is a browser-based tool that helps musicians add chord fingering diagrams to their PDF sheet music or create formatted chord charts from plain text lyrics. Whether you're working with PDFs downloaded from the internet or formatting your own song lyrics, this app makes it easy to generate professional-looking chord charts with accurate fingering diagrams.

### Key Features

- **Dual Instrument Support**: Full support for both standard ukulele (GCEA) and guitar (EADGBE) tunings
- **PDF Integration**: Upload PDF sheet music and overlay chord diagrams directly onto any page
- **Chord Recognition**: Automatically detects and extracts chord names from text (handles variations like C, Cm, C#m, Cmaj7, etc.)
- **Chord Diagram Generation**: Renders accurate fingering diagrams with proper barre chord indication and fingering numbers
- **Dynamic Chord Strumming Patterns**: Browse and select from 50+ authentic strumming patterns, each with song examples
- **Sheet Building**: Create formatted PDF from plain text with automatic page reflowing
- **Per-Page Controls**: Control chord placement independently on each page of multi-page PDFs
- **Dark/Light Theme**: Toggle between themes for comfortable viewing in any lighting
- **Touch-Friendly Interface**: Large touch-enabled controls for repositioning and resizing chord diagrams
- **Text Outline Detection**: Automatically detects when PDF chord text is stored as vector outlines (not extractable) and alerts the user

## Features in Detail

### Your Song
- Paste plain text lyrics or import a PDF file
- Text is automatically analyzed for chord names
- PDF upload creates a preview of the sheet music
- Clean interface for starting your music project

### Chords Found
- View all extracted chord names with their fingering diagrams
- Diagrams show:
  - Fretboard positions (numbered strings/frets)
  - Finger placement (1=index, 2=middle, 3=ring, 4=pinky)
  - Barre chords indicated with curved line
  - Open strings marked with 'o'
  - Muted strings marked with 'x'
- Support for alternate voicings for complex chords
- Selector to choose between standard instruments or custom tunings

### Strumming Patterns
- 50+ carefully curated strumming patterns
- Each pattern includes:
  - Pattern name and rhythm
  - Song examples that use this pattern
  - Standard 4/4 time eighth-note notation
- Patterns are visually coded by rhythm feel
- Selection is saved to your session

### PDF Tab

#### Display & Stamp Mode
- Preview your PDF page-by-page
- Drag and resize the chord diagram overlay using handles (no sliders needed!)
- Large left/right navigation arrows for multi-page documents
- Per-page settings: control which pages get chords
- Checkbox for "Every page" option (applies same placement to all pages)
- Chord diagram auto-hides off-screen for better visibility
- Large touch-friendly handles for repositioning and resizing
- Save PDF with chords stamped as an overlay

#### Build a Sheet Mode
- Create a new formatted PDF from your text lyrics
- Reflowing options: fit onto 1, 2, or 3 pages
- Adjustable margins (default: 0.5 inches)
- Optional: fold chord names into lyric lines as [C] notation
- Live preview before saving
- Automatic title and artist repetition at page bottoms
- Page numbers on multi-page PDFs

## Usage

### Getting Started

1. **Open the App**: Click the button below or open `chord-strip.html` in any modern web browser
2. **Add Your Music**: 
   - Paste song lyrics with chord names, OR
   - Upload a PDF of sheet music
3. **Review Chords**: Check the "Chords Found" tab to verify extracted chord names
4. **Select Strumming**: Choose a strumming pattern from the "Strumming" tab (optional)
5. **Stamp or Build**: 
   - Use "PDF" tab to overlay chords onto your PDF, OR
   - Use "Build a Sheet" to create a formatted text-based chart

### Chord Name Format

The app recognizes standard chord notation including:
- **Basic**: C, D, E, F, G, A, B (any note letter)
- **Accidentals**: C#, Db, F# (sharp/flat notes)
- **Chord Types**: 
  - Major (C, Cmaj)
  - Minor (Cm, Cmin)
  - Diminished (Cdim, Co)
  - Augmented (Caug, C+)
  - Dominant 7th (C7, Cdom7)
  - Major 7th (Cmaj7, CM7)
  - Minor 7th (Cm7)
  - Suspended (Csus2, Csus4)
  - And many more jazz/extended voicings

### Tips & Tricks

- **Touch Interface**: Use the large handles on chord diagrams for repositioning and resizing—no need for sliders
- **Dark Mode**: Perfect for reading lyrics on a music stand at night
- **Multi-Page PDFs**: Use the left/right arrows to navigate, and set chords per-page
- **Strumming Patterns**: Each pattern has song examples to help you find the right groove
- **PDF Outline Detection**: If chord names appear outlined/pixelated in the preview, the app will suggest adding chords by hand
- **Clean Slate**: Loading a new song clears all previous settings for a fresh start

## Technology Stack

### Frontend Libraries
- **pdf.js** (v3.11.174) - PDF document reading and manipulation
- **pdf-lib** (v1.17.1) - PDF creation and modification with overlays
- **Google Fonts** (Archivo, DM Mono) - Professional typography

### Design & UX
- **Tailwind CSS** - Responsive utility-first styling
- **CSS Grid/Flexbox** - Modern layout system
- **CSS Variables** - Theme customization (light/dark mode)

### Browser APIs
- **Canvas API** - Rendering chord diagrams and sheet previews
- **LocalStorage API** - Saving user preferences
- **FileReader API** - Handling file uploads
- **Fetch API** - Loading external resources

## Compatibility

- **Browsers**: Chrome, Firefox, Safari, Edge (all modern versions)
- **PDF Support**: Readable PDFs with text layers (scanned PDFs may have limited text extraction)
- **Screen Sizes**: Fully responsive from mobile to desktop
- **Keyboard & Touch**: Full support for both input methods

## System Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- 4+ MB free disk space for browser cache
- 100+ MB free RAM for large PDF processing
- Internet connection (for Google Fonts)

## Installation & Deployment

### Local Use
1. Download `chord-strip.html`
2. Open the file directly in your web browser
3. No installation or server required!

### GitHub Pages
1. Upload all files to a GitHub repository
2. Enable GitHub Pages in repository settings
3. Access your app at `https://yourusername.github.io/repo-name/`

### Self-Hosted Server
```bash
# Simple Python server
python3 -m http.server 8000

# Node.js with http-server
npx http-server

# Or any static file server
```

## License Information

This application uses the following open-source projects:

### pdf.js
- **Version**: 3.11.174
- **License**: Apache License 2.0
- **Copyright**: Mozilla Foundation and contributors
- **Source**: https://mozilla.github.io/pdf.js/

### pdf-lib
- **Version**: 1.17.1
- **License**: MIT License
- **Copyright**: Andrew Dillon
- **Source**: https://pdf-lib.js.org/

### Google Fonts
- **Licenses**: Open Font License (OFL)
- **Fonts Used**:
  - Archivo (Multiple weights)
  - DM Mono (Multiple weights)
- **Source**: https://fonts.google.com/

### Tailwind CSS
- **License**: MIT License
- **Copyright**: Tailwind Labs Inc.
- **Source**: https://tailwindcss.com/

All licenses are included in full in the `LICENSE.md` file.

## Troubleshooting

### PDF Won't Load
- Ensure the PDF uses standard text encoding, not scanned images
- Try a different PDF file to verify compatibility
- Check browser console for error messages (F12 → Console tab)

### Chords Not Detected
- Verify chord names are spelled correctly (e.g., "Am" not "am")
- Some PDFs have chord text stored as vector outlines—the app will alert you to this
- Manual chord entry is always available via the text field

### Diagram Positioning
- Use the handles (large squares) to reposition and resize diagrams
- For precise control, drag from the center of the chord diagram
- Resize by dragging corner handles

### Strumming Pattern Not Showing
- The pattern is stored internally; refresh the page or rebuild the PDF to see it included

## Contributing

Contributions are welcome! Areas for improvement:
- Additional strumming patterns
- Support for more instruments (banjo, mandolin, etc.)
- Chord voicing database expansion
- Performance optimizations for large PDFs

## Feedback & Support

Found a bug or have a feature request? Please open an issue on GitHub.

## Author

Created with ❤️ for musicians and songwriters everywhere.

---

**Version**: 23  
**Last Updated**: October 2026  
**License**: See LICENSE.md for dependency licensing

Enjoy creating beautiful chord charts! 🎸🎵
