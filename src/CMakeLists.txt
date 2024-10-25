cmake_minimum_required(VERSION 3.6.0)
add_library(allocator INTERFACE)
add_library(container INTERFACE)

# Добавляем include директорию с заголовочными файлами
target_include_directories(allocator INTERFACE ../include)
target_include_directories(container INTERFACE ../include)

# Делаем так, чтобы container зависел от allocator
target_link_libraries(container INTERFACE allocator)