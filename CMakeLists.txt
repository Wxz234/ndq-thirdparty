file(GLOB IMGUI_FILE "imgui/*.cpp" "imgui/*.h")
add_library(imgui STATIC ${IMGUI_FILE})
target_include_directories(imgui PUBLIC "imgui")
set_target_properties(imgui PROPERTIES FOLDER "libraries")

set(NDQ_DXCOMPILER_INCLUDE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/DirectXShaderCompiler/inc" CACHE STRING "NDQ_DXCOMPILER_INCLUDE_DIR")
set(NDQ_DXCOMPILER_DLL "${CMAKE_CURRENT_SOURCE_DIR}/DirectXShaderCompiler/bin/x64/dxcompiler.dll" CACHE STRING "NDQ_DXCOMPILER_DLL")

add_subdirectory(DirectX-Headers)
set_target_properties(DirectX-Headers PROPERTIES FOLDER "libraries")
set_target_properties(DirectX-Guids PROPERTIES FOLDER "libraries")
