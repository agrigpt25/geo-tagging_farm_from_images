
# Tesseract OCR – Email Extraction from Images

A professional, beginner-friendly project demonstrating how to use **Tesseract OCR with Python** to extract text from images and detect **email addresses** using Optical Character Recognition (OCR).

This repository is suitable for **students, beginners, and interview demonstrations**, and can be executed end-to-end with clear setup instructions.

---

## Table of Contents
- Overview
- Features
- Tech Stack
- Project Structure
- Dataset
- Installation
  - Tesseract OCR
  - Python Dependencies
- Configuration
- Running the Project
- Output
- Limitations
- Future Enhancements
- License

---

## Overview

This project uses the Tesseract OCR engine with Python to:
- Read text from images
- Identify email addresses using regular expressions
- Draw bounding boxes around detected emails
- Print extracted results to the console

The goal is to provide a **simple and clean OCR pipeline** without using deep learning or external APIs.

---

## Features

- Pure OCR-based text extraction
- Email detection using Regex
- Bounding box visualization using OpenCV
- Beginner-friendly and well-documented
- Easy to extend for other text patterns

---

## Tech Stack

- Python 3.8+
- Tesseract OCR
- pytesseract
- OpenCV (cv2)
- Regular Expressions (re)

---

## Project Structure

```
project-root/
│
├── demo_tesseract.py        # Main Python script
├── demo_image.png           # Sample input image
└── README.md                # Project documentation
```

---

## Dataset

You can use **any image containing visible text**.

Sample dataset / image reference:
https://www.kaggleusercontent.com/kf/51419076/eyJhbGciOiJkaXIiLCJlbmMiOiJBMTI4Q0JDLUhTMjU2In0..G5S5I9FVZg9tTlxhRxdgbg.jY1LefTVxpgYkUVKYa0N6kez3spOKW9UQ3cRlKxd_2AkFmnmxLVtgO1acoQAKf1I3vMrDMhvPORIOaSyMqoS7lnBV96Midy0fH5uR2A8Ge4RMSm31lzV2_Xj4KH_c_n9OZtsUXsz-XO7_2pxpHoihYKmm3cRgr7fSOkPajauhcqsh8OYjjrw-pmDblnNtVWTN-7r6pCitPjA7xKOsn8wqAfpS8b_CGb_75_85fD2-vddahiZWt5CUIc17yKLFrTLmBP4Gbc_DecHPtjbK6AQ0bRIO0zaQfwFGVfGoYv5HRUcWdAzuhqmL3Zyy8-o0_5-6mGzsrJOBmGuNDss6qBAk9wzc5yGPphj2B-KThXCZE-skKFLbYRwR-FGPEFW7TJEcEDzvHj-G5M1YD8VMYClHSd-Vtj216mLU74x46xtE1McS22FwY4BQdmUzr_GNX46jK7aEOBK7A0tem9yVkn3EaChgdWwVogY8mo3KDUYTOQCGDpe7NX35fKNBrMTSP6KDHNoJbByKp6_3NmkFvp8mWpVbAgbLCWxnfw0WSQlg88hzvAZ-3QFrdYDELEb4I7gtnk5dRzmHHOGpNtRU5D4WI3dxuUzgKWZiShamsc8xK1Q_z8zOITcL-9RW7qDsV5-6JhmiVKHoiIGcFo0Lq2qAQ.aD99KR4F_tJOM02GQ9mf4w/__results___files/__results___2_1.png

---

## Installation

### 1. Install Tesseract OCR

#### Windows
1. Download from:
   https://github.com/UB-Mannheim/tesseract/wiki
2. Install to:
   ```
   C:\Program Files\Tesseract-OCR\
   ```
3. Ensure **“Add to PATH”** is checked during installation.

Verify:
```bash
tesseract --version
```

#### Linux (Ubuntu)
```bash
sudo apt update
sudo apt install tesseract-ocr
```

#### macOS
```bash
brew install tesseract
```

---

### 2. Install Python Dependencies

```bash
pip install pytesseract opencv-python
```

---

## Configuration

### Update Tesseract Path (Windows only)

Inside `demo_tesseract.py`:

```python
pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"
```

### Update Image Path

```python
img = cv2.imread("demo_image.png")
```

Ensure the image path is correct.

---

## Running the Project

From the project directory:

```bash
python demo_tesseract.py
```

---

## Output

### Console Output
```
Email: example@email.com
```

### Visual Output
- Green bounding box drawn around detected email text in the image

---

## Limitations

- OCR accuracy depends on image quality
- Not suitable for handwritten text
- Sensitive to blur and low resolution images

---

## Future Enhancements

- Image preprocessing for better accuracy
- Batch processing multiple images
- Export results to CSV or Excel
- Detection of phone numbers, dates, and addresses

---

## License

This project is released under the MIT License and is free to use for educational and demonstration purposes.
