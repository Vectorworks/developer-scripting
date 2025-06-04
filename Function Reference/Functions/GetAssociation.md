# GetAssociation

## Description
Gets info about association of specified object.

```pascal
FUNCTION GetAssociation(
				handle              : HANDLE;
				index               : INTEGER;
				VAR associationkind : INTEGER;
				VAR value           : INTEGER): HANDLE;
```

```python
def vs.GetAssociation(handle, index):
    return (HANDLE, associationkind, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|Associated object handle.|
|index|INTEGER|Index of association.|
|associationkind|INTEGER|Kind of association - reset or delete action|
|value|INTEGER|   |

## Remarks
Returns association handle.

## Version
Availability: from Vectorworks 2018

## Category
* [Object Editing](../Categories/Object%20Editing.md)
