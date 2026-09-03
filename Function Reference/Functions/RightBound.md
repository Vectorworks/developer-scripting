# RightBound

## Description
_[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)_. See [RightBoundN](RightBoundN.md) for a replacement.

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
#### VectorScript ####
```pascal
RightBValue:=RightBound(N='MyRect');
```
#### Python ####
```python

```

```pascal
BEGIN
	currentUIP		:= GetPrefReal(152);
	symWidth		:= ( RightBound( N=symbolName ) / currentUIP ) - ( LeftBound( N=symbolName ) / currentUIP );
	symHeight		:= ( TopBound( N=symbolName ) / currentUIP ) - ( BotBound( N=symbolName ) / currentUIP );
	IF ( ( symWidth - kSymbolDisplayWidth ) > ( symHeight - symbolDisplayHeight ) ) THEN
	BEGIN
		scaleFactor := kSymbolDisplayWidth / symWidth;
```
```python
result = vs.RightBound(c)
```

## Version
Availability: from All Versions
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Criteria](../Categories/Criteria.md)
