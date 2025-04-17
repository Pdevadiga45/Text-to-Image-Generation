# Text to Image Generation using DALL-E

This project uses a DALL-E model from Hugging Face to generate images from text descriptions.

## Setup

1. Make sure you have Python 3.7+ installed
2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Run the script using:
```bash
python text_to_image.py
```

The script will:
1. Prompt you to enter a text description
2. Generate an image based on your description
3. Save the generated image in the `output` directory

## Features

- Supports GPU acceleration if available
- Automatically creates output directory
- Error handling for failed generations
- Uses the ProteusV0.2 model for high-quality image generation

## Notes

- The first run will download the model weights (several GB)
- GPU is recommended for faster generation
- Generated images are saved in PNG format 
