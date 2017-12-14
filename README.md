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

SeqA.fasta and SeqB.fasta files with sequences. This is the examples for this package. You can run the example like:

    doAlignment(SeqA.fasta, SeqB.fasta, -20, 40, 2)
    GC_Content(SeqA.fasta)
The output sample like:


  Match Score: 10;  
  Mismatch Score:  -20 
  Gap-Open Penalty:  40 
  Gap-Extension Penalty:  2 

Alignment Score:  1056 
 Length:  341 

Start Position in A:  123 
Start Position in B:  234 

  End Position in A:  442 
  End Position in B:  553 

Number of matches:  248 
Number of mismatches:  51
Length of gaps:  42
Percent Identity:  72.73% 



123           GGACTGGGCGTTACGGCGGGTGCCCACAGGCTATGGA--CACATCGCTCTTACAAAGCTAAACTCCCCCT   190
              ||||||||| | || || || |  |||||||||||||  ||||  |  | ||||||||||| || || ||
234           GGACTGGGCATCACTGCTGGAGTACACAGGCTATGGAGTCACAAGG--CCTACAAAGCTAACCTGCCTCT   301


191           ACGAGTGATGCT-----TATGCTCTTCCACTGTATTGCT-------ATACAGAACACTGTACTGGACTGG   248
               |||||||| ||     ||     ||| ||  |||||||       || ||       || ||  |||||
302           CCGAGTGATACTCGCACTA-----TTCAACACTATTGCTTTCCAAGATGCA-------GTTCTACACTGG   359


249           GCACGTAACCACCGCATGCACCACAAGTACTCGGAAACAGACGCGGACCCTCACAACGCCACACGCGGTT   318
              || ||  ||||||||||||| |||||||||||||| |||||||| ||||||||||| ||||| || || |
360           GCTCGCGACCACCGCATGCATCACAAGTACTCGGAGACAGACGCTGACCCTCACAATGCCACGCGTGGGT   429


319           TCTTCTTCTCCCACATGGGATGGCTTATGGTTAGAAAGCATCCGGACATCAAAGCTAAAGGTCATACCAT   388
              |||||||||||||| | |||||||| ||||| |  || ||||| || ||||| ||||||| ||| || ||
430           TCTTCTTCTCCCACGTCGGATGGCTGATGGTCAAGAAACATCCAGAGATCAAGGCTAAAGCTCACACTAT   499


389           CGACATAAGTGAC-------CTAACGTCCGATCCTGTACTTCAGTTCCAGAAAAAGTACTA   442
              ||| |||||||||       ||       ||||| || |||   |||||||||||||||||
500           CGATATAAGTGACTTATTAGCT-------GATCCCGTCCTTACTTTCCAGAAAAAGTACTA   553
