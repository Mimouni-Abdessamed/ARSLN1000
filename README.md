# ARSLN1000: Arabic Sign Language Numbers Dataset (0–1000)

ARSLN1000 is a curated dataset of Arabic Sign Language numbers created by a team of six contributors. It includes:

- Left and right hand representations
- Arabic sign numbers from 0 to 1000, in intervals (0, 1, 2, ..., 10, 20, 30, ..., 100, 200, ..., 1000)
- Approximately 800 to 1200 images per class
- Each sign was manually performed and captured by the contributors using consistent backgrounds and lighting

## Dataset Structure

ARSLN1000/
├── dataset/
│ ├── 0/
│ ├── 1/
│ ├── ...
│ ├── 100/
│ ├── ...
│ └── 1000/
├── README.md
└── LICENSE


Each folder contains `.jpg` images for a specific sign number (e.g., `30/` contains all images of the number 30 in sign language).

## Image Specifications

- Format: `.jpg`
- Image size: `224 x 224` pixels
- Horizontal resolution: `96 DPI`
- Vertical resolution: `96 DPI`
- Color: RGB

## Contributors

This dataset was created by a team of six students:

- Abdessamed
- [Add the other 5 names here]

Each contributor performed approximately 200 images per number (100 using the left hand and 100 using the right hand).

## Dataset Statistics

- Number of Classes: Approximately 42 (e.g., 0, 1, 2, ..., 10, 20, ..., 1000)
- Images per Class: 800–1200
- Total Images: **30,813**
- Image Format: JPG

## Applications

- Sign language recognition projects
- Gesture-based AI models
- Arabic Sign Language educational tools
- Dataset benchmarking for hand sign recognition

## Example: How to Load Images in Python

```python
import os
from PIL import Image

folder = 'dataset/50'  # Folder for number 50
images = []

for filename in os.listdir(folder):
    if filename.endswith(".jpg") or filename.endswith(".png"):
        img = Image.open(os.path.join(folder, filename))
        images.append(img)

