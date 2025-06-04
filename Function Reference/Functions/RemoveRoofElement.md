# RemoveRoofElement

## Description
Procedure RemoveRoofElement removes the specified roof element from the referenced roof.

```pascal
PROCEDURE RemoveRoofElement(
				roofObject : HANDLE;
				id         : INTEGER);
```

```python
def vs.RemoveRoofElement(roofObject, id):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|id|INTEGER|Index of dormer element.|

## Remarks
id is the value returned from Create...Dormer() or CreateSkylight() routine.

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
