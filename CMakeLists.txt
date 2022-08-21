# Set where the ImGui files are stored
set(IMGUIZMO_PATH  .)

file(GLOB IMGUIZMO_SRC
	"*.h"
	"*.cpp"
)

add_library("imguizmo" STATIC ${IMGUIZMO_SRC})

target_include_directories("imguizmo" 
	PUBLIC ${IMGUIZMO_PATH}
	PRIVATE ${IMGUIZMO_PATH}/example
)
