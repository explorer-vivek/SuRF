find_package(Threads REQUIRED)
find_package(GTest REQUIRED)

function (add_surf_test file_name )
  add_executable(${file_name} ${file_name}.cpp)
  target_link_libraries(${file_name} GTest::GTest)
  add_test(NAME ${file_name} COMMAND ${CMAKE_CURRENT_BINARY_DIR}/${file_name})
endfunction()

add_subdirectory(unitTest)