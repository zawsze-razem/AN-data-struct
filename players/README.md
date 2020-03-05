# Player document data structure explained

* name:"STRING" <- unique player name to be used to identify them
* emmr:? <- Escort MMR value, input a default value of 1000
* mhmmr:? <- Manhunt MMR value, input a default value of 1000
* ign:[] <- list of Strings - known IGNs of the player
* link:"?" <- link to twitter or some social media, can be left empty
* nation:"?" <- String, two characted code of the country of origin according to the ISO standard, all caps, can be empty
* ehistory:[] <- an array of objects, leave empty, data structure of stored objects TBD, escort mmr history
* mhhistory:[] <- an array of objects, leave empty, data structure of stored objects TBD, manhunt mmr history
* egames:{total:0,won:0,lost:0} <- objects with game statistics - Escort
* mhgames:{total:0,won:0,lost:0} <- objects with game statistics - Manhunt
* platforms:[] <- array of Strings, platforms on which the player plays
* estats:{avgscore:0,highscore:NumberInt(0),kills:NumberInt(0),deaths:NumberInt(0)}
* mhstats:{avgscore:0,highscore:NumberInt(0),kills:NumberInt(0),deaths:NumberInt(0)}
