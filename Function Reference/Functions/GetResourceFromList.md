# GetResourceFromList

## Description
Returns the indicated resource from the indicated resource list, if the resource is in the current document.  Otherwise it returns nil.

```pascal
FUNCTION GetResourceFromList(
				listID : LONGINT;
				index  : LONGINT): HANDLE;
```

```python
def vs.GetResourceFromList(listID, index):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resource list created by the BuildResourceList command.|
|index|LONGINT|an index into the list.|

## Remarks
You can check the referenced status of a resource with the object preference 700:
```pascal
IsReferenced := GetObjectVariableBoolean(handleToResourceDefinition, 700);
{locked/referenced status }
```

## Examples
[WorkingWithResrouceList](examples/WorkingWithResrouceList.md)

```pascal
BEGIN
	IF GetResourceFromList( defConListID, cnt ) = NIL THEN
	BEGIN
		resourceH := ImportResourceToCurrentFile( defConListID, cnt );
		PIOHand := FInSymDef( resourceH );
		gSymbolInfo [cnt].shapeName := GetName( GetRecord ( PIOHand, (NumRecords(PIOHand))) );
		gSymbolInfo[cnt].deleteMe := TRUE;
		gSymbolInfo[cnt].symbolName := GetSDName( resourceH );

BEGIN
	hAccessible := GetResourceFromList(currentResourceList,index);
	SetName(hAccessible, GetStr5(1));
END;

BEGIN
	IF (folderHandle = GetResourceFromList(listID, listItemIter)) THEN
		didCreateViewsFolder := FALSE;
END;
```
```python
import vs

# Returns the indicated resource from the indicated resource list, if the
# resource is in the current document.
listID = 1
index = 1

objHandle = vs.GetResourceFromList(listID, index)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
