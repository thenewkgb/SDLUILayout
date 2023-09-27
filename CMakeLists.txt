cmake_minimum_required(VERSION 3.6.0)
project(UILAYOUT)
include_directories(
	${PROJECT_SOURCE_DIR}/include
	${PROJECT_SOURCE_DIR}/src
)
file(GLOB SRCS
	"${PROJECT_SOURCE_DIR}/include/*"
	"${PROJECT_SOURCE_DIR}/src/*"
)
add_executable(UILAYOUT ${SRCS})
find_package(SDL2 REQUIRED)
target_link_libraries(UILAYOUT ${SDL2_LIBRARIES})