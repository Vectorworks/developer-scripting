# GetProjectUserNames

## Description
Get a list of userids that are part of the current project.

```pascal
FUNCTION GetProjectUserNames(VAR userArray : ARRAY): BOOLEAN;
```

```python
def vs.GetProjectUserNames():
    return (BOOLEAN, userArray)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|userArray|ARRAY|Array of userids as strings|

## Examples
```pascal
resultOK := GetProjectUserNames(userArray);
```
```python
import vs

# Get a list of userids that are part of the current project.
ok, userArray = vs.GetProjectUserNames()
vs.Message('GetProjectUserNames returned: ' + str((ok, userArray)))
```

## See Also
VS Functions:
[GetProjectUser](GetProjectUser.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
