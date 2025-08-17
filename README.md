<<<<<<< HEAD
Extracting Text & Bounding Boxes from Scanned PDFs 📄

This project demonstrates how to perform Optical Character Recognition (OCR) on a scanned PDF document to extract text and their corresponding bounding boxes. This is particularly useful for working with image-based PDFs where traditional text extraction methods fail. The process involves converting the PDF to an image, applying various image preprocessing techniques, and then using Tesseract OCR to recognize text and its location.

Key Concepts 

    Scanned PDFs: These are essentially images within a PDF container. You cannot extract text directly from them like you would from a digital, text-based PDF.

    Optical Character Recognition (OCR): A technology that enables you to convert different types of documents, such as scanned paper documents or images, into editable and searchable data.

    Bounding Box: A rectangular coordinate system (x, y, width, height) that defines the location of a word or a block of text on an image.

    Image Preprocessing: Techniques like grayscaling, adaptive thresholding, and bilateral filtering are applied to an image to improve its quality and make it easier for the OCR engine to recognize characters accurately.

Project Steps 

    Dependency Setup: Installs necessary libraries, including tesseract-ocr, PyMuPDF, pytesseract, OpenCV, and Pillow.

    PDF to Image Conversion: A scanned PDF page is converted into a high-resolution image using PyMuPDF.

    Image Preprocessing: The image is preprocessed with grayscaling, adaptive thresholding, and bilateral filtering to optimize it for OCR. Resizing the image is also a key step to improve Tesseract's performance.

    OCR Text Extraction: pytesseract is used to perform OCR on the preprocessed image to get the raw text content.

    Bounding Box Extraction: The image_to_data function from pytesseract is used to get not just the text, but also detailed information about each detected word, including its confidence score and bounding box coordinates.

    Post-OCR Processing: The raw OCR text is cleaned by removing extra spaces and special characters. Common OCR errors are also corrected using regular expressions.

    Visualization: Bounding boxes are drawn directly onto the image using OpenCV, visually highlighting both all detected words and specific key fields (like "LENDER" or "MORTGAGE") within the document.

    Structured Data Output: The extracted key fields and their bounding box coordinates are stored in a structured JSON format, making the data easy to use for further processing or storage.

This project provides a robust workflow for handling scanned documents, transforming them from static images into structured, searchable data.

give me the README.md text exactly for me talk about how this was initially for mortgage documents but i used a Resume as a example document

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
=======
# ML-Doc-Data-and-Bounding-Box-Extraction
>>>>>>> origin/main
