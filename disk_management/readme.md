------
Step 2: Mount Disk to Correct Folder
--------
This folder discusses the way of mounting corresponding disks to correct folder for data distruction in later step discussed in the main folder.

**manage_disk.bash** is the bash I wrote to mount **$row_par\*$col_par** amount of (Samsung SSD 850) SSDs under the folder -- **/home/hang/graph/2d**. 

Following steps are necessary for disk mounting step:
- Format every disk.
- Make file system on each disk (assuming ext4).
- Assuming you want to mount **4** disks (/dev/sda1, /dev/sdb1, /dev/sdc1, /dev/sdd1), so they should be mounted to:
  - /home/hang/graph/2d/row_0_col_0/ <- /dev/sda1
  - /home/hang/graph/2d/row_0_col_1/ <- /dev/sdb1
  - /home/hang/graph/2d/row_1_col_0/ <- /dev/sdc1
  - /home/hang/graph/2d/row_1_col_1/ <- /dev/sdd1


----
Step 3: Distribute Partitioned Graph Data (from step 1) to Correct Disk
-----
You need to put map correct datasets to correct file directory (disk mounting point) as follows:
- **/home/hang/graph/2d/row_0_col_0/** contains: com-orkut.ungraph.txt-split_beg.0_0_of_2x2.bin and com-orkut.ungraph.txt-split_csr.0_0_of_2x2.bin.

- **/home/hang/graph/2d/row_0_col_1/** contains: com-orkut.ungraph.txt-split_beg.0_1_of_2x2.bin and com-orkut.ungraph.txt-split_csr.0_1_of_2x2.bin

- **/home/hang/graph/2d/row_1_col_0/** contains: com-orkut.ungraph.txt-split_beg.1_0_of_2x2.bin and com-orkut.ungraph.txt-split_csr.1_0_of_2x2.bin

- **/home/hang/graph/2d/row_1_col_1/** contains: com-orkut.ungraph.txt-split_beg.1_1_of_2x2.bin and com-orkut.ungraph.txt-split_csr.1_1_of_2x2.bin.
