# RemoveAssociation

## Description
Removes an object-to-object association.

```pascal
FUNCTION RemoveAssociation(
				ioOwnerObj  : HANDLE;
				inKind      : INTEGER;
				ioTargetObj : HANDLE):BOOLEAN;
```

```python
def vs.RemoveAssociation(ioOwnerObj, inKind, ioTargetObj):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ioOwnerObj|HANDLE|   |
|inKind|INTEGER|   |
|ioTargetObj|HANDLE|   |

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
