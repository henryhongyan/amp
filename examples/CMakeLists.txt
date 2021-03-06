link_directories(${CMAKE_SOURCE_DIR}/src)
link_directories(${yaml-cpp_LIBRARY_DIRS})
list(APPEND LIBS amp)

set(SOURCES parse_urdf_example.cpp)
add_executable(parse_urdf_example ${SOURCES})
target_include_directories(parse_urdf_example SYSTEM PRIVATE ${Eigen_INCLUDE_DIRS})
target_include_directories(parse_urdf_example SYSTEM PRIVATE ${yaml-cpp_INCLUDE_DIRS})
target_include_directories(parse_urdf_example SYSTEM PRIVATE ${rbdl_INCLUDE_DIRS})
target_include_directories(parse_urdf_example SYSTEM PRIVATE ${kdtree_INCLUDE_DIRS})
target_include_directories(parse_urdf_example SYSTEM PRIVATE ${CMAKE_SOURCE_DIR}/contrib)
target_include_directories(parse_urdf_example PUBLIC ${CMAKE_SOURCE_DIR}/include)
target_link_libraries(parse_urdf_example ${LIBS})
install(TARGETS parse_urdf_example RUNTIME DESTINATION bin)

set(SOURCES inverse_kinematics_example.cpp)
add_executable(inverse_kinematics_example ${SOURCES})
target_include_directories(inverse_kinematics_example SYSTEM PRIVATE ${Eigen_INCLUDE_DIRS})
target_include_directories(inverse_kinematics_example SYSTEM PRIVATE ${yaml-cpp_INCLUDE_DIRS})
target_include_directories(inverse_kinematics_example SYSTEM PRIVATE ${rbdl_INCLUDE_DIRS})
target_include_directories(inverse_kinematics_example SYSTEM PRIVATE ${kdtree_INCLUDE_DIRS})
target_include_directories(inverse_kinematics_example SYSTEM PRIVATE ${CMAKE_SOURCE_DIR}/contrib)
target_include_directories(inverse_kinematics_example PUBLIC ${CMAKE_SOURCE_DIR}/include)
target_link_libraries(inverse_kinematics_example ${LIBS})
install(TARGETS inverse_kinematics_example RUNTIME DESTINATION bin)

set(SOURCES rrt_example.cpp)
add_executable(rrt_example ${SOURCES})
target_include_directories(rrt_example SYSTEM PRIVATE ${Eigen_INCLUDE_DIRS})
target_include_directories(rrt_example SYSTEM PRIVATE ${yaml-cpp_INCLUDE_DIRS})
target_include_directories(rrt_example SYSTEM PRIVATE ${rbdl_INCLUDE_DIRS})
target_include_directories(rrt_example SYSTEM PRIVATE ${kdtree_INCLUDE_DIRS})
target_include_directories(rrt_example SYSTEM PRIVATE ${CMAKE_SOURCE_DIR}/contrib)
target_include_directories(rrt_example PUBLIC ${CMAKE_SOURCE_DIR}/include)
target_link_libraries(rrt_example ${LIBS})
install(TARGETS rrt_example RUNTIME DESTINATION bin)

set(SOURCES jacobian_example.cpp)
add_executable(jacobian_example ${SOURCES})
target_include_directories(jacobian_example SYSTEM PRIVATE ${Eigen_INCLUDE_DIRS})
target_include_directories(jacobian_example SYSTEM PRIVATE ${yaml-cpp_INCLUDE_DIRS})
target_include_directories(jacobian_example SYSTEM PRIVATE ${rbdl_INCLUDE_DIRS})
target_include_directories(jacobian_example SYSTEM PRIVATE ${kdtree_INCLUDE_DIRS})
target_include_directories(jacobian_example SYSTEM PRIVATE ${CMAKE_SOURCE_DIR}/contrib)
target_include_directories(jacobian_example PUBLIC ${CMAKE_SOURCE_DIR}/include)
target_link_libraries(jacobian_example ${LIBS})
install(TARGETS jacobian_example RUNTIME DESTINATION bin)
#set(SOURCES trajectory_smoothing_test.cpp)
#add_executable(trajectory_smoothing_test ${SOURCES})
#target_link_libraries(trajectory_smoothing_test ${LIBS})
#if(DEFINED ENV{DLRRM_HOST_PLATFORM})
#    install(TARGETS trajectory_smoothing_test
#        RUNTIME DESTINATION ${CMAKE_SOURCE_DIR}/bin/$ENV{DLRRM_HOST_PLATFORM})
#else(DEFINED ENV{DLRRM_HOST_PLATFORM})
#    install(TARGETS trajectory_smoothing_test
#        RUNTIME DESTINATION ${CMAKE_SOURCE_DIR}/bin)
#endif(DEFINED ENV{DLRRM_HOST_PLATFORM})
