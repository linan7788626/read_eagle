# Specify location of read_eagle library
include_directories(${CMAKE_BINARY_DIR}/include/)
link_directories(${CMAKE_BINARY_DIR}/lib/)

# Create the example executable
add_executable(read_eagle_f90_example example.f90)

# Link to read_eagle library
target_link_libraries(read_eagle_f90_example read_eagle)

# Put executable in bin dir. if we "make install"
install (TARGETS read_eagle_f90_example DESTINATION bin)
