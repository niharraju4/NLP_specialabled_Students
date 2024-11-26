# AI Learning Platform

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Backend (Flask)](#backend-flask)
4. [Frontend (Streamlit)](#frontend-streamlit)
5. [Installation](#installation)
6. [Usage](#usage)
7. [Future Enhancements](#future-enhancements)
8. [PDF Question Answering Streamlit App](#pdf-question-answering-streamlit-app)
9. [Running the PDF Question Answering App](#running-the-pdf-question-answering-app)
10. [Limitations and Improvements](#limitations-and-improvements)

## Introduction

This project provides a comprehensive AI-based audio learning platform using Python for both backend and frontend. The platform includes features such as lesson creation, text-to-speech conversion, question answering, text summarization, basic translation, and speech-to-text conversion.

## Features

### Backend (Flask)

- Lesson creation and retrieval
- Text-to-speech conversion using gTTS
- Question answering using a pre-trained model
- Text summarization
- Basic translation
- Speech-to-text conversion

### Frontend (Streamlit)

- User-friendly interface for creating and viewing lessons
- Audio playback of lessons
- Question asking functionality
- Display of lesson summaries
- Speech-to-text feature
- Text translation feature

## Backend (Flask)

The backend is implemented using Flask and provides various endpoints for lesson management, text-to-speech conversion, question answering, text summarization, translation, and speech-to-text conversion.

### Endpoints

- `/api/lessons`: Create and list lessons.
- `/api/lessons/<lesson_id>`: Get a specific lesson.
- `/api/lessons/<lesson_id>/ask`: Ask a question about a lesson.
- `/api/translate`: Translate text.
- `/api/speech-to-text`: Convert speech to text.

### Dependencies

- Flask
- Flask-CORS
- Transformers
- Torch
- gTTS
- SpeechRecognition

## Frontend (Streamlit)

The frontend is implemented using Streamlit and provides a user-friendly interface for interacting with the backend.

### Features

- Create and view lessons
- Play audio of lessons
- Ask questions about lessons
- Display lesson summaries
- Convert speech to text
- Translate text

### Dependencies

- Streamlit
- Requests
- gTTS

## Installation

### Backend

1. Clone the repository.
2. Navigate to the backend directory.
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the Flask app:
   ```bash
   python app.py
   ```

### Frontend

1. Navigate to the frontend directory.
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Streamlit app:
   ```bash
   streamlit run streamlit_app.py
   ```

## Usage

1. Start the backend server.
2. Start the frontend server.
3. Open the Streamlit app in your browser.
4. Use the interface to create lessons, view lessons, ask questions, convert speech to text, and translate text.

## Future Enhancements

- Implement user authentication and authorization
- Add a database for persistent storage of lessons and user data
- Enhance the NLP capabilities with more advanced models or fine-tuned models for educational content
- Implement more robust error handling and validation
- Add support for creating and taking quizzes
- Implement progress tracking for students
- Enhance multilingual support with more language options
- Optimize performance for larger datasets
- Implement caching mechanisms to improve response times

## PDF Question Answering Streamlit App

This simplified implementation allows users to upload a PDF document, ask questions, and get exact matches from the text.

### Features

- PDF Upload: Users can upload a PDF document.
- Text Extraction: The app extracts text from the uploaded PDF.
- Question Input: Users can enter questions about the document.
- Exact Matching: The app searches for sentences in the document that contain all the words from the question.
- Answer Display: Matching sentences are displayed as potential answers.

### Limitations

- Only works with text-based PDFs (not scanned documents).
- The matching is based on exact word matches, so it may miss relevant sentences if the wording is different.
- It doesn't understand context or semantics, just word presence.

### Improvements

- Add support for other document types (e.g., .docx, .txt).
- Implement more advanced text processing (e.g., stemming, removing stop words).
- Use a more sophisticated search algorithm or a basic NLP model for better matching.
- Add a feature to highlight the matching text in the original document.
- Implement caching to improve performance for large documents.

## Running the PDF Question Answering App

1. Save the code in a file named `app.py`.
2. Install the required libraries:
   ```bash
   pip install streamlit PyPDF2
   ```
3. Run the Streamlit app:
   ```bash
   streamlit run app.py
   ```

## Limitations and Improvements

### Limitations

- The current implementation only works with text-based PDFs.
- The matching algorithm is simple and may miss relevant sentences.
- The app does not understand context or semantics.

### Improvements

- Add support for other document types.
- Implement more advanced text processing.
- Use a more sophisticated search algorithm or a basic NLP model.
- Add a feature to highlight the matching text in the original document.
- Implement caching to improve performance for large documents.

