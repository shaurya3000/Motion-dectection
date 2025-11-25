# Motion Detection using OpenCV

This is a simple computer vision project that detects motion through the webcam.
Whenever something moves in front of the camera, the program marks the moving area with a rectangle.
It is a basic demonstration of real-time motion tracking using OpenCV.

## Requirements

- Python 3
- OpenCV

Install OpenCV using:
pip install opencv-python

## How to Run

Make sure your webcam is connected, then run:
python Motion.py

## How it works

- The webcam captures video frames continuously.
- A background subtractor (cv2.createBackgroundSubtractorMOG2) creates a model of the static scene.
- Each new frame is compared with the background to find changes.
- Noise is reduced using thresholding, erosion, and dilation.
- Contours are detected on the processed mask.
- Rectangles are drawn around contour regions that are large enough to be considered motion.
