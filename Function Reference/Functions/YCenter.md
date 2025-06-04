# YCenter

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See [[VS:YCenterN|YCenterN]] for a replacement function.


Returns the y-coordinate of the center point of an object matching the serach criteria. If more than one object matches the search criteria, the function will return the sum of the coordinates of all the matching objects.

```pascal
FUNCTION YCenter(c : CRITERIA): REAL;
```

```python
def vs.YCenter(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
YCenValue:=YCenter(N='Board');
{returns the y-coord of the center of the named object 'Board'}
```
#### Python ####
```python

```

## Version
Availability: from All Versions
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Criteria](../Categories/Criteria.md)
