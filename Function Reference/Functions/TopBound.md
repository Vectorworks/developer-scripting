# TopBound

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See [[VS:TopBoundN|TopBoundN]] for a replacement.

Returns the y-coordinate of the bounding box (top left corner) of an object matching the search criteria. If more than one object matches the search criteria, the function will return the sum of the coordinates of all the matching objects.

```pascal
FUNCTION TopBound(c : CRITERIA): REAL;
```

```python
def vs.TopBound(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
==== VectorScript ====
```pascal
TopBValue:=TopBound(N='MyRect');
```
==== Python ====
```python

```

## Version
Availability: from All Versions
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Criteria](../Categories/Criteria.md)
