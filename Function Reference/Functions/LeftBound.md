# LeftBound

## Description
_[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)_. See [LeftBoundN](LeftBoundN.md) for a replacement.

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
#### VectorScript ####
```pascal
LeftBValue:=LeftBound(N='MyRect');
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
result = vs.LeftBound(c)
```

## Version
Availability: from All Versions
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Criteria](../Categories/Criteria.md)
