# 🔍 Crack Segmentation using UNet-VGG16

A deep learning model for **automatic crack detection and segmentation** in concrete/pavement surfaces using a **UNet architecture with VGG-16 encoder** backbone, built with PyTorch.

## 📌 Overview

Cracks in infrastructure such as roads, bridges, and buildings can indicate structural deterioration. Manual inspection is time-consuming and error-prone. This project uses a semantic segmentation approach to automatically detect and segment cracks from images.

## 🏗️ Model Architecture

- **Architecture:** UNet (Encoder-Decoder with skip connections)
- **Encoder Backbone:** VGG-16 (pre-trained on ImageNet)
- **Framework:** PyTorch
- **Task:** Binary Semantic Segmentation (Crack vs Background)

```
Input Image → VGG-16 Encoder → Bottleneck → Decoder (with skip connections) → Segmentation Mask
```

## 📂 Project Structure

```
├── model_unet_vgg_16_best.pt   # Best trained model weights
├── .gitattributes               # Git LFS tracking config
└── README.md                    # Project documentation
```

## 🚀 Usage

### Prerequisites

```bash
pip install torch torchvision
```

### Load the Model

```python
import torch

# Load the trained model
model = torch.load('model_unet_vgg_16_best.pt', map_location='cpu')
model.eval()

# Run inference on an image
with torch.no_grad():
    prediction = model(input_tensor)  # input_tensor: [B, 3, H, W]
```

## 📊 Results

| Metric | Score |
|--------|-------|
| Model Size | ~117 MB |
| Architecture | UNet + VGG-16 |
| Output | Binary Segmentation Mask |

## 🛠️ Tech Stack

- **Python**
- **PyTorch**
- **VGG-16** (ImageNet pre-trained)
- **UNet** architecture

## 📜 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.

## 📬 Contact

- GitHub: [@adi-coderr](https://github.com/adi-coderr)

---

⭐ **Star this repo** if you find it useful!
