# Perim

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See [[VS:PerimN|PerimN]] for a replacement.

Returns the perimeter of an object. If more than one object matches the search criteria, the function will return the sum of the matching objects' perimeters.

```pascal
FUNCTION Perim(c : CRITERIA): REAL;
```

```python
def vs.Perim(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
PerimValue := Perim(C='Fence');
{returns the total perimeter of all objects in the class 'Fence'}
```
#### Python ####
```python

```

## Version
Availability: from All Versions
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Criteria](../Categories/Criteria.md)
