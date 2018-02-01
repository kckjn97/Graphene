project (Graphene)

include_directories("${PROJECT_SOURCE_DIR}")

subdirs(read)

add_executable(text_to_bin.bin tuple_text_to_bin.cpp)