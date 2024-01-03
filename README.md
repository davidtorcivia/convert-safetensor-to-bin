# SafeTensor to Bin Converter

This repository contains the `safetensor-to-bin.py` script, which is designed to convert `.safetensors` files to a binary format (`.bin`) for LoRA's and QLoRA's for Large Language Models (LLM's).

Why would you want to do this? The default training tab of text-generation-webui saves loras and qloras as adapter_model.safetensors which do not have an easy way to convert to ggml files for use with gguf quantized base models. `convert-lora-to-ggml.py`, part of the transformers package that converts loras to work with gguf, only accepts .bin files. This script allows you to convert your safetensors to bin files that can then be easily converted to ggml for use with gguf's in koboldcpp, etc.

## Installation

### Prerequisites

- Python 3.11 recommended (may work with 3.8, I didn't test)
- Conda (recommended for managing environments)

### Setting up the Environment

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/davidtorcivia/safetensor-to-bin.git
   cd safetensor-to-bin
   conda create --name safetensor-to-bin python=3.11
   conda activate safetensor-to-bin
   ```
2. **Install Requirements**:

   ```bash
   pip install -r requirements.txt
   ```
### Usage

   Run the script from the command line by providing the path to the .safetensors file and the desired output path for the .bin file.
   ```bash
   python safetensor-to-bin.py path/to/adapter_model.safetensors path/to/adapter_model.bin
   ```
   Replace path/to/adapter_model.safetensors and path/to/adapter_model.bin with the actual paths to your .safetensors file and the desired output path, respectively.
