
The Reversion Test: Can we reposition the reads to their orignal genome? 

1. General Procedure
We randomly selected ten species belonging to distinct genera and prepared 1,000 100-base pair (bp) DNA fragments from the genome of a selected species (i.e. 1,000 x10 species / run).

After mapping the 10,000 reads to microbial genomes, we calculated the false discovery rate (FDR) for each species in the random reads; TN / (TN+TP), where TP (true positive) is the number of reads mapped to their origin and TN (true negative) is the number of reads mapped to others.

2. File Description
2-1. The directory "CFG/" is the configuration file for generating the random 10,000 reads for each run

2-2. The directory "FASTQ/" includes the prepared reads for each run

2-3. The directory "Sim_x" is the xth reversion test.
2-3-1. "ngs.contami.conf" in "Sim_x" is the configuration file for each run.

2-3-2. The text file "HISAT2/UNMAPPED/contami_profile.txt" is the final contamination profile for the run: including the counts for muti-mapped-reads, uniquely-mapped-reads, and weighted reads.

2-3-3. The BED files "HISAT2/UNMAPPED/*.bed" are the answers (i.e. the origin species of input reads).

2-3-4. The BAM files "HISAT2/UNMAPPED/UNM_ALL_R1_{bacteria|fungi|viral}/2.Sorted_{bacteria|fungi|viral}.bam" include mapped results and have been used to calculate FDR.

2-3-5. The file "this_accuracy.txt" is the result of the reversion test, which includes mapped reads at genus level, species level, and locus level.

NOTE: "RND_1-10.tar.gz" includes files for only 10 runs out of 1,000 runs. The full dataset and results (2.53GB) is downloadable from https://openlooper.hgc.jp/opencontami/help_oct.html
