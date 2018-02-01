project (Graphene)
include_directories("${PROJECT_SOURCE_DIR}")
include_directories(../../lib)
file(GLOB lib
        "../../lib/*.h"
        "../../lib/*.hpp"
        "../../lib/*.cpp"
        )

add_executable(aio_pagerank.bin pagerank.cpp ${lib})

target_link_libraries(aio_pagerank.bin aio)