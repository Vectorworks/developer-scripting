# GetName

## Description
Function GetName returns the object name of the referenced object. The function returns "None" if the object has no object name.

A handle to layer may not passed to this routine; to obtain a layer name, use [ GetLName](GetLName.md).

```pascal
FUNCTION GetName(h : HANDLE): STRING;
```

```python
def vs.GetName(h):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
*\_c\_* (2016.02.18): If the string 'none' is returned (and not 'None' as stated above) this is not localized. Checked in the German VW.

(Unsigned): 
This function is a little non-intuitive. If the namestring of object h is empty, this function returns the literal string "none". I don't know what the localization implications of this are.

If the name has been deleted it returns an empty string, so test for both (empty string or "none" string).

## Examples
#### VectorScript ####
```pascal
ObjectName := GetName(HandleToObject);
```
#### Python ####
```python
ObjectName = vs.GetName(vs.FSActLayer())
```

```pascal
BEGIN
	PushAttrs;
	recordName := GetName (recordH);
	upi := GetPrefReal (152);

recordName := GetName (recordH);
upi := GetPrefReal (152);

BEGIN
	j := j + 1;
	ALLOCATE gRecordN [1..j];
	gRecordN [j] := GetName (recordH);
END;
```
```python
if (parentRecord != None) and (vs.GetTypeN(parentRecord) == kRecordNode):
	strParentName = vs.GetName(parentRecord)

if ( objH == None ) or ( vs.IsNewCustomObject( vs.GetName( objH ) ) ):
	containerHandle = vs.ActLayer()
else:
	containerHandle = objH
```
See also in tutorials: [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [25. Geometric Property Extraction Table](ai%20examples/25_WorksheetPolyGeometry.md), [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md), [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## See Also
VS Functions:
[SetName](SetName.md)

## Version
Availability: from All Versions

## Category
* [Object Names](../Categories/Object%20Names.md)
