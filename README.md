OCR Text and Bounding Box Extraction: Scanned PDF to Structured Data 📄

This project provides a comprehensive workflow for extracting text and bounding box information from scanned PDF documents using OCR. While the initial use case was for mortgage documents, the process is highly adaptable and can be applied to any scanned document type, as demonstrated here using a resume as an example.

How It Works 

Traditional PDF text extraction fails on scanned documents because they are essentially images. This solution addresses that by:

    Converting the PDF to an Image: Each page of the scanned PDF is rendered as an image file.

    Preprocessing the Image: The image is optimized for OCR using techniques like grayscaling, adaptive thresholding, and noise reduction. This step is crucial for improving OCR accuracy.

    Applying OCR: The preprocessed image is fed into Tesseract OCR, which recognizes the text and provides the bounding box coordinates for each word.

    Post-Processing and Data Extraction: The raw OCR output is cleaned to remove errors. Key fields (e.g., "Name," "Education," "Experience" on a resume) are identified, and their text and bounding box data are extracted into a structured JSON format.

Key Features 

    Robust Text Extraction: Successfully extracts text from image-based PDFs where standard methods fail.

    Bounding Box Coordinates: Provides the (x, y, width, height) for each word, allowing for precise location of text on the page.

    Visual Validation: Generates an image with bounding boxes drawn around the detected text, providing a clear visual representation of the OCR output.

    Structured Data Output: Converts extracted information into a machine-readable JSON format, perfect for downstream applications like data entry or document analysis.

How to Use 

    Clone the repository or copy the code into a Python environment.

    Install dependencies:
    Bash

    !pip install pymupdf pytesseract opencv-python pillow
    !apt install tesseract-ocr

    Upload your scanned PDF (e.g., my_resume.pdf).

    Run the script. The output will include the extracted text, a visual representation with bounding boxes, and the structured JSON data.

This project is a powerful tool for anyone needing to convert unstructured, scanned documents into usable, digital data.
