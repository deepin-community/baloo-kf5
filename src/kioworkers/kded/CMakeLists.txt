set (KDED_BALOOSEARCH_SRCS
     baloosearchmodule.cpp
)

add_library(baloosearchmodule MODULE ${KDED_BALOOSEARCH_SRCS})

target_link_libraries(baloosearchmodule
    KF5::CoreAddons
    KF5::DBusAddons
    KF5::KIOCore
)

install(TARGETS baloosearchmodule DESTINATION ${KDE_INSTALL_PLUGINDIR}/kf${QT_MAJOR_VERSION}/kded)
