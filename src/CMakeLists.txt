include(AMXConfig)
include(AddSAMPPlugin)

set(SAMP_SDK_ROOT "${PROJECT_SOURCE_DIR}/lib/samp-plugin-sdk")
find_package(SAMPSDK REQUIRED)

include_directories(
	${SAMPSDK_INCLUDE_DIR}
)

add_samp_plugin(bcrypt
	${SAMPSDK_DIR}/amxplugin.cpp
	${SAMPSDK_DIR}/amxplugin2.cpp
	${SAMPSDK_DIR}/amx/getch.c
	main.hpp
	main.cpp
	bcrypt.hpp
	bcrypt.cpp
	callback.hpp
	callback.cpp
	plugin.cpp
	plugin.hpp
	natives.cpp
	natives.hpp
	plugin.def
)
