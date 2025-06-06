# CriteriaVolume

## Description
_[Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)_. See [VolumeN](VolumeN.md) for a replacement.

Returns the volume of the items matching the specified criteria. If more than one object matches the search criteria, the sum of all the volumes of the matching objects will be returned. 

CriteriaVolume will return only return volumes on objects which support the solids modelling functions.

```pascal
FUNCTION CriteriaVolume(c : CRITERIA): REAL;
```

```python
def vs.CriteriaVolume(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Remarks
This function returns the volume of the items matching the current criteria.  It will return 0 for any objects that will not work with the solids modeling functions.

## Examples
#### VectorScript ####
```pascal
totalVol := CriteriaVolume((C = 'Empty Space'));
```
#### Python ####
```python
totalVol = vs.CriteriaVolume(("C = 'Empty Space'"))
```

## Version
Availability: from VectorWorks12.0
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Criteria](../Categories/Criteria.md)
