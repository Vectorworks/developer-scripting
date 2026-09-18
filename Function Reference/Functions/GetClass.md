# GetClass

## Description
Function GetClass returns the class assigned to the referenced object. None is returned if the object has no class assigned to it.

```pascal
FUNCTION GetClass(h : HANDLE): STRING;
```

```python
def vs.GetClass(h):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
#### VectorScript ####
```pascal
ObjectClass:=GetClass(handleToObject);
```
#### Python ####
```python
ObjectClass = vs.GetClass(handleToObject)
```

```pascal
BEGIN
	gClassN := getClass( gLine );
	SetClass( gParmH, gClassN );
	{ When creating the object, SetClass regenerates it in Screen Plane.
		TO fix this we will SET it in the same plane with the gLine }
	planarRef := GetPlanarRef( gLine );

BEGIN	{ Main }
	{DselectAll;}
	{IF SetUpObject( gPluginName, gPluginH, recordH, wallH, saveClass, noneClass ) THEN}
	{BEGIN}
		IF kUseContainerClass THEN NameClass( GetClass( gPluginH ) );

BEGIN
	{SetRField(hObj, kRedlinePathObjName, kRedlinePathObjMemoField, gErrStr);}
	SetRField(hObj, kRedlinePathObjName, kRedlinePathObjPickedUpField, Concat(FALSE));
	SetClass(hObj, GetClass(hObj));
END
```
```python
if objectHand != None:
	noneClass = vs.GetClass( objectHand )
	succeeded = True

if ( len(gCurb_Class) == 0 ): gCurb_Class = vs.GetClass( gObjHandle )
if ( len(gPaving_Class) == 0 ): gPaving_Class = vs.GetClass( gObjHandle )
```
See also in tutorials: [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md), [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
