# Automatic sequence verifier for Kunkel mutagenesis 

After you've recieved Sanger sequencing results, you'll have paired reads for each clone (picked colony), one forward and one reverse. This notebook will help you 

1. pair the two reads (taking the quality scores into account) into a consensus sequence 
2. determine the differences between the consensus sequence and a given reference sequence 

Since we are doing mutagenesis for protein design, we care only about the amino acid sequence. We use `blastx` to align all three frames of our nucleotide sequence to a reference amino acid sequence. 

## Input files 

+ Sanger reads (.ab1 format) 
+ wild type amino acid sequence 

## Instructions for use 

Use the Jupyter notebook in this repo to merge your paired Sanger reads with [`pear`](http://sco.h-its.org/exelixis/web/software/pear/) and align them to the native amino acid sequence using [`blastx`](http://blast.ncbi.nlm.nih.gov/Blast.cgi). 

## Output 

You can configure the output by editing the if/else stanzas at the end of the code. By default, the notebook will print out the names of constructs with a wild type sequence so you can evaluate your Kunkel efficiency. Note that the default setting is to print **only single mutants** though this can be easily changed by setting a different value in the code. 
