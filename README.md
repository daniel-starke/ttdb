# Text Templated Database

## Project Goal

The aim is to provide a library as back-end and a application as front-end.  
The front-end shall be able to read structured text templates to map the  
formatting, descriptions and the actual content to database entries.  
It will also provide ways to show and modify the results, be it as native GUI,  
web side or in another form.  
The back-end on the other hand shall be able to parse and process the templates,  
put the data entries into the right correlations and map the content and keys  
with the database or other databases.  

## Implementation

The implementation will be split into 3 parts.  
 - Template Parser (back-end)
 - Database Mapper (back-end)
 - GUI (front-end)

## Template Parser

 - should be able to parse visually formatted text files ([example](doc/example.tt))
 - checks and reports syntax errors
 - extracts the database keys and their properties
 - builds a structure (AST?) to aid formatted output

## Database Mapper

 - takes the output of the template parser to create/modify the databases
 - validates input data (wrong key correlation or invalid types for example)
 - provides methods to access and modify the needed data
 - probably uses a NoSQL database in the background ([UnQLite](https://unqlite.org/)?)

## GUI

 - wxWidget or HTML-based cross-platform GUI
 - should present the forms as formatted in the template files
