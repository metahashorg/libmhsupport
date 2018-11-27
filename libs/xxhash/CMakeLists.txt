set(LIB xxhash)

include_directories(.)

#Library
add_library(mh_${LIB} STATIC xxhash.c xxhash.h)

#Install
install(TARGETS mh_${LIB} ARCHIVE DESTINATION lib/mh)
install(FILES xxhash.h DESTINATION include/mh/${LIB} CONFIGURATIONS Release)
