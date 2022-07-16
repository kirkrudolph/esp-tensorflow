# For more information about build system see
# https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html
# The following five lines of boilerplate have to be in your project's
# CMakeLists in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.5)

include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(esp-tensorflow C CXX)

set(TENSORFLOW_SOURCE_DIR "tensorflow" CACHE PATH
  "Directory that contains the TensorFlow project" )

add_subdirectory(
    "${TENSORFLOW_SOURCE_DIR}/tensorflow/lite"
    "${CMAKE_CURRENT_BINARY_DIR}/tensorflow-lite" EXCLUDE_FROM_ALL)

target_link_libraries(esp-tensorflow tensorflow-lite)