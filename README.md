# R_PACKAGES_alignSeqInR
R packages for pairwise alignment  ----for STAT430

To run the package and function in R,

    install.packages (“alignSeqInR”)
    library(“alignSeqInR”)
    doAlignment(filename1,filename2, sigma, q , r)
    GC_Content(filename)
    
 filename1 and filename2 are two files with sequences in fasta file
 Sigma is the mismatch score (a negative integer), for the mismatched nucleotides
 Q and r are gap open penalty (a non-negative integer) and gap extension penalty (a positive integer)
 The filename is the fasta file with one DNA sequence

The output of “doAlignment” function is the optimal local alignment. It has the summary of sequence and alignment information and the alignment.

The output of "GC_Content" is the percentage of nucleotides of G and C in the full sequences
