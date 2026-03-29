# Automated PDF Generator

A web-based PDF generation system that creates personalized duty books using a fixed template design.

## Features

- **Template-based PDF Generation**: Uses your uploaded template image as a fixed background
- **Batch Processing**: Generate multiple PDFs from a simple text list
- **Individual Downloads**: Download each PDF separately
- **Combined PDF Export**: Download ONE multi-page PDF with all entries (NEW!)
- **Bulk ZIP Download**: Download all PDFs as a single ZIP file
- **Customizable Positioning**: Fine-tune text positions for perfect alignment
- **No Backend Required**: Runs entirely in the browser
- **High-Quality Output**: Maintains original resolution and layout for all export options

## How to Use

### Step 1: Upload Template Image
1. Click "Choose Template Image" button
2. Select your template image (the Student Volunteer Duty Book template)
3. Preview will appear once uploaded

### Step 2: Adjust Text Positions (Optional)
Fine-tune the following settings if needed:
- **Number Field**: Position, size, and alignment (default: top-right corner)
- **Name Field**: Position, size, and alignment (default: bottom center)

Default settings are optimized for the standard template.
![Adjustments](https://i.ibb.co/2Y6ZN74d/Screenshot-2026-03-29-191326.png)

### Step 3: Paste Names List
Enter your data in the textarea with the following format:
```
01, Kasun Perera
02, Nimal Silva
03, Ayesha Fernando
04, Chaminda Rajapakse
05, Dilini Perera
```

**Format Rules:**
- Each line = one PDF
- Format: `number, name`
- Comma-separated values
- Empty lines are automatically skipped

### Step 4: Generate PDFs
1. Click "Generate PDFs" button
2. Wait for processing to complete
3. View generated PDFs in the list below

### Step 5: Download

You have THREE download options:

**Option 1: Individual Download**
- Click "Download" button next to each PDF
- Downloads one file at a time

**Option 2: Download as Single PDF** 📄
- Click "Download as Single PDF" button
- Creates ONE multi-page PDF containing all entries
- Each student gets their own page in the combined document
- File name: "All Students.pdf"
- Perfect for printing or sharing as a single document

**Option 3: Download as ZIP** 📦
- Click "Download as ZIP" button
- All PDFs compressed into a single ZIP file
- Each student's PDF remains as a separate file
- File name: "Student_Duty_Books.zip"

## Technical Details

### Text Replacement
The system replaces only two dynamic fields:
1. **{{number}}**: Top-right position (default: 168mm, 45mm)
2. **{{name}}**: Bottom-center position (default: 105mm, 275mm)

### Fonts
- Number: Times New Roman, Bold
- Name: Times New Roman, Regular

### PDF Specifications
- Format: A4 (210mm × 297mm)
- Orientation: Portrait
- Quality: High resolution

### Combined PDF Generation
- Each record is rendered fresh (NOT merged from existing PDFs)
- Pages are appended in order during generation
- Maintains exact template layout and text positioning
- No quality loss or scaling issues
- Each entry appears on its own page

## Files

- `generator.html` - Main application file (open this in your browser)
- `README.md` - This documentation file

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for loading libraries)
- Template image file

## Libraries Used

- jsPDF 2.5.1 - PDF generation
- JSZip 3.10.1 - ZIP file creation
- FileSaver.js 2.0.5 - File download

## Browser Support

✅ Chrome 90+
✅ Firefox 88+
✅ Safari 14+
✅ Edge 90+

## Troubleshooting

**PDFs not generating?**
- Ensure template image is uploaded
- Check that input format is correct (number, name)
- Look for error messages in the status bar

**Text not aligned properly?**
- Adjust position settings in Step 2
- Try different X/Y coordinates
- Preview one PDF first before generating all

**Download not working?**
- Check browser's download settings
- Disable popup blockers
- Try a different browser

## Privacy & Security

- All processing happens in your browser
- No data is sent to any server
- Template and generated PDFs stay on your device
- No tracking or analytics

## License

This project is licensed under the GNU GPL v3 License.
![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)
