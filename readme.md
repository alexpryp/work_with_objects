Record Collection


We have such original oblect:
let collection = {
    "2548": {
      "album": "Slippery When Wet",
      "artist": "Bon Jovi",
      "tracks": [ 
        "Let It Rock", 
        "You Give Love a Bad Name" 
      ]
    },
    "2468": {
      "album": "1999",
      "artist": "Prince",
      "tracks": [ 
        "1999", 
        "Little Red Corvette" 
      ]
    },
    "1245": {
      "artist": "Robert Palmer",
      "tracks": [ ]
    },
    "5439": {
      "album": "ABBA Gold"
    }
};



Main task:

You are given a JSON object representing a part of your musical album collection. Each album has several properties and a unique id number as its key. Not all albums have complete information.

Write a function which takes an album's id (like 2548), a property prop (like "artist" or "tracks"), and a value (like "Addicted to Love") to modify the data in this collection.

If prop isn't "tracks" and value isn't empty (""), update or set the value for that record album's property.

Your function must always change object clone.

There are several rules for handling incomplete data:

If prop is "tracks" but the album doesn't have a "tracks" property, create an empty array before adding the new value to the album's corresponding property.

If prop is "tracks" and value isn't empty (""), push the value onto the end of the album's existing tracks array.

If value is empty (""), delete the given prop property from the album.


Tasks:
1) After updateRecords(5439, "artist", "ABBA"), artist should be "ABBA"
2) After updateRecords(5439, "tracks", "Take a Chance on Me"), tracks should have "Take a Chance on Me" as the last element.
Passed
3) After updateRecords(2548, "artist", ""), artist should not be set
4) After updateRecords(1245, "tracks", "Addicted to Love"), tracks should have "Addicted to Love" as the last element.
5) After updateRecords(2468, "tracks", "Free"), tracks should have "1999" as the first element.
6) After updateRecords(2548, "tracks", ""), tracks should not be set
7) After updateRecords(1245, "album", "Riptide"), album should be "Riptide"


After all the transformations we have to get such an object:

let cloneOriginalCollection = {
    "2548": {
      "album": "Slippery When Wet"
    },
    "2468": {
      "album": "1999",
      "artist": "Prince",
      "tracks": [ 
        "1999", 
        "Little Red Corvette",
        "Free" 
      ]
    },
    "1245": {
      "album": "Riptide"
      "artist": "Robert Palmer",
      "tracks": [ 
        "Addicted to Love"
      ]
    },
    "5439": {
      "album": "ABBA Gold",
      "artist": "ABBA",
      "tracks": [
		"Take a Chance on Me"
      ]
    }
};
