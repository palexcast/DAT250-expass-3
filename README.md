# DAT250-expass-3



```
   db.characters.bulkWrite(
      [
         { insertOne :
            {
               "document" :
               {
                  "_id" : 4, "char" : "Rick", "class" : "barbarian", "lvl" : 23
               }
            }
         },
         { insertOne :
            {
               "document" :
               {
                  "_id" : 5, "char" : "Morty", "class" : "fighter", "lvl" : 3
               }
            }
         },
         { updateOne :
            {
               "filter" : { "char" : "Morty" },
               "update" : { $set : { "status" : "Critical Injury" } }
            }
         },
         { deleteOne :
            { "filter" : { "char" : "Rick" } }
         },
         { replaceOne :
            {
               "filter" : { "char" : "Morty" },
               "replacement" : { "char" : "MrSanchez", "class" : "oracle", "lvl" : 9000 }
            }
         }
      ]
   );
```