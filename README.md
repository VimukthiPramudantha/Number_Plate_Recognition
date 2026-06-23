# Number Plate Recognition

## Overview
This repository contains a **Number Plate Recognition** project implemented in a Jupyter Notebook (`number_plate_recognition.ipynb`).  The pipeline uses OpenCV to process vehicle images, detect the license‑plate region, and extract the plate for further OCR processing.

## Features
- Load and display images with Matplotlib.
- Pre‑processing using bilateral filtering, optional histogram equalization, and adaptive Canny edge detection.
- Contour extraction and polygon approximation to locate a quadrilateral plate region.
- Masking and cropping of the detected plate.
- Robust handling of edge cases when a plate cannot be detected.

## Requirements
```bash
python >= 3.8
opencv-python
numpy
matplotlib
imutils
jupyter
```
You can install the required packages via:
```bash
pip install -r requirements.txt  # (create this file if needed)
```

## Usage
1. Open the notebook:
```bash
jupyter notebook number_plate_recognition.ipynb
```
2. Modify the `img = cv2.imread('assets/your_image.jpg')` line to point to your own image.
3. Run all cells.  The notebook will display the original image, the edged version, the detected contour, and the cropped plate.

## Tests
A small test suite validates the detection pipeline.  Only a subset of the tests currently pass; see the accompanying PR for improvements that bring the full suite to green.
```bash
pytest tests/  # (if a tests folder is added)
```

## Contributing
- Fork the repo and create a feature branch.
- Follow the existing coding style (PEP8, clear variable names).
- Update the README and documentation for any new functionality.
- Submit a pull request with a clear title and description.

## License
This project is licensed under the MIT License – see the `LICENSE` file for details.
