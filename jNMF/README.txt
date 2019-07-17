Joint Non-negative Matrix Factorization (jNMF)

1. How to compile it
The C++ codes have been compiled by "g++". Please, take a look at the file "compile.sh"

2.  How to run
%>jnmf -r 5 -l 10000 -k 3 -t 0.8 -p 1 -g ../TOY/X1.txt -c ../TOY/X2.txt
The command line above runs the jNMF algorithm with the gene expression matrix "X1.txt" and the contamination matrix "X2.txt".
The parameters declare that; 

  A) Number of ranks (-k) is 3
  B) Maximal number of steps in a run (-l) is 10000
  C) Threshold in consensus matrix (-t) is >0.8 
  D) Yes, allowing to output clustered features in "X1.txt" (-p) (It will be time-consuming if X1 is larger).
  E) Repeat (A)-(D) by resetting 5 times (-r)

"X1.txt"  is the n1 x m, where n1 is gene expression levels and m is the cells.
"X2.txt"  is the n2 x m, where n2 is contamination levels and m is the cells.
 
3. Description for output files
The directory "Example" includes the output files from the program.

3-1 "Cell_jnmf_cons.txt": Consensus matrix for Cells
3-2 "Gene_jnmf_cons.txt": Consensus matrix for Genes
3-3: "Microbe_jnmf_cons.txt": consenus matrix for Contaminants
3-4 "H1_jnmf_best.txt":  H1 matrix (for expresson x cell matrix)
3-5: "H2_jnmf_best.txt": H2 matrix (for contamination x cell matrix)
3-6: "W_jnmf_best.txt": W matrix
3-7: "Module_jnmf.txt": The output of modulations
