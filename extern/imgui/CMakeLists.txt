project(imgui CXX)

# dear imgui
set(IMGUI_SOURCE_FILES
  imgui.cpp
  imgui_draw.cpp
  imgui_widgets.cpp
  imgui_tables.cpp
  backends/imgui_impl_glfw.cpp
  backends/imgui_impl_opengl2.cpp)

set(IMGUI_HEADER_FILES
  imconfig.h
  imgui.h
  imgui_internal.h
  imstb_rectpack.h
  imstb_textedit.h
  imstb_truetype.h
  backends/imgui_impl_glfw.h
  backends/imgui_impl_opengl2.h)

add_library(imgui STATIC ${IMGUI_SOURCE_FILES} ${IMGUI_HEADER_FILES})
target_include_directories(imgui PUBLIC .)
#target_include_directories(imgui PUBLIC ..)
target_include_directories(imgui PRIVATE ../glfw/include)
target_include_directories(imgui PRIVATE ../glad/include)
