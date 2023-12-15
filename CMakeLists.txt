add_library(adafruitgfx STATIC)

target_include_directories(adafruitgfx
	PUBLIC
		includes
)

file(GLOB adafruitgfx_sources sources/*.cpp sources/*.c)
target_sources(adafruitgfx
    PRIVATE
        ${adafruitgfx_sources}
)

target_link_libraries(adafruitgfx mbed-os)
