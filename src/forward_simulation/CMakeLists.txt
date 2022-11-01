project(rs_naivphs4r_forward_simulation)

rs_add_library(rs_naivphs4r_ForwardSimulator src/ForwardSimulator.cpp)
target_link_libraries(rs_naivphs4r_forward_simulation rs_core)

#if(X_FOUND)
# rs_add_library(rs_CaffeAnnotator src/CaffeAnnotator.cpp)
# target_link_libraries(rs_CaffeAnnotator rs_core rs_caffeProxy)
#endif()

rs_add_executable(ForwardSimulator src/ForwardSimulator.cpp)
target_link_libraries(ForwardSimulator rs_naivphs4r_forward_simulation ${catkin_LIBRARIES})
