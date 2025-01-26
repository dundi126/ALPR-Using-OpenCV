# ALPR (Automatic License Plate Recognition) using OpenCV

## Overview

This project implements an Automatic License Plate Recognition (ALPR) system using OpenCV and Python. The system is capable of detecting vehicle license plates from images or video streams and extracting the text using Optical Character Recognition (OCR).

The project analyzes prediction results based on preprocessing techniques such as scaling, bilateral filtering, edge detection, and sharpening. The document categorizes the results into three prediction categories: GOOD, MEDIUM, and POOR, explaining the reasons behind each outcome.

## Features

- Detect license plates in images or video.
- Extract text from license plates using OCR (EasyOCR or Tesseract).
- Preprocessing steps to improve plate recognition accuracy.
- Lightweight and easy to use.

## Requirements

To run this project, you'll need:

- Python 3.7+
- OpenCV
- EasyOCR
- Imutils
- NumPy
- Matplotlib (optional for visualization)

Install dependencies using:

```bash
pip install opencv-python easyocr imutils numpy matplotlib
```

## How It Works

1. **License Plate Detection:**

   - The project uses OpenCV for image processing and contour detection to locate license plates.
   - Preprocessing techniques such as grayscale conversion, blurring, edge detection, and thresholding are applied to improve detection accuracy.

2. **Text Extraction:**

   - Once the license plate is detected, it is passed to an OCR library (e.g., EasyOCR) to extract the alphanumeric text.

3. **Result Visualization:**
   - Detected plates and extracted text are visualized on the image or video frame.

## Prediction Categories

### 1. GOOD Predictions

- **Success Factors:**
  - Effective preprocessing steps: scaling, bilateral filtering, edge detection.
  - Sharpening techniques enhanced text clarity.
- **Examples:**
  - Recognized plates: `DXZ-7929`, `KLF-5768`.

### 2. MEDIUM Predictions

- **Challenges Faced:**
  - Partial recognition due to emblem misclassification.
  - Inappropriate preprocessing parameters leading to noise interference.
- **Examples:**
  - Misclassified plates such as `1010169` instead of `101169`.

### 3. POOR Predictions

- **Failure Causes:**
  - Incomplete contour detection.
  - Difficult image conditions (e.g., poor lighting, camera distortion).
  - Suboptimal preprocessing settings.
- **Examples:**
  - Only partial characters recognized, such as `D`, `E`, or `8`.

## Preprocessing Techniques Used

1. **Scaling:** Adjusting the image size for better feature extraction.
2. **Bilateral Filtering:** Reducing noise while preserving important edges.
3. **Edge Detection:** Identifying contours of the license plate.
4. **Sharpening:** Enhancing the clarity of text for accurate recognition.

## Project Structure

```
├── README.md          # Project documentation
├── scripts/           # Code for preprocessing and recognition
└── results/           # Output results categorized
```

## Examples

### Image Example

![License Plate Detection Example](/results/output_image8.jpg)

## Setup and Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ALPR-Using OpenCV.git
   ```
2. Navigate to the project folder:
   ```bash
   cd ALPR-Using OpenCV/scripts
   ```
3. Run the individula file

## Future Enhancements

- Enhance plate detection with advanced deep learning models.
- Integrate a real-time ALPR system with a web interface.
- Support for multi-language OCR.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
