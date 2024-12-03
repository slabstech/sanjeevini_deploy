Voice Integrations - 

- Download Whisper models from Huggingface
    - pip install -U "huggingface_hub[cli]"

    - huggingface-cli download Systran/faster-distil-whisper-small.en




- Docker for 
    - Speech ASR
        - docker compose -f speech-asr-compose.yml up -d
    
    - Speech LLM
        - docker compose -f speech-llm-compose.yml up -d

    - For Speech to Speech - 
        - docker compose -f speech-to-speech-compose.yml up -d

