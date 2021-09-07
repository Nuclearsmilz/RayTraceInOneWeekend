
cmake_minimum_required ( VERSION 3.1.0 )

project ( RTWeekend
  VERSION 1.0.0
  LANGUAGES CXX
)

# Set to c++11
set ( CMAKE_CXX_STANDARD 17 )

# Source
set ( COMMON_ALL
  #src/common/rtweekend.h
  src/common/camera.h
  src/common/ray.h
  src/common/vec3.h
)

set ( SOURCE_ONEWEEKEND
  ${COMMON_ALL}
  #src/RayTraceInOneWeekend/hittable.h
  #src/RayTraceInOneWeekend/hittable_list.h
  #src/RayTraceInOneWeekend/material.h
  #src/RayTraceInOneWeekend/sphere.h
  src/RayTraceInOneWeekend/main.cpp
)

# Executables
add_executable(inOneWeekend      ${SOURCE_ONE_WEEKEND})

include_directories(src/common)