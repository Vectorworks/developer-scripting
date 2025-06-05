# Perim

## Description
<b>[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)</b>. See [PerimN](PerimN.md) for a replacement.

Returns the perimeter of an object. If more than one object matches the search criteria, the function will return the sum of the matching objects' perimeters.

```pascal
FUNCTION Perim(c : CRITERIA): REAL;
```

```python
def vs.Perim(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
PerimValue := Perim(C='Fence');
{returns the total perimeter of all objects in the class 'Fence'}
```
#### Python ####
```python

```

## Version
Availability: from All Versions
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Criteria](../Categories/Criteria.md)
