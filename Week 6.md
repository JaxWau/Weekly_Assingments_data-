Here is the code and answer to questions for Weekly Assignmnet 6. 

First the needed files were downloaded using the following code:
wget https://github.com/stechtmann/BL4300-5300/raw/master/data/Weekly_Assignment_data/Unk_therm.faa

Then the searchable BLAST database was setup using the following code:

makeblastdb -in Unk_therm.faa -dbtype prot -title hsp_protein
