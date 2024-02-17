# Assignment-AI-ML
Multipara Monitor Data Extraction

This Python code extracts and displays numeric data from multipara patient monitors captured in a video feed. It allows getting heart rate and oxygen saturation values from varying models of monitors in a non-invasive manner using computer vision and optical character recognition techniques.
Overview

The code loads a template image of a sample monitor display layout to use as reference. As video frames are captured from the webcam feed, template matching is used to identify the monitor screen in each frame. Once detected, predefined regions of interest are cropped from the monitor display to isolate the data values. These cropped images are passed to an OCR engine (PyTesseract) which extracts the numeric text. The text is converted to integer values and printed to the console.

The key steps are:

    Load monitor template
    Capture video frames
    Detect monitor in frames via template matching
    Crop regions of interest (heart rate, SpO2 etc)
    Apply OCR to cropped regions
    Extract numeric values
    Print values

Usage

The following dependencies need to be installed:

    OpenCV
    PyTesseract
    Numpy

A sample monitor template image is required, such as monitor_template.jpg.

The path to the Tesseract OCR executable must be configured in the code.

A webcam connected to the computer is required to capture video frames.

The code can simply be run as:

python monitor_data.py

Position the camera with a clear view of the monitor display. The program will continuously extract and display heart rate and oxygen saturation values from the feed.
Customization

    The template matching method can be tuned for improved monitor detection.
    The regions of interest can be configured to work with different monitor models.
    Preprocessing steps like blurring or thresholding can improve OCR accuracy.
    Error handling should be added for invalid or missing data.
    The extracted values can be logged to a file or database.

Conclusion

This code serves as a basic template for non-invasively capturing and digitizing data from medical monitors using computer vision techniques. It can be extended and customized for use in telemedicine applications to remotely monitor patient vital signs.
