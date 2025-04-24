# Deployment Guide for Gaganyatri.in

This guide provides instructions on how to deploy the Gaganyatri.in project, which includes both the frontend and backend components. You can deploy the project to the cloud or locally on your machine.

## Prerequisites

Before you begin, make sure you have the following:

- A GitHub account
- Docker (for local deployment)
- Node.js and npm (for local frontend deployment)
- Python and pip (for local backend deployment)

## Fork the Repository

1. Fork the repository from [https://github.com/slabstech/gaganyatri.in](https://github.com/slabstech/gaganyatri.in) to your GitHub account.

## Cloud Deployment

### Backend

1. Duplicate the Huggingface Space at [https://huggingface.co/spaces/gaganyatri/django_spaces](https://huggingface.co/spaces/gaganyatri/django_spaces).
2. Add the following environment variables for AI Inference:
   - Get a subscription for Mistral, Sarvam, and NVIDIA nim.
   - Set the API keys as environment variables:
     - `MISTRAL_API_KEY='MISTRAL_KEY_ADD_HERE'`
     - `NIM_API_KEY='NVIDIA-NIM-ADD-HERE'`
     - `SARVAM_API_KEY='SARVAM-KEY-ADD-KEY-HERE'`
3. Restart the Spaces to apply the changes.

### Frontend

1. In your GitHub repository, add a repository secret for Huggingface Spaces:
   - `VITE_SANJEEVINI_BACKEND_APP_API_URL=https://Your-Spaces-URL/api/v1`
2. Navigate to the `frontend` directory:
   - `cd frontend`
3. Build the frontend:
   - `npm run build`
4. Deploy the frontend:
   - `npm run deploy`

## Local Deployment with GPU

### Without Docker

1. For the UI/frontend:
   - Navigate to the `frontend` directory:
     - `cd frontend`
   - Install dependencies:
     - `npm install`
   - Run the development server:
     - `npm run dev`
2. For the App Server/backend:
   - Create a virtual environment:
     - `python -m venv venv`
   - Activate the virtual environment:
     - `source venv/bin/activate`
   - Install dependencies:
     - `pip install -r requirements.txt`
   - Run the server:
     - `python manage.py runserver`


### With Docker

1. To deploy the application:
  - Update Environment Variables for Docker 
    - Copy .env.prod.sample as .env.prod
    - If required, change the database parameters

  - Start the Containers 
   - `docker compose -f docker-compose.prod.yml up`
2. To deploy the inference:
   - `docker compose -f inference-compose.yml up -d`


### Inference
cd compose-files

1. For Text LLM only
  - docker compose -f llm-compose.yml up -d

2. For Speech ASR only
  - docker compose -f speech-asr-compose.yml up -d

3. For Speech ASR + LLM
  - docker compose -f speech-llm-compose.yml up -d

4. For Speech ASR + LLM + TTS
  - docker compose -f speech-to-speech-compose.yml up -d

## Speech AI (GPU Required)

- Download the model:
  - `huggingface-cli download Systran/faster-distil-whisper-small.en`

Follow these steps to deploy the speech AI component, which requires a GPU for optimal performance. Please note that this section is still under development.
