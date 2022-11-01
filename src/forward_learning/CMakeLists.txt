project(rs_naivphs4r_forward_learning)

rs_add_library(rs_naivphs4r_ForwardLearner src/ForwardLearner.cpp)
target_link_libraries(rs_naivphs4r_forward_learning rs_core)

#if(X_FOUND)
# rs_add_library(rs_CaffeAnnotator src/CaffeAnnotator.cpp)
# target_link_libraries(rs_CaffeAnnotator rs_core rs_caffeProxy)
#endif()

rs_add_executable(ForwardLearner src/ForwardLearner.cpp)
target_link_libraries(ForwardLearner rs_naivphs4r_forward_learning ${catkin_LIBRARIES})
