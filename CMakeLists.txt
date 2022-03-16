
cmake_minimum_required(VERSION 3.5)
project(opengldev LANGUAGES CXX)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
add_executable(ImGui_single-board_OpenGL main.cpp)
target_link_libraries(ImGui_single-board_OpenGL glfw GLESv2)

add_compile_definitions(
    GLFW_INCLUDE_ES3=1
    IMGUI_IMPL_OPENGL_LOADER_CUSTOM=<GLFW/glfw3.h>
    IMGUI_IMPL_OPENGL_ES3=1)

# ImGui needs to be a subproject that would add the include paths, libs etc..

target_include_directories(ImGui_single-board_OpenGL PUBLIC imgui imgui/backends)
target_sources(ImGui_single-board_OpenGL PUBLIC
        imgui/imconfig.h
        imgui/imgui.cpp
        imgui/imgui.h
        imgui/imgui_demo.cpp
        imgui/imgui_draw.cpp
        imgui/imgui_internal.h
        imgui/imgui_tables.cpp
        imgui/imgui_widgets.cpp
        imgui/imstb_rectpack.h
        imgui/imstb_truetype.h
        imgui/backends/imgui_impl_glfw.cpp
        imgui/backends/imgui_impl_glfw.h
        imgui/backends/imgui_impl_opengl3.cpp
        imgui/backends/imgui_impl_opengl3.h)
