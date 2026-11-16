cmake_minimum_required(VERSION 3.10)
project(LocalLRU CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Include headers

# Add executables
#add_executable(trading_demo
#    examples/trading_demo.cpp
#)
add_library(local_lru INTERFACE)
target_include_directories(local_lru INTERFACE ${PROJECT_SOURCE_DIR}/include)

# Link extra sources (lock-based cache, etc.)
#target_sources(local_lru PRIVATE
#    src/lock_cache.hpp
#)

# If curl is used for real-time data
#find_package(CURL REQUIRED)
#target_link_libraries(trading_demo PRIVATE CURL::libcurl)
