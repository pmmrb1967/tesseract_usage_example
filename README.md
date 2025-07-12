# PDF Scanned Data to Excel Extractor

This Jupyter Notebook demonstrates how to use **Tesseract OCR** to extract structured data from scanned PDF documents with a predefined layout and export it to Excel.

## ⚠️ Important Requirements

1. **PDF Type**: Works ONLY with **scanned/image-based PDFs** (no selectable text)
2. **Layout**: PDFs **must match** [this exact layout](reference_layout.png)  
   (Agent blocks must appear in specific positions for proper extraction)
3. **Output**: Generates an Excel file with structured agent data

## 📋 Features

- Extracts: Agent Name, Firm, Address, Contact Info, etc.
- Processes multiple pages
- Handles common OCR challenges in scanned documents
- Exports clean structured data to Excel

## 🛠️ Libraries Used

- `pytesseract` (Tesseract OCR engine)
- `pdf2image` (PDF to image conversion)
- `Pillow` (Image processing)
- `pandas` (Data structuring & Excel export)

## ⚙️ Setup

1. Install Tesseract OCR:
   ```bash
   # Windows (download installer): https://github.com/UB-Mannheim/tesseract/wiki
   # Mac: brew install tesseract
   # Linux: sudo apt install tesseract-ocr

2. Install Python dependencies:
   ```bash
   pip install pytesseract pdf2image pandas pillow

3. Place your scanned PDFs in the /Input folder

## � Demo Files

For testing, we've included:
- `Input/demo_agents.pdf`: Example scanned PDF matching the required layout
- `Input/reference_layout.png`: Visual guide to the required structure

To use your own files:
1. Place scanned PDFs in the `/Input` folder
2. Ensure they match [the reference layout](Input/reference_layout.png)

## 🚀 Usage

- Configure paths in the notebook's Configuration section
- Run all cells
- Find results in /Output/agents_export.xlsx

## 📁 File Management

### Input Files
- Place your scanned PDFs in `/Input`
- Must follow [this exact layout](Input/reference_layout.png)
- Sample file included: `Input/demo_agents.pdf`

### Output Files
- Generated Excel files appear in `/Output`
- (Folder created automatically on first run)

## ⚠️ Limitations

- Will NOT work with digital/native PDFs
- Requires precise document layout
- OCR accuracy depends on scan quality
