add_library(Logger STATIC)
add_library(Watchdog STATIC)
target_sources(Logger PRIVATE src/Logger.cpp)
target_sources(Watchdog PRIVATE src/(WatchdogWrapper.cpp)
target_include_directories(Logger PUBLIC include)
target_include_directories(WatchdogWrapper PUBLIC include)
target_set_mbed_dependency(Logger)
target_set_mbed_dependency(WatchdogWrapper)

add_library(LookupTable INTERFACE)
target_include_directories(LookupTable INTERFACE include)
              