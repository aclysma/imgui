cmake_minimum_required(VERSION 3.15)
project(prototype_app)

include_directories(../..)
include_directories(../../backends)
include_directories(/usr/local/include)
include_directories(/opt/local/include)
include_directories(/usr/local/include/SDL2)
link_directories(/usr/local/lib)

add_executable(prototype_app main.cpp ../../imgui.cpp ../../imgui_demo.cpp ../../imgui_draw.cpp ../../imgui_tables.cpp ../../imgui_widgets.cpp ../../backends/imgui_impl_sdl.cpp ../../backends/imgui_impl_opengl3.cpp)

target_link_libraries(prototype_app SDL2)
target_link_libraries(prototype_app "-framework OpenGL")
target_link_libraries(prototype_app "-framework Cocoa")
target_link_libraries(prototype_app "-framework IOKit")
target_link_libraries(prototype_app "-framework CoreVideo")
