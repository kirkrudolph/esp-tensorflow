# ESP-TENSORFLOW

This idea didn't work. Tried to follow the [tensorflow instructions](https://www.tensorflow.org/lite/guide/build_cmake#create_a_cmake_project_which_uses_tensorflow_lite).


## CMake Build Error

```
CMake Warning at build/abseil-cpp/CMakeLists.txt:74 (message):
  A future Abseil release will default ABSL_PROPAGATE_CXX_STD to ON for CMake
  3.8 and up.  We recommend enabling this option to ensure your project still
  builds correctly.


CMake Warning at build/abseil-cpp/absl/copts/AbseilConfigureCopts.cmake:30 (message):
  Value of CMAKE_SYSTEM_PROCESSOR () is unknown and cannot be used to set
  ABSL_RANDOM_RANDEN_COPTS
Call Stack (most recent call first):
  build/abseil-cpp/CMake/AbseilHelpers.cmake:18 (include)
  build/abseil-cpp/CMakeLists.txt:85 (include)

-- Looking for pthread.h
-- Looking for pthread.h - found
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Failed
-- Looking for pthread_create in pthreads
-- Looking for pthread_create in pthreads - not found
-- Looking for pthread_create in pthread
-- Looking for pthread_create in pthread - not found
-- Check if compiler accepts -pthread
-- Check if compiler accepts -pthread - no
CMake Error at /Applications/CMake.app/Contents/share/cmake-3.23/Modules/FindPackageHandleStandardArgs.cmake:230 (message):
  Could NOT find Threads (missing: Threads_FOUND)
Call Stack (most recent call first):
  /Applications/CMake.app/Contents/share/cmake-3.23/Modules/FindPackageHandleStandardArgs.cmake:594 (_FPHSA_FAILURE_MESSAGE)
  /Applications/CMake.app/Contents/share/cmake-3.23/Modules/FindThreads.cmake:238 (FIND_PACKAGE_HANDLE_STANDARD_ARGS)
  build/abseil-cpp/CMakeLists.txt:110 (find_package)

-- Configuring incomplete, errors occurred!
cmake failed with exit code 1
```