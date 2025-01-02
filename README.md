# Medical Report Extraction and Analysis

This repository provides a solution for extracting, analyzing, and generating medical reports from images or PDFs containing medical data. It uses Optical Character Recognition (OCR) to extract the text from uploaded files, processes the data, validates the results based on normal test ranges, generates a tabular output, visualizes the data, and creates a downloadable PDF medical report. Additionally, it can generate a voice summary of the report.

## Features

- **OCR-based Text Extraction**: Extracts text from images or PDFs using Tesseract OCR.
- **Data Extraction & Parsing**: Extracts relevant information such as patient name, age, glucose levels, WBC count, and diagnosis using regular expressions.
- **Data Validation**: Validates the extracted data (e.g., glucose level, WBC count) against normal ranges to determine if the results are normal or abnormal.
- **Tabular Representation**: Converts the parsed data into a tabular format using pandas for easy analysis.
- **Report Visualization**: Plots visual representations of the medical data using `matplotlib` to give a quick overview of the patient’s health status.
- **PDF Generation**: Creates a downloadable PDF of the medical report.
- **Audio Summary**: Generates a speech summary of the medical report using `gTTS` (Google Text-to-Speech).

## Technologies Used

- **Tesseract OCR**: For extracting text from images and PDFs.
- **pytesseract**: Python wrapper for Tesseract OCR.
- **pdfplumber**: For reading and extracting text from PDFs.
- **pandas**: For structuring extracted data into a tabular format.
- **matplotlib**: For generating visual representations of the extracted data.
- **FPDF**: For generating downloadable PDF reports.
- **gTTS (Google Text-to-Speech)**: For generating audio reports.

## Installation

To use this tool, you'll need to install the following dependencies:

1. Install Tesseract OCR:
    ```bash
    sudo apt install tesseract-ocr
    ```

2. Install Python dependencies:
    ```bash
    pip install pytesseract pdfplumber pandas matplotlib fpdf gtts
    ```

## How to Use

1. **Upload an Image or PDF**:
   - Upload the medical document in image (e.g., PNG, JPEG) or PDF format using the file upload prompt.

2. **Extract Text**:
   - The script will automatically extract text from the uploaded image or PDF using Tesseract OCR.

3. **Parse Medical Data**:
   - Relevant information such as Patient Name, Age, Glucose Level, WBC Count, and Diagnosis will be extracted using regular expressions.

4. **Validate and Visualize**:
   - The extracted medical data will be validated against normal test ranges (e.g., glucose level, WBC count).
   - The results will be visualized in a bar chart.

5. **Generate PDF**:
   - The script will generate a PDF containing the medical report which you can download.

6. **Generate Audio**:
   - An audio summary of the medical report will be created and played using Google Text-to-Speech (gTTS).

## Example Workflow

- Upload an image or PDF containing medical information.
- The system will process the file, extract relevant medical data, validate it, generate a visual chart, and create a downloadable PDF report.
- The report summary will also be available as an audio file.

## Output Examples

1. **Tabular Output**:
    ```plaintext
    Patient Name     | John Doe
    Age              | 35
    Gender           | Male
    Glucose Level    | 140 mg/dL
    WBC Count        | 8500 cells/μL
    Diagnosis        | Hypertension
    ```


2. **Medical Report in PDF**:
    - A downloadable PDF containing the extracted and validated data.
    - [Download Medical Report PDF](./Medical_Report%20(1).pdf)


3. **Speech Summary**:
    - A voice summary of the medical report.
