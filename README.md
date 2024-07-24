# Google Drive Backup Service

## Project Overview

This project involves the development of a robust and automated backup service that securely uploads folder contents to Google Drive at regular intervals. The service leverages Docker for containerization and Kubernetes for scheduling, ensuring scalability and reliability.

## Key Components

1. **Google Drive API Integration:**
   - Enable and configure the Google Drive API through the Google Cloud Console.
   - Obtain and securely manage OAuth credentials for authentication.

2. **Docker Containerization:**
   - Create a Dockerfile to install necessary dependencies and copy the backup script.
   - Build a Docker image to encapsulate the backup functionality.

3. **Backup Script Development:**
   - Implement a Python script to authenticate with Google Drive and manage file operations (list, upload).
   - Ensure the script handles errors, network failures, and API rate limits.

4. **Scheduling with Kubernetes:**
   - Use Kubernetes CronJobs to schedule the Docker container to run the backup script at specified intervals.

This service ensures that critical data is periodically backed up to Google Drive, providing a reliable and scalable solution for data protection.

## Setup Instructions

### 1. Set up Google Drive API

1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project or select an existing one.
3. Enable the Google Drive API for your project.
4. Create credentials for the API by selecting 'Create credentials' and choosing 'OAuth client ID'. This will generate a client ID and client secret.
5. Download the credentials file (JSON format) which contains your client ID and client secret. This file will be used by your Python script to authenticate with Google Drive.
6. Install the `google-api-python-client` library if not already installed:
   ```sh
   pip install google-api-python-client
