# Some useful commands in powershell:
1. **ni**: To create a new file. 
2. **cd**: Change directory.
3. **cat**: To view a file.
4. **history**: To view previous commands
5. **mkdir**: To create new directory.
6. **rm** To remove a file.

# To Process the data in the file:
- Transform each space ' ' into a return character '\12' (aka ASCII line feed) 
tr ' ' '\12' < data.txt
- Sort the data in the file
tr ' ' '\12' < data.txt | sort
- Pipe the sorted output to uniq -c to count
tr ' ' '\12' < data.txt | sort | uniq -c
- Pipe the reduced output to sort with -nr flag
tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr
- Redirect the output to result.txt
tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr > result.txt