

- ARTPARK-IISc/whisper-small-vaani-kannada
    - huggingface-cli download ARTPARK-IISc/whisper-small-vaani-kannada

- 

https://huggingface.co/ai4bharat/indicconformer_stt_kn_hybrid_ctc_rnnt_large


https://ai4bharat.iitm.ac.in/areas/model/ASR/IndicWhisper

- Tranlsate IndicWhisper with Ctranslate2 to run faster in docker

https://github.com/OpenNMT/CTranslate2


https://huggingface.co/distil-whisper/distil-large-v3

ct2-transformers-converter --model openai/whisper-base --output_dir faster-whisper-base \
    --copy_files tokenizer.json --quantization float16

-- Conversion to cranslate2

huggingface-cli download ARTPARK-IISc/whisper-small-vaani-kannada --local-dir kannada-asr/

pip install ctranslate2
pip install torch transformers