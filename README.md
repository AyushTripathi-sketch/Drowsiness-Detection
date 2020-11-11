## INTRODUCTION

'NAP-BUZZER" is the title of our project. It includes detection of a Drowsing face while driving and activities including motion. A alarm will be setup which will quickly wake up the driver and automatic brakes would be installed to completely stop the vehicle on occurrence of such conditions.It will also restrict the driver from driving the vehicle if the drowsiness exceeds a specific number of time.
We are going to use a method to determine how long a given person’s eyes have been closed for. If there eyes have been closed for a certain amount of time, we’ll assume that they are starting to doze off and play an alarm to wake them up and grab their attention.

# The drowsiness detector algorithm
It will be implemented using OpenCV, dlib, and Python.First, we’ll setup a camera that monitors a stream for faces.If a face is found, we apply facial landmark detection and extract the eye regions.
A eye_aspect_ratio function will be defined to which is used to compute the ratio of distances between the vertical eye landmarks and the distances between the horizontal eye landmarks:
The return value of the eye aspect ratio will be approximately constant when the eye is open. The value will then rapid decrease towards zero during a blink.
If the eye is closed, the eye aspect ratio will again remain approximately constant, but will be much smaller than the ratio when the eye is open.

# Dataset
Shape_prediictor_68_face_ladndmarks
