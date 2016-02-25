# Automatic sequence verifier for Kunkel mutagenesis 

After you've recieved Sanger sequencing results from your Kunkel constructs, you'll have paired reads for each clone, one forward and one revser, each covering about two thirds of the gene (approximately 1,500 bp). 

## Input files 

+ paired Sanger reads 
+ wild type amino acid sequence 

## Instructions for use 

Use the Jupyter notebook in this repo to merge your paired Sanger reads with [`pear`](http://sco.h-its.org/exelixis/web/software/pear/) and align them to the native amino acid sequence using [`blastx`](http://blast.ncbi.nlm.nih.gov/Blast.cgi). 

## Output 

You can configure the output by editing the if/else stanzas at the end of the code. By default, the notebook will print out the names of constructs with a wild type sequence so you can evaluate your Kunkel efficiency. Note that the default setting is to print **only single mutants** though this can be easily changed by setting a different value in the code. 
