cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  WFSOExThreadTest.c
)

add_executable(paltest_waitforsingleobject_wfsoexthreadtest
  ${SOURCES}
)

add_dependencies(paltest_waitforsingleobject_wfsoexthreadtest CoreClrPal)

target_link_libraries(paltest_waitforsingleobject_wfsoexthreadtest
  pthread
  rt
  m
  CoreClrPal
)
