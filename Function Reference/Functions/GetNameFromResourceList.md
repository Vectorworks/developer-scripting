# GetNameFromResourceList

## Description
Returns the name to display of the indicated item in the specified resource list.  If the list has items with the same name from different files, the display name will have the filename added to it in parentheses.

```pascal
FUNCTION GetNameFromResourceList(
				listID : LONGINT;
				index  : LONGINT): STRING;
```

```python
def vs.GetNameFromResourceList(listID, index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resouce list created by the BuildResourceList function.|
|index|LONGINT|an index into the list.|

## Remarks
To get the actual name use GetActualNameFromResourceList.

## Examples
[WorkingWithResrouceList](examples/WorkingWithResrouceList.md)

## See Also
VS Functions:
[GetActualNameFromResourceList](GetActualNameFromResourceList.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
