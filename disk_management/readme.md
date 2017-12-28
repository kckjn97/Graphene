------
Disk management specification
--------
This folder discusses the way of mounting corresponding disks to correct folder for data distruction in later step discussed in the main folder.

**manage_disk.bash** is the bash I wrote to mount **$row_par*$col_par** amount of (Samsung SSD 850) SSDs under the folder -- **/home/hang/graph/2d**. 

Following steps are necessary for this disk mounting:
- Format every disk to ext4 format.
- Assuming we want to mount **4** disks, so they should be mounted to **/home/hang/graph/2d/row_0_col_0/**, **/home/hang/graph/2d/row_0_col_1/**, **/home/hang/graph/2d/row_1_col_0/** and **/home/hang/graph/2d/row_1_col_1/**. 
