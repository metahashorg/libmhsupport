add_custom_target(cmake_modules SOURCES MHSupportConfig.cmake.in)

include(CMakePackageConfigHelpers)
configure_package_config_file(MHSupportConfig.cmake.in ${CMAKE_BINARY_DIR}/MHSupportConfig.cmake
                              INSTALL_DESTINATION lib/cmake/MHSupport)

install(FILES ${CMAKE_BINARY_DIR}/MHSupportConfig.cmake DESTINATION lib/cmake/MHSupport CONFIGURATIONS Release)
