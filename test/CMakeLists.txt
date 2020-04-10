add_executable(test_main util.c util.h write_read.c write_read.h test.c)

add_test(NAME test_main COMMAND test_main WORKING_DIRECTORY ${PROJECT_BINARY_DIR}/lib)
target_link_libraries(test_main PRIVATE vorbisenc)
target_compile_definitions(test_main PRIVATE _USE_MATH_DEFINES)
