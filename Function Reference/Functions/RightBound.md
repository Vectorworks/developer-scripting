# RightBound

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See [[VS:RightBoundN|RightBoundN]] for a replacement.

Returns the x-coordinate of the bounding box (bottom right corner) of an object matching the search criteria If more than one object matches the search criteria, the function will return the sum of the coordinates of all the matching objects.

```pascal
FUNCTION RightBound(c : CRITERIA): REAL;
```

```python
def vs.RightBound(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Remarks
It would be nice if this would return the rightmost coordinate of the matching objects. Don't see how the sum of coordinates can be of any use.

## Examples
==== VectorScript ====
```pascal
RightBValue:=RightBound(N='MyRect');
```
==== Python ====
```python

```

## Version
Availability: from All Versions
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Criteria](../Categories/Criteria.md)
