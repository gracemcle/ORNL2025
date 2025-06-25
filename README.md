# ChatX

## Quick Start

Very quick start, follow:

    python3 -m venv --upgrade-deps --prompt $(basename $PWD) .venv
    source .venv/bin/activate
    pip install -r requirements.txt
    chathpc --config config.json train
    chathpc --config config.json verify
    chathpc --config config.json run

## How to Export Trained Assistant to Ollama

After installing the requirments and running training, you can use the commands below to export the model to Ollama. Each of the training scripts also export the GGUF model needed for ollama uploading.

    module load ollama
    /home/7ry/Data/ellora/llama.cpp/convert_hf_to_gguf.py merged_adapters/     
    ollama create <appname>
