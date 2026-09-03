# Width

## Description
Returns the width of an object matching the search criteria. If more than one object matches the search criteria, the function will return the sum of the matching object widths.

```pascal
FUNCTION Width(c : CRITERIA): REAL;
```

```python
def vs.Width(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
WidthValue:=Width(N='Box');
```
#### Python ####
```python

```

```pascal
{====================================================================}
{	PROCEDURE DrawBeam2DWidth;	Draws the 2D Width (rectangle) Joist representation
{====================================================================}
PROCEDURE DrawBeam2DWidth;
BEGIN
	{ draw the 2D bounding rectangle of the Joist}
```
```python
result = vs.Width(c)
```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
