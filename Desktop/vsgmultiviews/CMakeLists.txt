set(SOURCES
    vsgmultiviews.cpp
)

add_executable(vsgmultiviews ${SOURCES})

target_link_libraries(vsgmultiviews vsg::vsg)

if (vsgXchange_FOUND)
    target_compile_definitions(vsgmultiviews PRIVATE USE_VSGXCHANGE)
    target_link_libraries(vsgmultiviews vsgXchange::vsgXchange)
endif()
