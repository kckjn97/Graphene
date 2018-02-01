project (Graphene)
include_directories("${PROJECT_SOURCE_DIR}")
include_directories(../../lib)
file(GLOB lib
        "../../lib/*.h"
        "../../lib/*.hpp"
        "../../lib/*.cpp"
        )

add_executable(aio_apsp.bin apsp.cpp ${lib})

target_link_libraries(aio_apsp.bin aio)