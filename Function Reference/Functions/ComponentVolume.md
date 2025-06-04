# ComponentVolume

## Description
Returns the total 3D volume of the specified component, minus any holes in the 3D object.

```pascal
FUNCTION ComponentVolume(
				c     : CRITERIA;
				index : INTEGER): REAL;
```

```python
def vs.ComponentVolume(c, index):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|The search criteria string.|
|index|INTEGER|The index of the component.|

## Version
Availability: from Vectorworks 2011

## Category
* [Criteria](../Categories/Criteria.md)
