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

## Examples
```pascal
BEGIN
	tempHandle := GetAssociation(parmHand, j, associationKind, value);
	if (tempHandle <> NIL) THEN
	BEGIN
		status := RemoveAssociation(tempHandle, kOnResetReset, parmHand);
		status := RemoveAssociation(tempHandle, kOnDeleteReset, parmHand);

BEGIN
	AssociationHandle := GetAssociation(ParamHandle, AssociationIndex, AssociationKind, AssociationValue);
	IF AssociationKind = 39{LoadObjectRiggingObj} THEN
		BEGIN
			gFirstInstHand := AssociationHandle;
		END;

BEGIN
	tempHandle := GetAssociation( ghParm, i, associationKind, tempValue);
	IF (tempHandle <> NIL) THEN
	BEGIN
		paramRecordHandle := GetParametricRecord( tempHandle );
		IF (paramRecordHandle <> NIL) THEN
```
```python
import vs

# Gets info about association of specified object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

objHandle, associationkind, value = vs.GetAssociation(handle, index)
vs.Message('GetAssociation returned: ' + str((objHandle, associationkind, value)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Object Editing](../Categories/Object%20Editing.md)
