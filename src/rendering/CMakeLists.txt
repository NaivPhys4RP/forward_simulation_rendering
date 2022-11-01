project(rs_naivphs4r_rendering)

rs_add_library(rs_naivphs4r_Renderer src/Renderer.cpp)
target_link_libraries(rs_naivphs4r_Renderer rs_core)

#if(X_FOUND)
# rs_add_library(rs_CaffeAnnotator src/CaffeAnnotator.cpp)
# target_link_libraries(rs_CaffeAnnotator rs_core rs_caffeProxy)
#endif()

rs_add_executable(Renderer src/Renderer.cpp)
target_link_libraries(Renderer rs_naivphs4r_rendering ${catkin_LIBRARIES})
