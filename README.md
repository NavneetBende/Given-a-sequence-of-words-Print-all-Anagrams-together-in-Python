Print all Anagrams Together in Python
Here on this page, we will learn how to Print all Anagrams Together in Python.

Example :

Input : wordArr = { “cat”, “dog”, “tac”, “god”, “act”, ”z” }
Output : cat tac act dog god z
Explanation : here the output of the current input is cat tac act dog god z as it’s printing all anagrams together
Print all Anagrams Together in Python

Algorithm
Creating a Hash Table is a simple method. Determine the hash value of each word so that all anagrams have the same hash value. Fill in the hash values in the Hash Table
Finally, print those words with the same hash values together. The modulo sum of all characters can be used to implement a simple hashing mechanism. Two non-anagram words can have the same hash value when using modulo sum. Individual characters can be matched to handle this
In the following program, an array of structure “Word” is used to store both index and word arrays. Dupray is another structure that stores an array of structure “Word”
Print all Anagrams Together
Python Code
Run
from collections import defaultdict # to create a dictionary
 
#taking the words as input list
words = [ "cat", "dog", "tac", "god", "act", "z" ]

# anagram dictionary
anagrams = defaultdict(list)

# this will check if the words are anagrams of eachother
for word in words:
  anagrams[''.join(sorted(word))].append(word)

# this loop will print all the anagrams together
for anagram in anagrams.values():
  print(' '.join(anagram))
Output
cat tac act
dog god
z
