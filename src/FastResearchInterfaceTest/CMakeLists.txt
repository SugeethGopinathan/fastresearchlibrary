include_directories (${FriLibrary_SOURCE_DIR}/include)

add_executable(FastResearchInterfaceTest FastResearchInterfaceTest.cpp MoveToCandle.cpp RunTrajectorySimple.cpp)
target_link_libraries(FastResearchInterfaceTest TypeIRML FastResearchInterface ${LIBRARIES})
