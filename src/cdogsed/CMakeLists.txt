add_subdirectory(osdialog)
include_directories(
	${SDL2_INCLUDE_DIRS}
	${SDL2_IMAGE_INCLUDE_DIRS}
	${SDL2_MIXER_INCLUDE_DIRS})
set(CDOGSED_SOURCES
	add_pickup_dialog.c
	campaign_options.c
	char_editor.c
	editor_brush.c
	editor_ui.c
	editor_ui_cave.c
	editor_ui_classic.c
	editor_ui_color.c
	editor_ui_common.c
	editor_ui_interior.c
	editor_ui_objectives.c
	editor_ui_static.c
	editor_ui_static_additem.c
	editor_ui_weapons.c
	exit_brush.c
	mission_options.c
	nk_window.c
	tile_brush.c
	ui_object.c)
set(CDOGSED_HEADERS
	add_pickup_dialog.h
	campaign_options.h
	char_editor.h
	editor_brush.h
	editor_ui.h
	editor_ui_cave.h
	editor_ui_classic.h
	editor_ui_color.h
	editor_ui_common.h
	editor_ui_interior.h
	editor_ui_objectives.h
	editor_ui_static.h
	editor_ui_static_additem.h
	editor_ui_weapons.h
	exit_brush.h
	mission_options.h
	nk_window.h
	tile_brush.h
	ui_object.h)
add_library(cdogsedlib STATIC ${CDOGSED_SOURCES} ${CDOGSED_HEADERS})
target_link_libraries(cdogsedlib
	${SDL2_LIBRARY} osdialog)
