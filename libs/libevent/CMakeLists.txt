set(LIB libevent)

include_directories(.)

#Library
add_library(mh_${LIB} STATIC LibEvent.h LibEvent.cpp)
target_compile_options(mh_${LIB} PRIVATE -Wno-unused-parameter -Wno-suggest-final-types)

#Install
install(TARGETS mh_${LIB} ARCHIVE DESTINATION lib/mh)
install(FILES LibEvent.h DESTINATION include/mh/${LIB} CONFIGURATIONS Release)
