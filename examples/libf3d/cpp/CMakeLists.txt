find_package(f3d REQUIRED COMPONENTS library)

if(BUILD_TESTING)
  enable_testing()
endif()

add_subdirectory(check-engine)
add_subdirectory(multi-files)
add_subdirectory(render-image)
add_subdirectory(render-interact)
add_subdirectory(use-options-string)
add_subdirectory(use-options-struct)
add_subdirectory(use-options-variant)

option(F3D_EXAMPLES_EXTERNAL_GLFW "Enable external-glfw example (requires GLFW)" OFF)
if(F3D_EXAMPLES_EXTERNAL_GLFW)
  add_subdirectory(external-glfw)
endif()
