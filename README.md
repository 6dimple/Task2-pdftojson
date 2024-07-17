# Task2-pdftojson
PDF Text and Image Extractor
This script extracts text and images from a PDF file using PyMuPDF (fitz) and converts the extracted data into a JSON format. The images are encoded in base64 and included in the JSON output.

Requirements
Python 3.7+
PyMuPDF
pydantic
Pillow
Installation
Install the required packages using pip:


pip install pymupdf pydantic pillow
Usage
Place your PDF file in the same directory as the script, or specify the path to your PDF file.

Update the pdf_file_path variable in the script with the path to your PDF file.

Run the script:


python extract_pdf_data.py
The script will extract text and images from the PDF, encode the images in base64, and save the data to output.json in the same directory.
Output
The output JSON file (output.json) will have the following structure:

json

{
    "file_name": "Biology2e-WEB_Excerpt.pdf",
    "pages": [
        {
            "page_number": 0,
            "text": "Extracted text from page 0...",
            "images": [
                {
                     page_number": 0,
                    "image_index": 0,
                    "image_base64": "base64-encoded image string..."
                },
                ...
            ]
        },
        ...
    ]
}
