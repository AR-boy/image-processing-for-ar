cmake_minimum_required(VERSION 3.0.0)

set(TESTS_NAME ExampleTests)

#file(GLOB TEST_SOURCES ${PROJECT_SOURCE_DIR}/test/*.ccp)

add_executable(${TESTS_NAME}  ${PROJECT_SOURCE_DIR}/test/ExampleTests)

target_link_libraries(${TESTS_NAME} PUBLIC
    gtest_main
    IM_AR
)

add_test(
    NAME ${TESTS_NAME}
    COMMAND ${TESTS_NAME}
)
