add_library(stdext-path::stdext-path ALIAS stdext-path)

hunter_add_package(GTest)
find_package(GTest CONFIG REQUIRED)

add_executable(stdext-path-test test.cpp)
target_link_libraries(stdext-path-test PUBLIC stdext-path::stdext-path GTest::main)

add_test(stdext-path-test stdext-path-test)

