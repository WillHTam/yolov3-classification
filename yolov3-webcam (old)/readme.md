- create environment
`conda env create -f environment.yml`
`conda activate webcam_env`

- get yolo weights
`wget https://pjreddie.com/media/files/yolov3.weights`

- convert darknet yolo model to keras model
`python convert_to_keras.py model_data/yolov3.cfg model_data/yolov3.weights model_data/yolo_weights.h5`

- activate
`python webcam_detect.py`

~1 FPS on CPU, ~15 on GPU
