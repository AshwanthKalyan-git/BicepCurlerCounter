Bicep Curl Counter Using Mediapipe and OpenCV

Overview

This project is a real-time bicep curl counter built with Python, Mediapipe, and OpenCV. It leverages pose detection to track arm movements, calculate elbow joint angles, and count repetitions for both the left and right arms. The application also displays the current stage of the curl ("up" or "down") for each arm, making it a valuable tool for fitness enthusiasts.

Features

Real-Time Pose Detection: Tracks body landmarks using Mediapipe’s Pose solution.

Dynamic Angle Calculation: Computes the angle of the elbow joint to determine movement stages.

Repetition Counter: Separate counters for the left and right arms to track bicep curls independently.

Stage Display: Indicates whether the arm is in the "up" or "down" phase of the curl.

Interactive Visualization: Displays the current angle, counters, and stages directly on the video feed.

README.md : Documentation for the project.

How It Works

Pose Detection: Mediapipe’s Pose solution identifies body landmarks in real-time.

Angle Calculation: The script calculates the angle between the shoulder, elbow, and wrist to determine the arm’s position.

Counting Logic:

If the elbow angle exceeds 160°, the stage is set to "down."

If the elbow angle drops below 40° and the stage is "down," a repetition is counted, and the stage changes to "up."

Visualization: OpenCV overlays the counters, angles, and stages on the video feed.

Customization

Adjust the angle thresholds (160° for "down" and 40° for "up") in the code to suit different exercises.

Modify the display colors and text positions in the OpenCV rendering logic.

Acknowledgments

Mediapipe by Google for the pose detection library.

OpenCV for computer vision capabilities.


