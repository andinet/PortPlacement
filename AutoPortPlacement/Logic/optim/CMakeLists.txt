# build NLOpt
add_subdirectory(nlopt)
include_directories(${nlopt_INCLUDE_DIRS})

add_library(optim STATIC optim.cxx)

target_link_libraries(optim
  ${VTK_LIBRARIES}
  davinci
  nlopt)
