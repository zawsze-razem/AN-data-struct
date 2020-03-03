# Player document data structure explained

* name:"STRING" <- unique player name to be used to identify them
* emmr:1000 <- Escort MMR value, input a default value of ???
* mhmmr:1000 <- Manhunt MMR value, input a default value of ???
* ign:[] <- list of Strings - known IGNs of the player
* link:"?" <- link to twitter or some social media, can be left empty
* nation:"?" <- String, two characted code of the country of origin according to the ISO standard, all caps, can be empty
* ehistory:[] <- an array of objects, leave empty, data structure of stored objects TBD, escort mmr history
* mhhistory:[] <- an array of objects, leave empty, data structure of stored objects TBD, manhunt mmr history
* egames:[0,0,0] <- array of ints: [GAMES_PLAYED, GAMES_WON, GAMES_LOST] - Escort
* mhgames:[0,0,0] <- array of ints: [GAMES_PLAYED, GAMES_WON, GAMES_LOST] - Manhunt
* platforms:[] <- array of Strings, platforms on which the player plays
