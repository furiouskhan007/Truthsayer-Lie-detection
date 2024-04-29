# A Remote-Control Lie Detector
* Truthsayer lets you monitor the heart rate and possible 'tells' of deception from any face, including live video calls or recordings.
* TruthSayer uses OpenCV and MediaPipe's Face Mesh to perform real-time detect of facial landmarks from video input. It also uses FER for mood detection. From there, relative differences are calculated to determine significant changes in specific facial movements from a person's baseline, including their:

* Heart rate
* Blink rate
* Change in gaze
* Hand covering face
* Lip compression
# Python Compatibility 
* Python 3.10.4

## Libraries Used
1. pip install mediapipe
2. pip install tensorflow
3. pip install ffpyplayer
4. pip install fer
5. pip install mss

## Usage
The following command can be used to run the web app.<br>
```python intercept.py --input 0```<br>
```python intercept.py --input 0 --landmarks 1 --flip 1 --bpm BPM --ttl TTL```<br>
```python intercept.py --input 2 --landmarks 1 --flip 1 --record 1``` - Camera device 2; overlay landmarks; flip; generate a recording<br>
```python intercept.py -i "/Downloads/shakira.mp4" --second 0``` - Use video file as input; use camera device 0 as secondary input for mirroring feedback<br>

## Optional flags:
* --help - Display the below options
* --input - Choose a camera, video file path, or screen dimensions in the form x y width height - defaults to device 0
* --landmarks - Set to any value to draw overlayed facial and hand landmarks
* --bpm - Set to any value to include a heart rate tracking chart
* --flip - Set to any value to flip along the y-axis for selfie view
* --landmarks - Set to any value to draw detected body landmarks from MediaPipe
* --record - Set to any value to write the output to a timestamped AVI recording in the current folder
* --second - Secondary video input device for mirroring prompts (device number or path)
* --ttl - Number of subsequent frames to display a tell; defaults to 30

