cmake_minimum_required (VERSION 3.15)
project (TS)

# Search for directories simular to "trunk/po0xxyy/task_0x/src/"
file(GLOB V_GLOB RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} "trunk/po0*/*/src/")
foreach(item ${V_GLOB})
	message( "Find \"${item}\"" )
	add_subdirectory(${item})
endforeach()