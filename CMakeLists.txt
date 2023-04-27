set(headers
    TFT_eSPI.h
)

set(sources
    TFT_eSPI.cpp
)

set(dependencies
    arduino-esp32
    freertos
    esp_system

    cpputils
    espcpputils
    esptftlib
)

idf_component_register(
    INCLUDE_DIRS
        .
    SRCS
        ${headers}
        ${sources}
    REQUIRES
        ${dependencies}
)

set_property(TARGET ${COMPONENT_LIB} PROPERTY CXX_STANDARD 23)

target_compile_options(${COMPONENT_TARGET}
    PUBLIC
        -DDISABLE_ALL_LIBRARY_WARNINGS
)
