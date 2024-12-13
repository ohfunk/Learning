Here are some useful links to resources for learning modern genomics

Single Cell:
Pachter Lab Course: https://github.com/pachterlab/Bi-BE-CS-183-2023
Best Practices Theis: https://www.nature.com/articles/s41576-023-00586-w.epdf?sharing_token=mPc01Mtbq3r__nP3ws5N99RgN0jAjWel9jnR3ZoTv0Md3S2ljmfWhhBCwlFE6hzj48-AGqEMXF9V8R6wDA_ll7K1w4fAczTw48hnQIZFmDS_uVhegJca3W6R9-oNBqBAmJLO5ABX1TFBk6kboh9quZWss7o6F_DYeQFnII7nyH4%3D

Stats and Theory:
Shrinkage:
Lior "tutorial" on RNAseq DE 2017 - https://www.youtube.com/watch?v=ZyRT1z1Sz3g](https://www.youtube.com/watch?v=ucPBBTjH5EE)https://www.youtube.com/watch?v=ucPBBTjH5EE

##Some misc. Linux commands I've foudn helpful for working with genomics data on an HPC:
----
### memory availbe on curent node
free -h

### number of reads in a fastq x4, compare R1 R2 to make sure they're paired and 
zgrep -c '^@' filename.fastq.gz
### getting total reads in various steps of RNAseq pipeline
#### for kallisto salmon txt files
awk '{sum += $2} END {print sum}' filename.txt
#### for dedupped bam files
samtools view -c -F 260 filename.bam
