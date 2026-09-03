# GetProjectFullPath

## Description
Gets the path and filename of the Project File for Project Sharing.

```pascal
FUNCTION GetProjectFullPath(VAR fullPath : STRING): BOOLEAN;
```

```python
def vs.GetProjectFullPath():
    return (BOOLEAN, fullPath)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fullPath|STRING|   |

## Examples
```pascal
resultOK := GetProjectFullPath('file.txt');
```
```python
import vs

# Gets the path and filename of the Project File for Project Sharing.
ok, fullPath = vs.GetProjectFullPath()
vs.Message('GetProjectFullPath returned: ' + str((ok, fullPath)))
```

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
