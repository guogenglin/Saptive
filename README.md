# RISST
Rapid In Silico SeroTyping for four common swine bacerial pathogens
# What is it?
Similar with primercheck we provide before, this repository is also writing for rapid batch predict the bacteria serotype for numerous genome sequence dataset.   
Here we provide 5 reference sequence files of serotype determine locus of four most common swine bacterial pathogens, *Streptococcus suis*, *Glaesserella parasuis*, *Actinobacillus pleuropneumoniae* and *Pasteurella multocida*. And a Klebsiella capsule and lipopolysaccharide serotype prediction tool--Kaptive were used. It just like a DLC of this software, for expand the database, let more bacteria serotype prediction becoming available.
# External Dependencies
Kaptive https://github.com/katholt/Kaptive/
# Usage
The using of this dapabase is same as Kaptive. you just need to replace the origional reference sequence file by the files we provide. Then run Kaptive. Here we give an example, if the species of your genome dataset are *Sreptococcus suis*, you just need to put ```Streptococcus_suis_cps_locus_primary_reference.gbk``` in the folder contain your genome sequence files, open a terminal and into the folder, get in the evironment if you create one by conda, and run Kaptive like this:   
``` Python
kaptive.py -a *.fna -k Streptococcus_suis_cps_locus_primary_reference.gbk -o output_directory
```
Then wait to it finish.
* We default to think the genome sequence file have a ".fna" suffix, if your file is not, please open the script and change every ".fna" to the suffix of your file.
# Further
You can also use create a reference sequence files for the bacteria you want to predict the serotypes, or other gene clusters which have different types, as the authors of Kaptive said. Just notice that your multi-record reference sequence file should include nucleotide sequences for each whole locus and protein sequences for their genes, if you download it from NCBI, just choose Genbank(full) format to download.
