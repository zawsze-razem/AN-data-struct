# The generic CSV (GCSV) file structure for data updates

This file defines the structure of generalized CSV files that can be used by backend algorithms to update the database.

The generic character of this format should be expressed by the ability to use flexible tokens. The default token, however, as per the name of the file type is a comma (","). Thus, it should never appear as a non-token value. Tokens are characters used to define where one value ends and another begins.

## Matches

The generic structure of the GCSV file should apply the following requirements:
* Each record is represented by a line of text in a file
* Each record should consist of a fixed-length header and a body of content
* The length of the body should be possible to determine based on the header
* The header as well as body fields should be separated with token (commas by default)
* The general structure of a record should be [header],[body]
* The header should consist of: mode flag(E-Escort,M-Manhunt), number of players on team 1, number of players on team 2, outcome flag (0-tie, 1-team 1 won, 2-team 2 won)
* The body should consist of: list of players on team 1, list of players on team 2

Example:
Let's say we have two teams: Team 1 (Joe and Dave), Team 2 (Susan and Karen). The teamd played a game of Escort with Team 1 winning. The GCSV file record (a single line with a new-line-sign at the end) to represent such situation should look like:

E,2,2,1,Joe,Dave,Susan,Karen

-header----------body----------\
[E,2,2,1],[Joe,Dave,Susan,Karen]

## Player Entry

The generic structure of the GCSV file should apply the following requirements:
* Each record is represented by a line of text in a file
* Each record should consist of a fixed-length header and a body of content
* The header as well as body fields should be separated with token (commas by default)
* The general structure of a record should be [header],[body]
* The header should consist of: player's country's of origin ISO code, player's social media link or flag of no value input, value correspoing to the platforms(1) 
* The body should consist of: list of player IGNs with the first one being the main IGN used as the name

(1) - the value would be a decimal representation of a bitmap, indicating platforms. Assuming a ['PC','PS3','XBOX'] representation of the platform array a PC and XBOX player would have the following bitmap:\
[1, 0, 1]\
['PC','PS3','XBOX']\
0s and 1s represent which value on the list should be added to his profile.\
Thus, taking the bitmap [1,0,1] (analogue to [True, False, True]) and assuming it is a binary value we get 101 or in decimal representation 5.\
We can use the following algorithm to determin the value:\
platform=0\
if PC:\
  platform += 4\
if PS3:\
  platform +=2\
if XBOX:\
  platform +=1
  
  
