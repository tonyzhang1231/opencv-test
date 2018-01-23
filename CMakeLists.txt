cmake_minimum_required(VERSION 2.8)
project( DisplayImage )
find_package( OpenCV REQUIRED )
include_directories( ${OpenCV_INCLUDE_DIRS} )

add_executable( DisplayImage DisplayImage.cpp )
target_link_libraries( DisplayImage ${OpenCV_LIBS} )


add_executable( how_to_scan_images how_to_scan_images.cpp )
target_link_libraries( how_to_scan_images ${OpenCV_LIBS} )


add_executable( yolo_object_detection yolo_object_detection.cpp )
target_link_libraries( yolo_object_detection ${OpenCV_LIBS} )
