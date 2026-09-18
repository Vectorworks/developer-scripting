# OLDGetMatDensity

## Description
Returns the density of the specified construction material.

```pascal
FUNCTION OLDGetMatDensity(materialName : STRING) : REAL;
```

```python

def vs.OLDGetMatDensity(materialName):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|materialName|STRING||

## Examples
```pascal
resultVal := OLDGetMatDensity('Example');
```
```python
import vs

# Returns the density of the specified construction material.
materialName = 'Example'

value = vs.OLDGetMatDensity(materialName)
vs.Message('OLDGetMatDensity returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss Analysis.md)
