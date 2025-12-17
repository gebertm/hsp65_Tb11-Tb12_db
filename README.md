# hsp65 Tb11-Tb12 marker gene database - updated 2024
> Total sequences (as of 24 January 2025): 189

> Read Length: 401bps

> A collaboration between Dr. Matthew J. Gebert (CU Boulder), Michael Hoffert (CU Boulder)
and Dr. Conor Meehan (Nottingham Trent University)


## Database update protocol

### Part I: Cleaning and preparing the training dataset (Dai et al, 2011)

> Reference database: https://journals.asm.org/doi/full/10.1128/jcm.02602-10

### Step 1: Align Dai et al reference sequences using MAFFT 
> (https://mafft.cbrc.jp/alignment/software/)

Command: 
```
	mafft --auto -in <hsp65_dai_database_file.fa> > <hsp65_dai_database_file.afa>
```


### Step 2: Trim aligned reads using trimAl 
> (https://trimal.readthedocs.io/en/latest/)

Command:
```
	trimal -in <hsp65_dai_database_file.afa> -out <hsp65_dai_database_file_trimmed.afa> -automated1 -keepheader
```
