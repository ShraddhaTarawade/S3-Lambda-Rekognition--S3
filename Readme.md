
# Video Player App For Video Processing: Serverless AWS Architecture

## Project Overview
This project consists of a FastAPI backend for uploading and downloading video files, integrated with AWS S3 for file storage and retrieval. It also includes a Streamlit frontend for user interaction and video comparison.

## Files in the Project

### `main.py`
The main FastAPI application handling file upload and download endpoints.

### `resolver.py`
Async functions for interacting with AWS S3 to upload and download video files.

### `requirements.txt`
Lists Python dependencies required for the project.

### `Dockerfile`
Builds Docker image for the FastAPI backend.

### `config.py`
Configurations for logging levels and AWS credentials.

### `app.py`
Streamlit frontend application for video upload and display.

### `Dockerfile` (Streamlit)
Builds Docker image for the Streamlit frontend.

### `requirements.txt` (Streamlit)
Specifies Python dependencies required for the Streamlit frontend.

### `docker-compose.yml`
Defines services for backend API and Streamlit frontend.

## Running the Project

### Prerequisites
- Docker installed on your system.

### Steps

1. **Clone the Repository:**
   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. **Set Environment Variables:**
   Create a `.env` file in the root directory and define the following environment variables:
   ```dotenv
   AWS_ACCESS_KEY=<your_aws_access_key>
   AWS_SECRET_KEY=<your_aws_secret_key>
   AWS_REGION=<aws_region>
   INPUT_BUCKET=<input_bucket_name>
   OUTPUT_BUCKET=<output_bucket_name>
   ```

3. **Build and Run with Docker Compose:**
   ```bash
   docker-compose up --build
   ```

4. **Access the Application:**
   - FastAPI backend: http://localhost:8000
   - Streamlit frontend: http://localhost:8501

5. **Upload and Compare Videos:**
   - Use the Streamlit interface to upload a video file.
   - The application will display the uploaded video and its processed version for comparison.

## Notes
- Ensure Docker and Docker Compose are properly configured and running on your system.
- Adjust AWS credentials and bucket names as per your AWS setup.
- For production use, consider securing environment variables and configuring logging and error handling as per your requirements.
