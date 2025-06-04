# Angle

## Description
Returns the angle value of a line segment or an arc. If more than one line segment or arc matches the search criteria, the function will return the sum of the matching objects' angle values.

```pascal
FUNCTION Angle(c : CRITERIA): REAL;
```

```python
def vs.Angle(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
aValue:=Angle(N='LineSeg');
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
