# BotBound

## Description
<b>[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)</b>. See [BotBoundN](BotBoundN.md) and [LeftBoundN](LeftBoundN.md) for a replacement.

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
#### VectorScript ####
```pascal
BotBValue:=BotBound(N='MyRect');
```
#### Python ####
```python

```

## Version
Availability: from All Versions
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Criteria](../Categories/Criteria.md)
