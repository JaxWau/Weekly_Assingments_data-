Here is the code and answer to questions for Weekly Assignmnet 6. 

First the needed files were downloaded using the following code:
wget https://github.com/stechtmann/BL4300-5300/raw/master/data/Weekly_Assignment_data/Unk_therm.faa

Then the searchable BLAST database was setup using the following code:

makeblastdb -in Unk_therm.faa -dbtype prot -title hsp_protein

Following this the CPN_BL was downloaded using the following code:

wget https://github.com/stechtmann/BL4300-5300/raw/master/data/Weekly_Assignment_data/HSP_prot.fasta

The blastable database was then queried with the following code:

blastp -db Unk_therm.faa -query HSP_prot.fasta -out CPN_BLAST.txt -outfmt 7

1 and 2. After running the blastp there were 6 quieres. Within each of these 6 quieries there we many hits as HSPs. In total there were 71 hits through these 6 quieres. After looking for E-values that were 0.0 or lower the number of HSPs was brought down to 12 HSPs. Looking further for those who had a high percent identity and long overall length the total number of HSPs was brought to 5. The criteria was that there needed to be a higher percentage over a larger number of base pairs. So %ID >30% along with >100 bp for length was kept. Therefore in total there were 5 HSPs that actually held weight and that we were interested in. 

After figuring the amount of HSPs the number of paralogs were found by looking more closely at the E-value and the %ID vs total length of the read. After looking for much lower E-values and greater %ID for longer lengths there are four (4) HSPs which could be paralogs. The reasoning for this is that their E-values are very small and therefore significant and that their %ID and alignment length was well within the "safe zone" that we had seen in class. While one represents an E-value of 0.0, which is much less than the others, its %ID was 61 for >500bp which is why it would stay as a paralog.  
