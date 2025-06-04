# BotBound

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See [[VS:BotBoundN|BotBoundN]] and [[VS:LeftBoundN|LeftBoundN]] for a replacement.

Returns the y-coordinate of the bounding box (bottom right corner) of an object matching the search criteria. If more than one object matches the search criteria, the function will return the bottom value of the last matching object found.

```pascal
FUNCTION BotBound(c : CRITERIA): REAL;
```

```python
def vs.BotBound(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
==== VectorScript ====
```pascal
BotBValue:=BotBound(N='MyRect');
```
==== Python ====
```python

```

## Version
Availability: from All Versions
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Criteria](../Categories/Criteria.md)
