compile a cpp file using g++

g++ `pkg-config --cflags opencv` DisplayImage.cpp `pkg-config --libs opencv` -o DisplayImage


// libraries must be placed behind objects needing them since 11.10
// https://ubuntuforums.org/showthread.php?t=2051889


./DisplayImage <imagefilename>
./how_to_scan_images <imagefilename> 10

./yolo_object_detection   can deal with image video and webcam
https://docs.opencv.org/master/da/d9d/tutorial_dnn_yolo.html

Execute with image:
./yolo_object_detection -source=[PATH-IMAGE]  -cfg=[PATH-TO-DARKNET]/cfg/yolo.cfg -model=[PATH-TO-DARKNET]/yolo.weights   -class_names=[PATH-TO-DARKNET]/data/coco.names

e.g.
cd build
./yolo_object_detection -source=../data/apple.jpg -cfg=${DARKNET_PATH}/cfg/yolo.cfg -model=${DARKNET_PATH}/yolo.weights -class_names=${DARKNET_PATH}/data/coco.names

Execute in video file:

$ yolo_object_detection -source=[PATH-TO-VIDEO] -cfg=[PATH-TO-DARKNET]/cfg/yolo.cfg -model=[PATH-TO-DARKNET]/yolo.weights   -class_names=[PATH-TO-DARKNET]/data/coco.names

e.g.
cd build
./yolo_object_detection -source=../data/vtest.avi -cfg=${DARKNET_PATH}/cfg/yolo.cfg -model=${DARKNET_PATH}/yolo.weights -class_names=${DARKNET_PATH}/data/coco.names
