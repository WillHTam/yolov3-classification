- activate environment
`conda env create -f yolo-<cpu/gpu>.yml`
`conda activate yolo-gpu`

- get yolo weights
`wget https://pjreddie.com/media/files/yolov3.weights`

- convert yolo model to tf model
`python convert_to_tf.py`

- run server
`python app.py`

with postman
post to localhost:5000/detection or /image
then submit with body of
key: images, type: file
and select an image

# also possible directly with
`python detect.py --images "data/images/dog.jpg, data/images/office.jpg"`

# webcam
`python detect_video.py --video 0`

# video file
`python detect_video.py --video data/video/paris.mp4 --weights ./weights/yolov3.tf`

# video file with output saved (can save webcam like this too)
`python detect_video.py --video path_to_file.mp4 --output ./detections/output.avi`


https://github.com/zzh8829/yolov3-tf2
