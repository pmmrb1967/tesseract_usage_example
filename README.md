# PDF Scanned Data to Excel Extractor

This Jupyter Notebook demonstrates how to use **Tesseract OCR** to extract structured data from scanned PDF documents with a predefined layout and export it to Excel.

## ⚠️ Important Requirements

1. **PDF Type**: Works ONLY with **scanned/image-based PDFs** (no selectable text)
2. **Layout**: PDFs **must match** [this exact layout](https://github.com/pmmrb1967/tesseract_usage_example/blob/main/Input/reference_layout.png))  
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

## 📁 File Management

### Input Files
- Place your scanned PDFs in `/Input`
- Must follow the layout in the 'Important Requirements' section
- Sample file included: `Input/demo_agents.pdf`

### Output Files
- Generated Excel files appear in `/Output`
- (Folder created automatically on first run)

## 🚀 Usage

- Configure paths in the notebook's Configuration section
- Run all cells
- Find results in /Output/agents_export.xlsx
- The Excel Output is like this [excel output](https://github.com/pmmrb1967/tesseract_usage_example/blob/main/Input/agents_export.png)

## ⚠️ Limitations

- Will NOT work with digital/native PDFs
- Requires precise document layout
- OCR accuracy depends on scan quality
