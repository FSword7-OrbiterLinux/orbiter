# Copyright (c) Martin Schweiger
# Licensed under the MIT License

add_subdirectory(samples)

if(ORBITER_MAKE_DOC)
	add_subdirectory(doc)
	if(Doxygen_FOUND)
		add_subdirectory(doxygen)
	endif()
endif()

install(DIRECTORY html include
	DESTINATION ${ORBITER_INSTALL_SDK_DIR}
)
