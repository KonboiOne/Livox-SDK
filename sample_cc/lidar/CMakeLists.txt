cmake_minimum_required(VERSION 3.0)

set(DEMO_NAME lidar_sample_cc)
add_executable(${DEMO_NAME} main.cpp lds_lidar.cpp)


add_executable(lidar_power lidar_power.cpp lds_lidar.cpp)


target_link_libraries(${DEMO_NAME}
        PRIVATE
        ${PROJECT_NAME}_static
        )


target_link_libraries(lidar_power
        PRIVATE
        ${PROJECT_NAME}_static
)
