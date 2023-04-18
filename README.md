# lbs-vision-app
Computer vision app to count people with REST endpoint for IoT

`pip install requirements`

Tested Windows 10 with a webcam on python 3.10
Run app with:
`$ py webcam.py -i 0 -m ./models/yolov7-tiny.onnx --use-flask`

## Optional run app with full version of Yolov7

Change directoy into the `models` directory and download the full non-tiny version of the [Yolov7 model here](https://drive.google.com/file/d/1QnzwuHUtpBpLALH8aayIbT-STESSpfKf/view?usp=share_link):


With optional full version of the Yolov7 model with:
`$ py webcam.py -i 0 -m ./models/yolov7.onnx --use-flask`


* Note if using the full larger Yolov7 model adjust the `-conf` arg to .1 else if using the tiny Yolo7 fine tune confidence levls higher as needed to prevent false positives. To fine tune the classification of objects keep restarting the app with the desired `--conf` or `-c` arg shown below:

`$ py webcam.py -i 0 -m ./models/yolov7.onnx --use-flask -c .1`