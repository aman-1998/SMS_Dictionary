SMS_Dictionary
SMS Dictionary is a famous problem given by NPTEL (IIT Madras) as an assignment in the course of Data-structures and Algorithms.

(Indian National Olympiad in Informatics, INOI, 2007)

Problem Statement:-

In the pre-smartphone era, most mobile phones with numeric keypads had a private dictionary of words to allow users to type messages quicker. On a typical phone of this type, each number key is assigned a subset of the alphabet {a,b,…,z}: 2 is assigned the subset {a,b,c}, 3 is assigned {d,e,f}, 4 is assigned {g,h,i}, 5 is assigned {j,k,l}, 6 is assigned {m,n,o}, 7 is assigned {p,q,r,s}, 8 is assigned {t,u,v} and 9 is assigned {w,x,y,z}.

When the user types a sequence of numbers, this sequence is mapped to all possible words that can be constructed from the key assignment. For instance, if the user types 66, this could correspond to any one of the letter sequences "mm", "mn", "mo", "nm", "nn", "no", "om", "on" or "oo". These letter sequences are looked up in the dictionary stored in the phone and all matches are reported. For instance, if the phone's dictionary contains only "on" and "no" from this set of sequences, the user will be offered a choice of "on" or "no" to insert in the message. Similarly, the input 4663 might be interpreted as either "good" or "home". An input sequence may have a unique interpretation---for example, the only word in the dictionary matching the input 28 may be "at". Other sequences may not match any word in the dictionary—for instance, 99999.

Your task is the following. Given the typical assignment from number keys to letters of the alphabet given above and given a dictionary of words, report the input sequence that matches the largest number of words in the dictionary. For example, if the dictionary consists of the words {at,on,good,no} then the answer is 66, because 66 matches both "on" and "no" while no other input matches more than one word in the dictionary. On the other hand, with the dictionary {at,on,good,no,home,gone}, the answer is 4663, because 4663 matches three words, "good", "home" and "gone" in the dictionary.

Solution hint
For each word in the input, compute the number key sequence that creates it by inverting the mapping 2→{a,b,c}, 3→{d,e,f} etc. Store the number corresponding to the word in an array.

After reading all the input, sort the numbers in the array.

Input format
The first line of input is an integer M, the number of words in the dictionary. This is followed by M lines of input. Each line contain one word from the dictionary, where a word is sequence of characters from the lowercase alphabet {a,b,c,…,z}.

Note: Each word in the dictionary is, in general, an arbitrary sequence of letters from {a,b,c,…,z}. In particular, it is not assumed that the words stored in the dictionary are valid words in English or any other language.

Output format
A single line containing the input sequence that matches the maximum number of words in the dictionary. If multiple input sequences qualify for the maximum number of matches, it suffices to report any one.

Test data
For all inputs, 1 ≤ M ≤ 100000. Each word in the dictionary is at most 8 characters long. In 50% of the inputs, 1 ≤ M ≤ 1000.

Example
Here is the sample input and output corresponding to the example discussed above.

Sample input 1:

4

at

on

good

no

Sample output 1:

66


Sample input 2:

6

at

on

good

no

home

gone

Sample output 2:

4663
