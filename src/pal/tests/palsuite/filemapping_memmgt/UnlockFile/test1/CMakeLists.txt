cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(TESTSOURCES
  test1.c
)

add_executable(paltest_unlockfile_test1
  ${TESTSOURCES}
)

add_dependencies(paltest_unlockfile_test1 CoreClrPal)

target_link_libraries(paltest_unlockfile_test1
  pthread
  rt
  m
  CoreClrPal
)


set(HELPERSOURCES
  helper.c
)

add_executable(paltest_unlockfile_test1_helper
  ${HELPERSOURCES}
)

add_dependencies(paltest_unlockfile_test1_helper CoreClrPal)

target_link_libraries(paltest_unlockfile_test1_helper
  pthread
  rt
  m
  CoreClrPal
)