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

target_compile_options(${COMPONENT_TARGET}
    PUBLIC
        -DDISABLE_ALL_LIBRARY_WARNINGS
)
