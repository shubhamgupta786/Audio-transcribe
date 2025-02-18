# Audio Transcription API

This project provides a RESTful API for audio transcription using OpenAI's audio transcription capabilities. The main controller, `TranscriptionController`, handles audio file uploads and returns the transcribed text.

## Overview

The `TranscriptionController` is responsible for:

- Accepting audio files via a POST request.
- Transcribing the audio content to text using OpenAI's transcription model.
- Returning the transcribed text as a response.

## Endpoints

### POST /api/transcibe

This endpoint allows users to upload an audio file for transcription.

#### Request

- **Content-Type**: `multipart/form-data`
- **Parameters**:
  - `file`: The audio file to be transcribed (must be in `.wav` format).
  - - **Status Code**: `200 OK`
- **Body**: The transcribed text from the audio file.

#### Example Request Using cURL

curl -X POST http://localhost:8080/api/transcibe
-F "file=@path/to/your/audio.wav"

#### Example Response
 {
"result": "This is the transcribed text from the audio."
 }
 


## Setup Instructions

1. **Clone the repository**:

2. **Install dependencies**:
Make sure you have Maven or Gradle installed. Run:

3. **Configure API Key**:
Add your OpenAI API key in the `application.properties` file:

4. **Run the application**:
Start your Spring Boot application:

5. **Test the API**:
Use tools like Postman or cURL to send requests to your API.

## Dependencies

- Spring Boot
- Spring Web
- OpenAI Java SDK (for audio transcription)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.





