# Algorithms
### Input: 
Receive a list of words as input.
### Initialization: 
Initialize an empty unordered map to store short forms mapping.
### Generate Short Forms:
For each word in the input list:
Iterate over each possible subsequence of lengths one to four characters within the word.
Check if the subsequence is already in the map:
If not, add it to the map with the original word as its value.
If yes, check if the existing value matches the current word:
If yes, continue.
If no, invalidate the subsequence by mapping it to an empty string.
### Output: 
Return the map containing valid short forms for the input words.
Here's a more detailed step-by-step algorithm:

For each word in the input list:
Initialize an empty string subsequence.
Iterate over each character ch in the word:
Append ch to subsequence.
If subsequence is not already in the map, add it with the current word as its value.
If subsequence is already in the map and the value does not match the current word, set the value to an empty string.
Repeat this process for subsequences of lengths two, three, and four by appending additional characters to subsequence.
Return the map containing valid short forms for the input words.


This algorithm ensures that each valid short form is a distinct subsequence of lengths one to four characters that occurs in the same order as the original word.





