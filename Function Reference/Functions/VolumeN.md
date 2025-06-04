# VolumeN

## Description
Returns the volume of the items matching the specified criteria. If more than one object matches the search criteria, the sum of all the volumes of the matching objects will be returned. <BR>
<BR>
VolumeN will only return volumes on objects which support the solids modelling functions.

```pascal
FUNCTION VolumeN(c : CRITERIA): REAL;
```

```python
def vs.VolumeN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
totalVol:=VolumeN((C='Empty Space'));
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
