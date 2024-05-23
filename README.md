# Ethical Interview Assessment App

This application facilitates recording audio responses to interview questions, converting the audio to text, and evaluating the responses using an AI model. The results are then compiled into a CSV report.

## Features

- Record audio answers to predefined interview questions
- Convert audio to text
- Evaluate responses using a predefined set of standard answers and an AI model
- Generate and upload a CSV report with questions, answers, scores, and feedback

## Setup and Installation

1. **Clone the Repository**
    ```bash
    git clone https://github.com/your-username/your-repository.git
    cd your-repository
    ```

2. **Install Dependencies**
    Make sure you have Python and pip installed. Then run:
    ```bash
    pip install -r requirements.txt
    ```

3. **Set Up Google Cloud Credentials**
    - Create a service account in Google Cloud with access to Google Cloud Storage.
    - Download the service account key file and save it as `ai-interview-assessment-ce180dfa157c.json`.
    - Set the environment variable for Google Application Credentials:
    ```bash
    export GOOGLE_APPLICATION_CREDENTIALS="path/to/ai-interview-assessment-ce180dfa157c.json"
    ```

4. **Set Up OpenAI API**
    - Obtain an API key from OpenAI.
    - Replace `"Key"` in the code with your actual API key.

5. **Run the Application**
    ```bash
    streamlit run app.py
    ```

## Usage

1. **User Details Section**
    - Enter your name and email to start the interview.

2. **Interview Questions**
    - You will be presented with three questions.
    - Each question has a preparation time of 30 seconds and a recording time of 30 seconds.
    - Your audio responses will be recorded, transcribed, and evaluated.

3. **Report Generation**
    - After answering all questions, a CSV report will be generated.
    - You can download the report directly from the application.

## Files and Directories

- `app.py`: Main application script
- `requirements.txt`: List of dependencies
- `ai-interview-assessment-ce180dfa157c.json`: Google Cloud service account key file (not included in the repository)

## Dependencies

- streamlit
- os
- io
- pyaudio
- wave
- google-cloud-storage
- time
- pydub
- speech_recognition
- shutil
- requests
- openai
- httpx
- csv

## Functionality Overview

- **Recording Audio**: Uses `pyaudio` to record audio responses to interview questions.
- **Transcription**: Converts recorded audio to text using `speech_recognition`.
- **Evaluation**: Uses an OpenAI model to score and provide feedback on the transcribed responses.
- **Report Generation**: Compiles responses, scores, and feedback into a CSV file.
- **Storage**: Uploads audio responses and reports to Google Cloud Storage.

## Contributing

Feel free to open issues or submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License.

