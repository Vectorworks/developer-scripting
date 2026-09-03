# NumRecords

## Description
Returns the number of records attached to the referenced object.

```pascal
FUNCTION NumRecords(h : HANDLE): INTEGER;
```

```python
def vs.NumRecords(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
#### VectorScript ####
```pascal
numAttached:=NumRecords(HandleToObject);
```
#### Python ####
```python
numAttached = vs.NumRecords(HandleToObject)
```

```pascal
BEGIN
	tempNumRec := NumRecords (NIL);
	j := 0;
	FOR i := 1 TO tempNumRec DO
	BEGIN
		recordH := GetRecord (NIL, i);

BEGIN
IF (GetType(objHand) = 86) & (GetName(GetRecord(objHand,NumRecords(objHand)))= parmName) THEN {Added to make sure we don't try to set anything other than 'this' object since we need to go deep}
	BEGIN
	SetRField(objHand, parmName,FieldName, SymName);
	ResetObject(objHand);
	END;

	BEGIN
		ObjCount := ObjCount + 1;
		RedList[ObjCount] := h;
	END
ELSE IF NumRecords(h) > 0 THEN
	IF (GetName(GetRecord(h, NumRecords(h))) = kRedlinePathObjName) THEN {New Path Based Redline object}
		BEGIN
			ObjCount := ObjCount + 1;
			RedList[ObjCount] := h;
		END;
```
```python
import vs

# Returns the number of records attached to the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.NumRecords(h)
vs.Message('NumRecords returned: ' + str(count))
```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
