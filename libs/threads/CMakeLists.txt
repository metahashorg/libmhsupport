set(LIB threads)

include_directories(.)

#Custom target for headers only lib
add_custom_target(mh_${LIB} SOURCES spinlock.hpp)

#Install
install(FILES spinlock.hpp DESTINATION include/mh/${LIB} CONFIGURATIONS Release)
