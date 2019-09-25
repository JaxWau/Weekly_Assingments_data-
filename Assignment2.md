Here is the information for Weekly Assingment 2

Code for finiding the number of protein sequences in the .fasta file.-----> **fgrep NC_008535 Assignment_2_Coffee_Sequence.fasta | wc -l > Names_o_Proteins.txt**
This line of code will all lines with "NC_008535" from the file and then count the number of lines there are, which should be the number of proteins in the file, and put it into a new file. That number is 85. *(It is good to note that it does say that there are 86 proteins but I was unable to figure out any number that differed from 85 even wehn manually counting them)*

Code for making a new file for all the names of the protein sequences in the .fasta file --> **grep from Assignment_2_Coffee_Sequence.fasta | sed 's/from//g' | sed 's/NC_008535//g' | sed's/>CoarCp//g' | sort -n > Protein_Name_Data.txt**
This line of code finds all lines containing "from" from the file and then deletes "from", "NC_008535", and ">CoarCP" from those lines to give you the number and name of the protein. I then added the sort command to sort the file numerically before putting that data into a new file. 

Code for finding the number of photosystem subunits on the chromosome ----> **grep photosystem Assignment_2_Coffee_Sequence.fasta | grep subunit**
This line of code finds all lines in the file that contains "phostosystem" in it and then finds the lines that contain "subunit" from the lines previously found. In total there are three photosystem subunits in this .fasta file (VIII, IX, and VII),

Code for making a .fasta file for the sequences of ATP synthase CF1 beta subunit protein sequence ----> **grep -A 1 CF1 Assignment_2_Coffee_Sequence.fasta | grep -A 1 beta > ATP_Synthase.fasta**
This code first finds all instances of "CF1" within the file and prints that line and the following line ( -A 1), it then looks for all instances of "beta" from those that contain "CF1" and then prints out that line and the next into a new file titled ATP_Synthase.fasta. 
