# License Plate Detection and Recognition

This project aims to detect and recognize license plates from images using image processing techniques and Optical Character Recognition (OCR). 

## Motivation

License plate recognition has numerous applications, including automated toll collection, traffic monitoring, parking management, and law enforcement. By automating the process of reading license plates, this project seeks to improve efficiency and accuracy in various scenarios.

## Methodology

1. **Image Preprocessing**: The input image is preprocessed to enhance features and reduce noise. This includes converting the image to grayscale, applying Gaussian blur to smooth edges, and detecting edges using the Canny edge detection algorithm.

2. **License Plate Detection**: After preprocessing, contours are identified in the image using the `cv2.findContours` function. The contours are then sorted based on their area in descending order. The contour with the largest area is considered as the potential license plate region.

3. **Text Recognition**: The identified license plate region is extracted from the original image. This region is then passed through an OCR engine, specifically the `easyocr` library, to read the text present on the license plate.

4. **Display Results**: The detected license plate region is outlined on the original image, and the recognized text is displayed alongside. If no text is detected, an appropriate message is displayed.

## Requirements

- Python 3.7 or higher
- Libraries: `easyocr`, `opencv-python`, `matplotlib`, `numpy`, `scipy`

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/license-plate-recognition.git
    cd license-plate-recognition
    ```

2. Install the required libraries:

    ```sh
    pip install easyocr opencv-python matplotlib numpy scipy
    ```

3. Ensure you have an image named `car11.jpg` in the project directory.

## Usage

1. Run the script:

    ```sh
    python main.py
    ```

2. The script will process the image, detect the license plate, and display the detected text.

## Limitations and Future Improvements

- Performance may vary depending on image quality, lighting conditions, and angle of the license plate.
- The current implementation may struggle with non-standard license plate formats or heavily distorted text.
- Future improvements could include training custom OCR models for better performance on license plates from specific regions or countries..
