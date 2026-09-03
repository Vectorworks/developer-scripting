# DeleteResourceFromList

## Description
Deletes the indicated object in the specified resource list.

```pascal
PROCEDURE DeleteResourceFromList(
				listID : LONGINT;
				index  : LONGINT);
```

```python
def vs.DeleteResourceFromList(listID, index):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resource list created by the BuildResourceList function.|
|index|LONGINT|an index into the list.|

## Examples
[WorkingWithResrouceList](examples/WorkingWithResrouceList.md)

```pascal
BEGIN
DeleteResourceFromList (defaultListID, i);
defaultListCount := defaultListCount - 1;
END;

BEGIN
DeleteResourceFromList(ResourceListID,cnt);
NumResources := NumResources -1;
END
```
```python
import vs

# Deletes the indicated object in the specified resource list.
listID = 1
index = 1

vs.DeleteResourceFromList(listID, index)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
