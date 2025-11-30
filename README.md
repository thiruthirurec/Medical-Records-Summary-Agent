# Medical Summary Record

This project uses Google Gemini and LangChain to analyze and summarize medical records from PDF files. It includes capabilities for:

- Parsing PDF documents (text and images).
- Summarizing medical images (charts, tables) using multimodal LLMs.
- Classifying medical record types.
- Generating chronological medical timelines.
- Creating structured radiology reports and medical summaries.
- Exporting summaries to DOCX format.

## Prerequisites

- Python 3.10+
- Google Cloud Project with Gemini API access.
- Tesseract OCR installed (for image text extraction).

## Installation

1.  Clone the repository.
2.  Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

3.  Install Tesseract OCR:
    - **macOS**: `brew install tesseract`
    - **Linux**: `sudo apt-get install tesseract-ocr`
    - **Windows**: Download and install the Tesseract installer.

## Configuration

Set up your Google API Key. You can set it as an environment variable or configure it within the notebook (not recommended for shared code).

```python
os.environ["GOOGLE_API_KEY"] = "your_api_key_here"
```

## Usage

1.  Place your medical PDF records in the `Data/` directory.
2.  Open `Medicalsummaryrecord.ipynb` in Jupyter Notebook or VS Code.
3.  Run the cells to process the documents.
4.  Outputs will be generated in the `Output/` directory or as specified in the notebook.

## Project Structure

- `Medicalsummaryrecord.ipynb`: Main notebook containing the logic.
- `requirements.txt`: List of Python dependencies.
- `Data/`: Directory for input PDF files (ignored by Git).
- `Output/`: Directory for generated summaries (ignored by Git).
- `tmp_images/`: Temporary directory for extracted images (ignored by Git).
