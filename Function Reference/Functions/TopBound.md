# TopBound

## Description
_[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)_. See [TopBoundN](TopBoundN.md) for a replacement.

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
#### VectorScript ####
```pascal
TopBValue:=TopBound(N='MyRect');
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
	END ELSE
```
```python
result = vs.TopBound(c)
```

## Version
Availability: from All Versions
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Criteria](../Categories/Criteria.md)
