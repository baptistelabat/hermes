

list(APPEND tests
        test_hermes
        test_eigenVectorsSerialization
        test_serializerDestructor
        )

message(STATUS "Hermes tests...")
foreach(test ${tests})
    message(STATUS "   ...${test}")
    add_executable(${test} "${test}.cpp")
    target_link_libraries(${test} hermes)
endforeach()
