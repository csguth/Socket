include_directories(..)

add_executable(tcp_receiver tcp_receiver.cpp)
add_executable(tcp_sender tcp_sender.cpp)
add_executable(udp_receiver udp_receiver.cpp)
add_executable(udp_sender udp_sender.cpp)

add_custom_command(
    TARGET udp_sender POST_BUILD
    COMMAND ln -sf ${CMAKE_CURRENT_SOURCE_DIR}/input.bmp ${CMAKE_CURRENT_BINARY_DIR}/input.bmp
)
