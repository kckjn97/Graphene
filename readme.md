----
Specification
-----
To run graphene, you need to do three things step by step: **[Step 1: Convert and Partition a Graph](https://github.com/asherliu/Graphene/tree/master/converter)**, **[Step 2: Mount Disk to Correct Folder](https://github.com/asherliu/Graphene/tree/master/disk_management)** and **[Step 3: Distribute Partitioned Graph Data (from step 1) to Correct Disk](https://github.com/asherliu/Graphene/tree/master/disk_management)**. Afterwards, you can run graphene as noted in the following step. 


-----
Run Graphene 
-----------
**graphene** subfolder contains *lib and test* two source code. Please find the detailed specification in the sub folders.

How to run an application from Graphene?
For instance, if you want to run BFS on the file you put distributed from [here]((https://github.com/asherliu/Graphene/tree/master/disk_management). You will need the following commandline to run the test:
./aio_bfs.bin 2 2 4 /home/hang/graph/2d/ /home/hang/graph/2d/ com-orkut.ungraph.txt-split_beg com-orkut.ungraph.txt-split_csr 4194304 33554432 4096 16384 32 16 1

The above commandline is reflecting following parameter configurations: /path/to/exe #row_partitions #col_partitions thread_count /path/to/beg_pos_dir /path/to/csr_dir beg_header csr_header num_chunks chunk_sz (#bytes) concurr_IO_ctx max_continuous_useless_blk ring_vert_count num_buffs source;


**Should you have any questions about this project, please contact us by hang_liu@uml.edu.**

-----
Reference
-------
[FAST '17] Graphene: Fine-Grained IO Management for Graph Computing[[PDF](https://www.usenix.org/system/files/conference/fast17/fast17-liu.pdf)] [[Slides](https://www.usenix.org/sites/default/files/conference/protected-files/fast17_slides_liu.pdf)]

