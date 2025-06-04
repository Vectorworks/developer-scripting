# Read

## Description
Procedure Read will read data from a currently open text file. The variable length parameter list returns the read data in the specified parameters.Supported data types include INTEGER, REAL, LONGINT, CHAR or STRING. 

Non STRING data values must be separated by a tab or space to be correctly read into variables. If the procedure encounters an EOF(end-of-file) marker, an error is generated. Read does not position the file position pointer to the beginning of a new line after the procedure is called.

Read will detect tabs as delimiters, allowing multiple string values to be assigned to variables.

```pascal
PROCEDURE Read(VAR z : ANY);
```

```python
def vs.Read():
    return z
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
