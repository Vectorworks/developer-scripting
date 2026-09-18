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
(*\_c\_*, 2014.03.25): This was hidden since VW 10 (NOT 2010!), so the compatibility is far more than VW 2014 only.

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

```pascal
if dialogType = 'DistDialog'  then temp_s := Num2StrF(   DistDialog(prompt, default)) ELSE
if dialogType = 'IntDialog'   then temp_s := Num2Str (0, IntDialog (prompt, default)) ELSE
if dialogType = 'RealDialog'  then temp_s := Num2Str (8, RealDialog(prompt, default)) ELSE
IF dialogType = 'StrDialog'   THEN temp_s :=             StrDialog (prompt, default)  ELSE
IF dialogType = 'GetFolder'   THEN temp_i :=             GetFolder (prompt, default);
IF temp_i < 1 THEN BEGIN
	temp_s := default;
	RunPreDefinedDialog := (temp_i = 0);
end ELSE RunPreDefinedDialog := (NOT DidCancel);
```
```python
import vs

# Gets the path to a user selected folder.
promptStr = 'Hello Vectorworks'

resultN, directoryPath = vs.GetFolder(promptStr)
vs.Message('GetFolder returned: ' + str((resultN, directoryPath)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
