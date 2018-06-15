CompoMug stands for COMputational Predictions Of MUtations in GPCRs. 

CompoMug consists of four modules: knowledge-based, sequence-based, structure-based, and machine-learning-based, taking maximum advantage of accumulated structural and biophysical data. 
CompoMug provides a computational platform for thermostabilization of GPCRs and can be further evolved with an accumulation of experimental mutation data.
Please check our paper for more details:
Popov et al., 'Computational design of thermostabilizing point mutations for G protein-coupled receptors', eLife, 2018

Knowledge-based module

requires a .fasta file and .csv file with generic numbering layout of the target GPCR, which can be obtained from the GPCRdb web-server (www.gpcrdb.org).
Given that, to get the list of point mutation candidates simply run : 
CompoMug-knowledge-module target.fasta target.csv


Sequence-based module

requires five multiple sequence alignment (MSA) files, where the first line in a file indicates the number of sequences in the MSA and the length of the MSA (number of positions). Note, that number of positions must be the same in all 5 MSA files.
Given that, to get the list of point mutation candidates simply run :
CompoMug-sequence-module msa1.txt msa2.txt msa3.txt msa4.txt msa5.txt


Machine-learning-based module

requires high-quality structural model of the target receptor.
First, use the CompoMug_descriptor.icm script to generate structural model of point mutation and to calculate the corresponding descriptor. You will need a separately licensed ICM-Pro package to be able to run the script (molsoft.com). Given that, to get the list of point mutation candidates simply run :
CompoMug-machine-learning-module compomug_descriptor.txt


Structure-based module

The module is currently in preparation for release in Version v1.1

Each module has an "example" folder, which contains input files in the required format.
All modules were tested on the MacOS operating system.
