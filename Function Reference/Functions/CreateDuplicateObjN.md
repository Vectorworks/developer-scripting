# CreateDuplicateObjN

## Description
Duplicates the specified object and inserts the new  object into the container.  If container is nil, the new object will be inserted in the active container (Functionality of CreateDuplicateObject). This functions add an extra input parameter to maintain height relative to the specified layer.

```pascal
FUNCTION CreateDuplicateObjN(
				objectToDuplicate             : HANDLE;
				containerHandle               : HANDLE;
				maintainHeightRelativeToLayer : BOOLEAN): HANDLE;
```

```python
def vs.CreateDuplicateObjN(objectToDuplicate, containerHandle, maintainHeightRelativeToLayer):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectToDuplicate|HANDLE|   |
|containerHandle|HANDLE|   |
|maintainHeightRelativeToLayer|BOOLEAN|   |

## Version
Availability: from Vectorworks 2020

## Category
* [Object Editing](../Categories/Object%20Editing.md)
