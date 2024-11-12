# Ex: 13 AI MINI PROJECT - Real-time Drowsiness Detection System using Facial Landmarks
### DATE:   04/11/24                                                         
### REGISTER NUMBER : 212221040168
### AIM: 
To develop a machine learning model for the Real-time Drowsiness Detection System using Facial Landmarks. 
###  Algorithm:

1. The system starts with an input image.

2. The input image undergoes pre- processing to enhance features.

3. The region of interest (ROI) is identified, usually the driver's face.

4. Eye detection techniques are applied to locate the eyes within the ROI.

5. A bounding box is drawn around the detected eyes.

6. The system tracks the movement of the eyes within the bounding box.

7. Drowsiness is recognized based on eye movement patterns and other cues.
        
8. If drowsiness is detected, a drowsiness alert is triggered.

### Program:

```
# Main loop for real-time processing
while True:
    ret, frame = cap.read()
    height, width = frame.shape[:2]
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
    # Detecting faces and eyes
    faces = face.detectMultiScale(gray, minNeighbors=5, scaleFactor=1.1,   						minSize=(25, 25))
    left_eye = leye.detectMultiScale(gray)
    right_eye = reye.detectMultiScale(gray)
    # Loop through detected eyes
    for (x, y, w, h) in right_eye:
        # Preprocess right eye for model input
        # Predict eye state (open or closed)
        break
    for (x, y, w, h) in left_eye:
        # Preprocess left eye for model input
        # Predict eye state (open or closed)
        break

```
```

 # Calculating score based on eye states
    if rpred[0] == 0 and lpred[0] == 0:
        score += 1
        # Display "Closed" when eyes are closed
    else:
        score -= 1
        # Display "Open" when at least one eye is open
    # Display score on the frame
    # If score crosses a threshold, trigger alarm and mark frame
    # Display frame with relevant information
    cv2.imshow('frame', frame)
    # Exit loop when 'q' is pressed
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
# Release video capture and close all windows
cap.release()
cv2.destroyAllWindows()
```

### Output:
Eyes opened


Eyes closed


### Result:
The model achieved a satisfactory level of accuracy, demonstrating its capability in predicting the specified target outcome.
