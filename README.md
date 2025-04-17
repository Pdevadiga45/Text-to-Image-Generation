# 🎨 DALL·E Text-to-Image Generator

[![Python Version](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green)](./LICENSE)

> Transform captions into stunning visuals with the ProteusV0.2 diffusion model.

---

## ✨ Features

- **Diffusion Magic**: Leverages `diffusers` & `transformers` for DALL·E–style image synthesis
- **Dataset Powered**: Processes a subset of COCO Caption 2017 via `datasets`
- **Auto-Organized**: Timestamped output directories for effortless result tracking
- **Metadata Logging**: JSON metadata for each run (prompt, filename, status, errors)
- **GPU Ready**: Seamless PyTorch `.to("cuda")` acceleration

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- (Optional) NVIDIA GPU + CUDA toolkit

### Installation

```bash
git clone https://github.com/Pdevadiga45/Text-to-Image-Generation.git
cd dall-e-text2img
pip install torch>=2.0.0 diffusers>=0.24.0 transformers>=4.36.0 datasets tqdm pillow
```

### Usage

1. **Jupyter Notebook**
   ```bash
   jupyter notebook Dall-ETexttoImage.ipynb
   ```
2. **CLI (script)**
   ```bash
   python generate_images.py --model dataautogpt3/ProteusV0.2 --split "val[:100]"
   ```

---

## 🛠️ Project Structure

```
dall-e-text2img/
├── Dall-ETexttoImage.ipynb   # Main notebook
├── generate_images.py        # CLI wrapper (optional)
├── requirements.txt          # Pin your versions here
└── LICENSE                   # MIT License
```

## ⚙️ Configuration

- Change `base_dir` in `setup_output_directory()` to customize save location
- Swap out the pretrained model in `initialize_model()` for different styles
- Tweak `split` parameter in `load_dataset()` to process more or fewer captions

## 📂 Output

- **Images**: Saved as `image_XXXX_<safe_prompt>.png` under `coco_generated/run_<TIMESTAMP>/`
- **Metadata**: Detailed `metadata.json` in the same directory

---

## 🤝 Contributing

Your contributions make this project better! Please fork, open issues, and submit PRs ✨

## 📜 License

Released under the MIT License. See [LICENSE](./LICENSE) for details.

