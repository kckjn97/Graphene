cmake_minimum_required (VERSION 2.6)
project (Graphene)
SET(CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS} -std=c++14 -O3 -g -laio -fopenmp -DKV_BOTH_SORTING -DBLK_SZ=512" )

subdirs(
        converter/multi_bin_to_2d_csr
        converter/tuple_to_bin.multithread
        graphene/test/apsp
        graphene/test/bfs
        graphene/test/kcore
        graphene/test/pagerank
        graphene/test/spmv
        graphene/test/wcc
)

