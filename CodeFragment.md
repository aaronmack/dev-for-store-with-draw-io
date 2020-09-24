### [vulkan_env]
if(WIN32)
    set(VULKAN_SDK_ROOT C:/Vulkan1.2.148.1)
    set(GLFW_ROOT C:/GLFW-WIN64)
    include_directories(${CMAKE_CURRENT_LIST_DIR}/includes)
    include_directories(${VULKAN_SDK_ROOT}/Include)
    include_directories(${GLFW_ROOT}/include)

    link_libraries(${VULKAN_SDK_ROOT}/Lib/vulkan-1.lib)
    link_libraries(${GLFW_ROOT}/lib/glfw3dll.lib)
else()
    set(VULKAN_SDK_ROOT /Vulkan1.2.148.1)
endif()
### [vulkan_env]

add_subdirectory(src)
