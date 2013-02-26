========================
TopicKeywordList.exe
========================
  Takes an input file in .csv (comma separated values)  
  format and writes out a topic file and a keyword file in 
  either XML or .csv format.  
  
-----------
Arguments:
-----------
   string outputType (-csv or -xml)
   string inputFilePath
   string outputTopicFilePath
   string outputKeywordFilePath

---------
Example:
---------
  TopicKeywordList.exe -xml "C:\Users\eeguzo\Documents\TopicKeyword Project\Master.csv" "C:\Users\eeguzo\Documents\TopicKeyword Project\Test\topic.xml" "C:\Users\eeguzo\Documents\TopicKeyword Project\Test\keywords.xml"

---------------
Input Details
---------------
Required format for .csv input file:
   column 1: id
   column 2: collection
   column 3: name
   column 4: keywords
   column 5: hq_keywords
   column 6: misspellings
   column 7: shortdescription
   column 8: description
   column 9: length
   column 10: category
   column 11: setId
   column 12: clientId
   column 13: questionnaire
   column 14: iOS


---------------------
.csv Output Details
---------------------
.csv output files will contain all rows from the input file.

Topic.csv will be a copy of the input .csv file, except the misspellings column is merged
into the keywords column.

Keywords.csv will contain all of the keywords from the keywords and hq_keywords columns.


--------------------
XML Output Details
--------------------
XML output files will ONLY contain rows that have "Yes" in column 14 (iOS) above.  

Topic.xml be a subset of the data from the input file:
  ID
  Name
  Category
  Description
  Short Description
  Keywords/Misspellings
  Hq_Keywords

Keywords.xml will contain data from the keywords and hq_keywords columns.

