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

## Examples
```pascal
IF (h <> NIL) & (GetName(GetRecord(h, NumRecords(h))) = 'Flowchart Node') THEN BEGIN
	found1 := TRUE;
	HCenter(h, pt1.x, pt1.y);
	pt1 := WorldToObjectCoords(objHand, pt1);
	status := RemoveAssociation(h, kOnDeleteDelete, objHand);
	status := AddAssociation   (h, kOnDeleteDelete, objHand);
END;

BEGIN
	status := RemoveAssociation(tempHandle, kOnResetReset, parmHand);
	status := RemoveAssociation(tempHandle, kOnDeleteReset, parmHand);
END;

BEGIN
	boo := RemoveAssociation(objHand,     kOnDeleteDelete, theOtherOne);
	boo := RemoveAssociation(theOtherOne, kOnDeleteDelete, objHand);
	boo := SetCustomObjectProfileGroup(objHand, theOtherOne);
	theOtherOne := NIL;
END;
```
```python
import vs

# Removes an object-to-object association.
ioOwnerObj = vs.FSActLayer()  # handle to the first selected object on the active layer
inKind = 0
ioTargetObj = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.RemoveAssociation(ioOwnerObj, inKind, ioTargetObj)
if ok:
    vs.Message('RemoveAssociation succeeded')
else:
    vs.Message('RemoveAssociation failed')
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
