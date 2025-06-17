# ReadLn

## Description
Procedure ReadLn will read data from a currently open text file. The variable length parameter list returns the read data in the specified parameters.

Supported data types include INTEGER, REAL, LONGINT, CHAR or STRING. If the procedure encounters an EOF(end-of-file) marker, an error is generated. ReadLn positions the file position pointer to the beginning of a new line after the procedure is called.

ReadLn will detect tabs as delimiters, allowing multiple string values to be assigned to variables.

```pascal
PROCEDURE ReadLn(VAR z : ANY);
```

```python
def vs.ReadLn():
    return z
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Remarks
In the example above, if there are actually only two values (separated by a tab) on the line being read, ReadLn will read the next line of text, looking for a value of the variable type specified by Val3.



ReadLn will strip leading spaces, at least from the first string in the line, if not from all of them.



RGBCOLOR triplets values stored on tabbed files will not be recognized by ReadLn, even if they are LONGINT (VW 12.5).

```pascal
color : RGBCOLOR;
...
ReadLn(color.red, color.green, color.blue); { WRONG: only 0-values are loaded }
```

You must recreate the structure in order to have it recognized.
```pascal
TYPE
ACOLOR = STRUCTURE
red, green, blue : LONGINT;
END;
VAR
color : ACOLOR;
...
ReadLn(color.red, color.green, color.blue); { LONGINT values are correctly loaded }
```


the empty value and space stripping issues are still valid today (VW 12.5.x).

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
fileName, value1, value2, value3 :STRING; 
major, minor, maintenance, platform :INTEGER;
BEGIN
GetVersion(major, minor, maintenance, platform);
IF platform = 1 THEN BEGIN
fileName := '/Example.txt';
END ELSE BEGIN
fileName := 'C:Example.txt';
END;
Open(fileName);
ReadLn(value1, value2, value3);
Close(fileName);
AlrtDialog(lineOfText);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
