# LeftBound

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See [[VS:LeftBoundN|LeftBoundN]] for a replacement.

Returns the x-coordinate of the bounding box (top left corner) of an object matching the search criteria. If more than one object matches the search criteria, the function will return the left value of the last matching object found.

```pascal
FUNCTION LeftBound(c : CRITERIA): REAL;
```

```python
def vs.LeftBound(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
==== VectorScript ====
```pascal
LeftBValue:=LeftBound(N='MyRect');
```
==== Python ====
```python

```

## Version
Availability: from All Versions
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Criteria](../Categories/Criteria.md)
