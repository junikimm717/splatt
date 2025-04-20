find_package(BLAS REQUIRED)
find_package(LAPACK REQUIRED)

project(SPLATT_LIB)
cmake_minimum_required(VERSION 2.8.0)

add_library(splatt ${SPLATT_SOURCES})
target_link_libraries(splatt PRIVATE ${BLAS_LIBRARIES} ${LAPACK_LIBRARIES})

install(TARGETS splatt
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib
)
