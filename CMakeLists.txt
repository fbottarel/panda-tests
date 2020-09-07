cmake_minimum_required(VERSION 3.4)

project(panda-tests
        LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 11)

## Find dependencies
find_package(Franka REQUIRED)
find_package(Eigen3 REQUIRED)


add_executable(test_zerotorque src/examples_common.h src/examples_common.cpp src/test_zerotorque.cpp)
target_link_libraries(test_zerotorque PRIVATE Franka::Franka Eigen3::Eigen)
