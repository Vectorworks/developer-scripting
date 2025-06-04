# StdRead

## Description
Procedure StdRead will read data from a currently open text file. The variable length parameter list returns the read data in the specified parameters.

Supported data types include INTEGER, REAL, LONGINT, CHAR or STRING. Non STRING data values must be separated by a tab or space to be correctly read into variables. If the procedure encounters an EOF(end-of-file) marker, an error is generated. StdRead does not position the file position pointer to the beginning of a new line after the procedure is called.

StdRead reads data according to the Pascal language standard. This differs from the Read procedure found in VectorScript primarily when reading STRING data. StdRead will read all characters, including tabs and spaces, as a single string value. Read will detect tabs as delimiters, allowing multiple string values to be assigned to variables.

```pascal
PROCEDURE StdRead(VAR z : ANY);
```

```python
def vs.StdRead():
    return z
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Examples
==== VectorScript ====
```pascal
GetFile(fName);
IF NOT DidCancel THEN BEGIN
Open(fName);
StdRead(partID,partName);
END;
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks8.0

## Category
* [File I@O](../Categories/File%20IO.md)
