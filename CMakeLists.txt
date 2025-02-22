cmake_minimum_required(VERSION 3.31)
set(PROJECT_NAME BattelCity)
project(${PROJECT_NAME})

# Добавляем исполняемый файл
add_executable(${PROJECT_NAME} src/main.cpp)

# Устанавливаем параметры для GLFW
set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

# Добавляем подкаталог с GLFW
add_subdirectory(external/glfw)

# Связываем библиотеку GLFW с вашим проектом
target_link_libraries(${PROJECT_NAME} glfw)