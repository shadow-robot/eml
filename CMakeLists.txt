cmake_minimum_required(VERSION 2.8.3)
project(eml)

find_package(Threads)

include_directories(include)

add_library(${PROJECT_NAME} SHARED
    src/ethercat_AL.cxx
    src/ethercat_FSM.cxx
    src/ethercat_master.cxx
    src/ethercat_mbx.cxx
    src/ethercat_process_data.cxx
    src/ethercat_router.cxx
    src/ethercat_slave_conf.cxx
    src/ethercat_slave_handler.cxx
    src/ethercat_device_addressed_telegram.cxx
    src/ethercat_dll.cxx
    src/ethercat_frame.cxx
    src/ethercat_logical_addressed_telegram.cxx
    src/ethercat_slave_memory.cxx
    src/ethercat_telegram.cxx
    src/ethercat_posix_drv.cxx
)

target_link_libraries(${PROJECT_NAME} ${CMAKE_THREAD_LIBS_INIT})

install(TARGETS ${PROJECT_NAME}
   LIBRARY DESTINATION lib
)

install(DIRECTORY include/${PROJECT_NAME}
   DESTINATION include
)
