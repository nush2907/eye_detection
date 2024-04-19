# eye_detection
he model described in the provided code snippets is designed to detect malpractice in video streams, such as those captured during exams or tests. It operates by analyzing video frames to identify and flag potential instances of cheating or malpractice. Here's a brief overview of what the model does:

1. Face Detection
The model uses a pre-trained Haar cascade classifier for face detection. This classifier is capable of identifying human faces in images or video frames. By detecting faces, the model can then analyze the behavior associated with each face to look for signs of malpractice.

2. Multiple Faces Detection
If more than one face is detected in a frame, the model flags this as potential malpractice. The assumption here is that having multiple faces in a single frame could indicate that someone is trying to cheat by having someone else look at the answers or questions.

3. Movement Detection
The model also attempts to detect sudden movements in the video frames. This is based on the difference between consecutive frames. If a significant change is detected, it could indicate that someone is trying to cheat by moving around or using external aids.

4. Eye Aspect Ratio (EAR) Calculation
For each detected face, the model calculates the Eye Aspect Ratio (EAR), which is a measure of the openness of the eyes. If the eyes are open, it could indicate that the person is awake and not sleeping during the test, which might be considered malpractice.

5. Malpractice Detection
Based on the criteria mentioned above (multiple faces, movement, and eyes being open), the model flags a frame as containing malpractice if any of these conditions are met. This is a binary classification problem, where the model predicts whether a given frame contains malpractice or not.
