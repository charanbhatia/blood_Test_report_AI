# Blood Test Analysis and Health Recommendation System

## Project Overview

This project is an automated system that analyzes blood test reports, searches for relevant health information, and provides personalized health recommendations. It uses AI-powered agents to process PDF blood test reports, interpret the results, find related medical articles, and generate tailored health advice.

## Features

- PDF parsing with OCR capability for extracting blood test data
- AI-powered analysis of blood test results
- Web search for relevant health articles based on test results
- Generation of personalized health recommendations
- Modular architecture using CrewAI for orchestrating multiple AI agents

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.8 or higher
- Tesseract OCR installed on your system
- OpenAI API key
- Google Custom Search API key and Search Engine ID

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/charanbhatia/blood_Test_report_AI
   cd blood_Test_report_AI
   ```

2. Create a virtual environment and activate it:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

4. Set up your environment variables:
   - Create a `.env` file in the project root
   - Add the following lines:
     ```
     OPENAI_API_KEY=your_openai_api_key
     GOOGLE_API_KEY=your_google_api_key
     GOOGLE_CSE_ID=your_google_custom_search_engine_id
     ```

## Usage

To analyze a blood test report:

```
python main.py path/to/your/blood_test_report.pdf
```

The script will process the PDF, analyze the blood test results, search for relevant health information, and provide recommendations.

## Project Structure

- `main.py`: The entry point of the application
- `agents.py`: Defines the AI agents, their tools, and the crew orchestration
- `requirements.txt`: Lists all Python dependencies

## How It Works

1. The system reads and extracts text from the provided PDF blood test report.
2. The Blood Test Analyzer agent interprets the test results.
3. The Web Search Specialist agent searches for relevant health articles based on the analysis.
4. The Health Recommendations Expert agent generates personalized health advice.
5. The results are compiled and presented to the user.

## Customization

You can customize the behavior of the agents by modifying their roles, goals, and tools in the `agents.py` file. Adjust the `max_iterations` and `max_rpm` parameters to fine-tune performance.

## Troubleshooting

- If you encounter OCR-related issues, ensure Tesseract is correctly installed and accessible in your system PATH.
- For API-related errors, double-check your environment variables and API key validity.


## Acknowledgments

- OpenAI for providing the language model capabilities
- Google for the Custom Search API
- The creators of CrewAI, langchain, and other open-source libraries used in this project
