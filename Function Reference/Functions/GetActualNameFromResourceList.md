# GetActualNameFromResourceList

## Description
Returns the actual name of the indicated item in the specified resource list. This call will delete the filename that is appended for resources with same name from different files.

```pascal
FUNCTION GetActualNameFromResourceList(
				listID : LONGINT;
				index  : LONGINT): STRING;
```

```python
def vs.GetActualNameFromResourceList(listID, index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resouce list created by the BuildResourceList function.|
|index|LONGINT|an index into the list.|

## Remarks
To get the display name use GetNameFromResourceList.

## Examples
[AddHatchToResource](examples/AddHatchToResource.md)

```pascal
BEGIN
FoundMarker := TRUE;
actualMarker1Name := GetActualNameFromResourceList(ResourceListID,I);
IF GetObject(TempStr) = NIL THEN
	BEGIN
	h := ImportResourceToCurrentFile(ResourceListID, I);
	ImportedMarker1 := TRUE;

BEGIN
{Symbol Not Found}
defaultListID := BuildResourceList(16, -kDefConSeatingLayoutSeats, '', defaultListCount);
symbolName := GetActualNameFromResourceList(defaultListID, 1);
IF GetObject(symbolName) = NIL THEN
	BEGIN
	symbolName := GetNameFromResourceList(defaultListID, 1);
	h := ImportResourceToCurrentFile(defaultListID, 1);

Marker1 := GetNameFromResourceList(ResourceListID,Marker1idx);
marker1ActualName := GetActualNameFromResourceList(ResourceListID,Marker1idx);
IF Matching THEN
	BEGIN
	Marker2 := Marker1;
	marker2ActualName := marker1ActualName;
```
```python
if strResName == strMarkerActualName:
	bFoundMarker = True
	strMarkerActualName = vs.GetActualNameFromResourceList( hResourceListID, index )
```

## See Also
VS Functions:
[GetNameFromResourceList](GetNameFromResourceList.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
