Trigonometric Pose Estimation and Correction

Overview
This project proposes a methodology that efficiently utilizes posture information in terms of identified landmarks using MediaPipe and then exploits OpenCV to compute the angles used as thresholds for verifying the correctness of postures.

Architecture
The initial stage of implementation starts with setting up OpenCV for processing the input (image/video/livestream) and MediaPipe for the detection of body landmarks. The landmarks are then converted into spatial coordinates to compute joint angles necessary for each exercise.

For the initial phase of the project, users must capture a video of themselves completing a certain exercise from a specific angle of view (front side, rear side, etc.) so that the activity can be adequately viewed. There are no constraints on the distance from the camera or the type of camera; the only requirement is that the user's posture is clearly apparent.
Once the prerequisites are set up, exercise-specific algorithms are presented to evaluate the exercise performed by the user. Our proposed approach includes maximum angles for accurately identifying the angle measures from an individual's specific posture to attain 
desirable accuracy for extending guidance on posture correction.

Exercise-Specific Algorithms
A. Planks
Plank is an isometric exercise where one contracts their muscles and holds them in one position. Planks help stabilize the spine and maintain correct upright posture. The main angles involved in the plank exercise are shoulder, elbow, hip, and ankle angles.
Conditions for correct plank posture:
1.	Shoulder angle: 65 to 95 degrees.
2.	Elbow angle: 70 to 100 degrees.
3.	Hip angle: 135 to 175 degrees.
4.	Ankle angle: 70 to 120 degrees.

B. Squats
Squats are functional exercises that can boost calorie burn when performed correctly. Squats involve flexing at the hip, knee, and ankle joints and bending to the desired squat depth.
Conditions for correct squat posture:
1.	Ankle angle: 105 to 120 degrees.
2.	Hip angle: More than 60 degrees.
3.	Trunk angle: Maintain an upright posture.
4.	Knee angle: 45 to 75 degrees.

C. Shoulder Press
Shoulder Press is an important upper-body exercise that targets the shoulder muscles and helps build shoulder strength. The main body components involved in the shoulder press are the back and the arms.
There are two states during the exercise: State 1 (lower state) and State 2 (upper state).
State 1 angle criteria:
•	Elbow angle: 55 to 75 degrees.
•	Shoulder angle: 85 to 105 degrees.
State 2 angle criteria:
•	Shoulder angle: 145 to 165 degrees.
•	Elbow angle: 125 to 140 degrees.

