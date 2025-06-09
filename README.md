# WERS Code Extractor

A Flask web application that extracts and processes codes from Word documents (.docx files). This tool helps in extracting specific codes and their descriptions from document content.

## Features

- Upload Word documents (.docx) for processing
- Extract codes and their descriptions from document content
- Compare codes across multiple documents
- Download extracted data in text format
- Simple and intuitive web interface

## Prerequisites

- Python 3.9 or higher
- pip (Python package installer)

## Local Development Setup

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd werscodeextractor
   ```

2. **Create and activate a virtual environment**
   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python app.py
   ```

5. **Access the application**
   Open your browser and go to `http://localhost:5000`

## Deployment on Render

This application is configured for easy deployment on [Render](https://render.com/):

1. Push your code to a GitHub repository
2. Create a new Web Service on Render and connect your GitHub repository
3. Use the following settings:
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `gunicorn app:app -c gunicorn_config.py`
4. Deploy the application

## Project Structure

```
werscodeextractor/
├── app.py                # Main application file
├── requirements.txt      # Python dependencies
├── gunicorn_config.py    # Gunicorn configuration
├── Procfile             # Process file for deployment
├── render.yaml          # Render deployment configuration
├── runtime.txt          # Python version specification
├── .gitignore          # Git ignore file
├── uploads/            # Directory for uploaded files (created at runtime)
└── templates/          # HTML templates
    ├── upload.html
    ├── display.html
    └── comparison_results.html
```

## Usage

1. **Upload Document**
   - Click "Choose File" to select a Word document (.docx)
   - Click "Upload" to process the document

2. **View Extracted Codes**
   - The application will display all extracted codes and their descriptions
   - You can download the results as a text file

3. **Compare Documents**
   - Upload multiple documents to compare the extracted codes
   - The application will show common and unique codes across documents

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support, please open an issue in the GitHub repository.
