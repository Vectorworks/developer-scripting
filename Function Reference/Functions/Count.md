# Count

## Description
Counts all of the objects which match the search criteria.

```pascal
FUNCTION Count(c : CRITERIA): LONGINT;
```

```python
def vs.Count(c):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Remarks
Undocumented is that criteria also accept the object type flag as parameter. The example above can also be written:

```pascal
CountValue := Count((FP=4)and(T=3)); { 3 is object type flag for 'Rectangle&amp' }
```

This is valid for all object types being assigned a name in the [Script Appendix](../Appendix/pages/Appendix%20D%20-%20Vectorworks%20Object%20Types%20and%20Subtypes.md).

## Examples
#### VectorScript ####
```pascal
CountValue := Count((FP=4)and(T='Rect'));
{counts all rectangles with a fillpat index of 4}
```
#### Python ####
```python
CountValue = vs.Count("(FP=4)AND(T='Rect')")
# counts all rectangles with a fillpat index of 4
```

```pascal
BEGIN
	ObjCount := Count(SEL);
	IF ObjCount > 0 THEN
		BEGIN
			ALLOCATE RedList[1..ObjCount];
			ObjCount := 0;

{Load our handle array with the current Selection Set}
gSelectionSize := Count(SEL);
ALLOCATE selHandles[1..gSelectionSize];
ALLOCATE ObjLoc[1..gSelectionSize];
gNumObjs := 0;
ForEachObjectInLayer(LoadHandleArray, 2, 0, 4);

BEGIN
	IF ResourceIsOK THEN
	if Count(ALL) > 0 then BEGIN
		for cnt := 1 to kMaxPopUp DO types[cnt] := GetLocStr(11004, cnt);
		mT := GetPlugInString(7002);
```
```python
import vs

# Counts all of the objects which match the search criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

count = vs.Count(c)
vs.Message('Count returned: ' + str(count))
```
See also in tutorials: [23. Count Objects by Criteria (Formula-Driven)](ai%20examples/23_WorksheetCountByCriteria.md)

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
