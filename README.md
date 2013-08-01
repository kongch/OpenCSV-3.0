OpenCSV-3.0
===========

This is the OpenCSV improvement from https://code.google.com/p/opencsv/

The version is increased to 3.0 due to the behavior is not backward compatible. If you would like a CSV parser to be similar to MS Excel and MySQL default behavior, this will be a good one. The decision was made due to CIShell Powered tool (http://cishell.org) is targeting users with no or limited programming skills. These users tend to be familiar with MS Excel, OpenOffice, etc. Programmer users can customize the parameters to achieve their goal. 

<b>Please submit your improvement on this version to be shared here. </b>

The following are the changes:
1. Fixed double standard issues on CSVReader and CSVWriter
- Different default parameters that caused output from CSVWrite couldn't be parsed by CSVRead.
- The CSVWriter default escape character were double quote while CSVReader is backslash
- Quote character should not be treated as escape character in the same time. CSVWriter default quote and escape character were the same but CSVReader throws exception if this is the case. Fixed by not allow both to be happenned.

2. Fixed OpenCSV can't handling qoute in quote issue. E.g. (1,"The "entry have quote",2) should be parsed as (1,"The entry have quote", 2) 

3. Synchronize quote handling as MS Excel and MySQL CSV.

4. Added and changed JUnit Test case to cover the above changes.
