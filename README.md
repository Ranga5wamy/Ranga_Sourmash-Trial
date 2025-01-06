## Ranga_Sourmash-Trial
Bagool



This is my attempt at making this tutorial and attempting sourmash


First get your data you want to analyze

wget -nc ftp://ftp.sra.ebi.ac.uk/vol1/fastq/SRR249/041/SRR24919441/SRR24919441_1.fastq.gz

wget -nc ftp://ftp.sra.ebi.ac.uk/vol1/fastq/SRR249/041/SRR24919441/SRR24919441_2.fastq.gz


Put them in a folder in your bash terminal
If you dont have one

mkdir NAME
cd NAME


now you are in it


Now join the fastq.gz files together. 

Activate Pip 

paste <(zcat SRR24919441_1.fastq.gz) <(zcat SRR24919441_2.fastq.gz) | paste -d '\n' - - - - - - - - | gzip > SRR24919441_combined.fastq.gz
