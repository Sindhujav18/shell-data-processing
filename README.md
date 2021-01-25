## Curl command to get the data

curl "http://shakespeare.mit.edu/romeo_juliet/full.html" -O "data.txt"

## To process text data in a file:


- Transform each space ' ' into a return character '\12'

   tr ' ' '\12' < data.txt



- To sort the above output in a file

   tr ' ' '\12' < data.txt | sort

- Pipe the sorted output to uniq -c to count

   tr ' ' '\12' < data.txt | sort | uniq -c

- Pipe the reduced output to sort with -nr flag
 
   tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr

- Redirect the output to result.txt

  tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr > result.txt

  
