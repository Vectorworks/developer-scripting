# GetProjectName

## Description
Gets the name of the Project File for Project Sharing.

```pascal
FUNCTION GetProjectName(VAR name : STRING): BOOLEAN;
```

```python
def vs.GetProjectName():
    return (BOOLEAN, name)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|   |

## Examples
```pascal
resultOK := GetProjectName('Example');
```
```python
import vs

# Gets the name of the Project File for Project Sharing.
ok, name = vs.GetProjectName()
vs.Message('GetProjectName returned: ' + str((ok, name)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
