project(SDLTemplate LANGUAGES CXX VERSION 0.0.1)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR})

add_executable(${PROJECT_NAME})
target_sources(${PROJECT_NAME} PRIVATE main.cpp Window.h Window.cc)
target_link_libraries(${PROJECT_NAME} PRIVATE
  SDL3::SDL3 
  SDL3_image::SDL3_image
)

target_compile_options(${PROJECT_NAME} PRIVATE -Wall)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_23)