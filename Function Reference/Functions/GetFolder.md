# GetFolder

## Description
Gets the path to a user selected folder

```pascal
FUNCTION GetFolder(
				promptStr         : STRING;
				VAR directoryPath : STRING): INTEGER;
```

```python
def vs.GetFolder(promptStr):
    return (INTEGER, directoryPath)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|promptStr|STRING|   |
|directoryPath|STRING|   |

## Remarks
(*_c_*, 2014.03.25): This was hidden since VW 10 (NOT 2010!), so the compatibility is far more than VW 2014 only.

Prompts for the selection of a folder. Defaults to the folder name in the argument list. Returns 0 if the user hits OK, and -1 if the user hits cancel. The starting VAR directoryPath is overwritten with the path of the chosen folder

## Examples
See [[Python Sample Import Images as Symbols]] for example.
```pascal
PROCEDURE Example;
VAR
   promptStr :STRING; 
   directoryPath :STRING;
   result :INTEGER;
BEGIN
   promptStr := 'Select the folder...';
   directoryPath := GetFolderPath(3);
   result := GetFolder(promptStr, directoryPath);
   Message(directoryPath);
END;
Run(Example);
```

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
