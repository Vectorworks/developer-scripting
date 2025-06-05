# CriteriaArea

## Description
<b>[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)</b>. See [AreaN](AreaN.md) for a replacement.

Returns the area of an object. If more than one object matches the search criteria, the function will return the sum of all the matching object areas.

```pascal
FUNCTION CriteriaArea(c : CRITERIA): REAL;
```

```python
def vs.CriteriaArea(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
totalA:=Area((C='Plywood')and(L='First'));
{returns the area of all objects in class 'Plywood' on layer 'First'}
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks12.0
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Criteria](../Categories/Criteria.md)
