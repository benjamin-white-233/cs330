cmake_minimum_required(VERSION 3.18)

add_subdirectory(external/glfw)
add_subdirectory(external/glm)

add_executable(${PROJECT_NAME} src/main.cpp src/shader.cpp src/glad.c)

target_include_directories(${PROJECT_NAME}
        PRIVATE
        glm
        glfw
        external/GLAD
        )

target_link_libraries(${PROJECT_NAME}
        PRIVATE
        glm
        glfw
        )