#Match document explained
Fields:
* mode : "Escort" / "Manhunt"
* players1 : ["1","2"] <- an array of players on Team 1
* players2 : ["1","2"] <- an array of players on Team 2
* outcome : 0/1/2 <- int value (0 - tie, 1 - team 1 won, 2 - team 2 won)
* new : bool <- new matches should all be flagges as new ("True"), used for the algorithm to be able to find matches to calculate
