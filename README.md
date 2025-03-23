## Detect whether a user is blinking or whether they are drowsy in real-time ##

This project implements a real-time eye drowsiness detection system using Python, OpenCV, Dlib, and Numpy. The program captures video from the webcam, detects the user's face and eyes, and calculates the eye aspect ratio (EAR) to monitor drowsiness levels based on eye blinks or whether they are blinking at the moment. You can customize parameters such as the number of frames for which the user appears to be dull, which when exceeded triggers a drowsy alert, the minimum eye aspect ratio, below which the user is perceived to be blinking, and the minimum eye aspect ratio for drowsiness which allows the program more leeway to detect whether a user has sustained droopy eyelids.

### Crux of the program: ###

1. **Video Capture**: Opens the webcam and reads frames.
2. **Face Detection**: Uses Dlib's frontal face detector to locate faces in the frame.
3. **Eye Aspect Ratio Calculation**: For each detected face, computes the EAR for both eyes.
4. **Drowsiness Detection**:
    1) Displays a message if the user is found to be blinking.
    2) Increments a counter if the user appears drowsy.
    3) If drowsiness is detected for more than the allowed frames, an alert is displayed and the counter reset.
5. **Real-time Display**: Shows the live feed with contours around the eyes and messages indicating the state of the user.
6. **Exiting the Program**: The application can be exited by pressing q.

