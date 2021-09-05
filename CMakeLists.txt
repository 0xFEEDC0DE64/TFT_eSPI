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
