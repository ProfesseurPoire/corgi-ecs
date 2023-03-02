project(TestECS)

enable_testing()

add_executable(${PROJECT_NAME} src/TestECS.cpp)

target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/../../../ext/boost/include)

find_package(corgi-test)

target_link_libraries(${PROJECT_NAME}
    PUBLIC
    corgi-ecs
    corgi-test)

set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 20)
