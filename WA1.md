I will write as if the code is being entered into the command line. 
**sort -R -r file.txt |grep -c -w hello|wc -c -w = the output would be the number of times the word "hello" is found within the file followed the byte count of that.**
The program first sorts the file randomly as done by -R and then sorts it in reverse hence -r. Following this the grep command then finds the number of times "hello" is found and the lines its found it. Following this the wc command then outputs the number of times the word was found and the byte ammount of that data.
