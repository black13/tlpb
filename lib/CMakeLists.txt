set(lib_SRCS
    alt_functions.c
	error_functions.c
	get_num.c
	ename.c.inc
)

# Declare the library
add_library(lib STATIC
    ${lib_SRCS}
)

add_custom_command(
  OUTPUT ename.c.inc
  COMMAND bash ${CMAKE_CURRENT_SOURCE_DIR}/Build_ename.sh > ${PROJECT_SOURCE_DIR}/lib/ename.c.inc
)

# Specify here the include directories exported
# by this library
target_include_directories(lib PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)
