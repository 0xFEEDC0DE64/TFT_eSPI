set(headers
    TFT_eSPI.h
)

set(sources
    TFT_eSPI.cpp
)

idf_component_register(INCLUDE_DIRS . SRCS ${headers} ${sources} REQUIRES arduino-esp32 freertos esp_system)
