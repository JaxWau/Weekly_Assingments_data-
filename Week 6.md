Here is the code and answer to questions for Weekly Assignmnet 6. 

First the needed files were downloaded using the following code:
wget https://github.com/stechtmann/BL4300-5300/raw/master/data/Weekly_Assignment_data/Unk_therm.faa

Then the searchable BLAST database was setup using the following code:

makeblastdb -in Unk_therm.faa -dbtype prot -title hsp_protein

Following this the CPN_BL was downloaded using the following code:

wget https://github.com/stechtmann/BL4300-5300/raw/master/data/Weekly_Assignment_data/HSP_prot.fasta

The blastable database was then queried with the following code:

blastp -db Unk_therm.faa -query HSP_prot.fasta -out CPN_BLAST.txt -outfmt 7

1 and 2. After running the blastp there were 6 quieres. Within each of these 6, x of them were HSPs. The reason for this being that the %identity was high relative to the others, the e.value was very low, and the length of the reads was long. 

Of these HSPs y of them have paralogs. The reason for this is....
