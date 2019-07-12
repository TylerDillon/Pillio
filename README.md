# Pillio
##A hack-a-thon project gone big (or at least a summer project)

Architecture Plan (WIP)
  * Front-end Android interface (in Java)
  * Back-end query builder and record writer classes (in Java)
  * Database to hold client records (in SQL)
  
  __Front-End Android Interface__:
  Multiple screens, as seen here: [Pillio on Figma](https://www.figma.com/file/YzSU7fncmoKLWMI9fDkHWyet/Pillio?node-id=136%3A152)
  
  *This implementation is mostly focused on the Analytics page of the application.*
  
  
  __Back-End QueryBuilder.java and RecordWriter.java__:
  
  
   QueryBuilder.java
   > will use the checkboxes and text-fields from the Android interface to "toggle on"
    certain query phrases. It writes the whole query as Strings to a new file 'query.sql', reads the file
    into a SQL database, and then deletes 'query.sql'.
      **Components to consider**: receiving input from UI, composing string messages for query, running on a SQL shell, 
      returning query results, deleting file
      
   RecordWriter.java 
   > will be responsible for writing new tuples to the database, meaning it will mainly be translating
    input from the interface into INSERT statements for SQL.
    
  __Database__:
    *TODO*: Decide what attributes the early-stage records will have, so we can decide what fields need to be filled
      from the UI side of things.
  * First Name
  * Last Name
  * ID
  * DOB
  * Gender
  * etc (need more)
