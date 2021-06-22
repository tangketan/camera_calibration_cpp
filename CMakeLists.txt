cmake_minimum_required(VERSION 3.5)
project(calibration_ceres)

find_package(gflags REQUIRED)
find_package(Ceres REQUIRED PATHS D:/ProgramFiles/Ceres)
find_package(OpenCV REQUIRED)
find_package(Eigen3 REQUIRED PATHS D:/ProgramFiles/Eigen3)

include_directories(${gflags_INCLUDE_DIR})

add_executable(${PROJECT_NAME}
	main.cpp
    class_camera_calibrator.hpp
    class_nonlinear_optimizer.hpp)

target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBRARIES} ${CERES_LIBRARIES})