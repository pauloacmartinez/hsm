enable_testing()
add_executable(front front.cpp)
target_link_libraries(front hsm)
add_executable(back back.cpp)
target_link_libraries(back hsm)
add_executable(alg alg.cpp)
target_link_libraries(alg hsm)
add_executable(sort sort_test.cpp)
target_link_libraries(sort hsm)

add_executable(alg_test alg_test.cpp)
target_link_libraries(alg_test hsm Catch2::Catch2)
add_test(NAME alg_test COMMAND alg_test)

add_executable(alg_test_unrolled alg_test_unrolled.cpp)
target_link_libraries(alg_test_unrolled hsm Catch2::Catch2)
add_test(NAME alg_test_unrolled COMMAND alg_test_unrolled)

add_executable(test_flatten_sm test_flatten_sm.cpp)
target_link_libraries(test_flatten_sm hsm Catch2::Catch2)
add_test(NAME test_flatten_sm COMMAND test_flatten_sm)
