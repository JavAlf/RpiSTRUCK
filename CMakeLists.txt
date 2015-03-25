project(STRUCK)

cmake_minimum_required(VERSION 2.6)

find_package(OpenCV REQUIRED)

set(CMAKE_BUILD_TYPE Release)

INCLUDE_DIRECTORIES ( src/GraphUtils /usr/include/eigen2 ${OpenCV_INCLUDE_DIRS})

add_executable(STRUCK
    Config.cpp
    Features.cpp
    HaarFeature.cpp
    HaarFeatures.cpp
    HistogramFeatures.cpp
    ImageRep.cpp
    LaRank.cpp
    main.cpp
    MultiFeatures.cpp
    RawFeatures.cpp
    Sampler.cpp
    Tracker.cpp
    GraphUtils.cpp
    )

target_link_libraries(STRUCK ${OpenCV_LIBS})
