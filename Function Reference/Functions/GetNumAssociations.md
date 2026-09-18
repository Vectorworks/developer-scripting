# GetNumAssociations

## Description
Get number of associations for specified object.

```pascal
FUNCTION GetNumAssociations(handle : HANDLE): INTEGER;
```

```python
def vs.GetNumAssociations(handle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|Object handle.|

## Remarks
Number of associations of specified object.

## Examples
```pascal
BEGIN
	numAssociations := GetNumAssociations(parmHand);
	FOR j := 0 TO numAssociations - 1 DO
	BEGIN
		tempHandle := GetAssociation(parmHand, j, associationKind, value);
		if (tempHandle <> NIL) THEN

BEGIN
	AssociationsNumber := GetNumAssociations(ParamHandle);
	AssociationIndex := 0;
	WHILE (AssociationIndex < AssociationsNumber) AND (gFirstInstHand = NIL) DO
		BEGIN
			AssociationHandle := GetAssociation(ParamHandle, AssociationIndex, AssociationKind, AssociationValue);

BEGIN
	numAssociations := GetNumAssociations( ghParm );
	FOR i := 0 TO numAssociations - 1 DO
	BEGIN
		tempHandle := GetAssociation( ghParm, i, associationKind, tempValue);
		IF (tempHandle <> NIL) THEN
```
```python
import vs

# Get number of associations for specified object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.GetNumAssociations(handle)
vs.Message('GetNumAssociations returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Object Editing](../Categories/Object%20Editing.md)
