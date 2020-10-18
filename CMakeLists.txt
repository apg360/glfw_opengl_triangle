cmake_minimum_required(VERSION 3.18.X)
project(GLFWtriangle-opengl_Project LANGUAGES C)
add_executable(GLFWtriangle-opengl triangle-opengl.c)
target_compile_features(GLFWtriangle-opengl PRIVATE c_std_11)

# -----------------------------------------------------
# (*) brew install glfw3 --HEAD
# (*) LunarG SDK Vulkan

#Finding and linking GLFW3 (windowing, context & input)
find_package(GLFW3 3.3 REQUIRED)
if (GLFW3_FOUND)
    message("GLFW3 FOUND")
    target_link_libraries(GLFWtriangle-opengl glfw)
endif (GLFW3_FOUND)

#Linker need GLAD library
# https://gen.glad.sh generate GL.h << Use this website
# BUT https://glad.dav1d.de generate glad.h and does not work
# Remember Do not tick header only, the linker needs the C file
add_library(GLAD "libs/GLAD/gl.c")
target_link_libraries(GLFWtriangle-opengl GLAD)

#For include <GLAD/gl.h> in triangle-opengl.c
target_include_directories(GLFWtriangle-opengl
   PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/libs"
   )

