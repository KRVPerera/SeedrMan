
add_executable(test2 integration_tests.cpp)
MESSAGE(${CONAN_LIBS})
target_link_libraries(test2 PRIVATE Catch2WithMain ${CONAN_LIBS} SeedrMan)
target_include_directories(test2 PRIVATE ${CMAKE_SOURCE_DIR}/include)



