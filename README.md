# JSON to CSV Converter

## Overview
A simple web tool to convert JSON files to CSV format. Easily upload and convert your JSON data for analysis and record-keeping.

## Features
- Drag-and-drop file upload
- Batch processing of multiple files
- Instant CSV download upon conversion
- Error handling during file reading and conversion

## Usage
1. **Upload Files**:
   - Drag and drop JSON files into the designated area.
   - Or click to select files via the file dialog.
2. **View Files**:
   - Uploaded files will be listed with their names and sizes.
3. **Convert**:
   - Click "Convert and Download CSV" to start the conversion.
   - Conversion status will be displayed below the button.
4. **Download**:
   - Converted files will be automatically downloaded as CSV.

## Notes
- Ensure files are in valid JSON format.
- Large files may take longer to convert.
- Compatible with modern browsers only.

## Technical Details
- **Frontend**: HTML, CSS, JavaScript
- **Core Function**: `JSON2CSV` for converting JSON arrays to CSV strings.
- **File Handling**: `FileReader` API, `Blob`, and `URL.createObjectURL`.

## Feedback & Support
For issues or assistance, contact us via [feedback channel](#).

## License
MIT License - see LICENSE file for details.

---
Replace `[feedback channel](#)` with the actual feedback link and ensure the LICENSE file is available for the users. This README is concise and provides essential information for users to understand and use the tool effectively.
