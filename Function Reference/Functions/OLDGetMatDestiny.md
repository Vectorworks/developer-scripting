# OLDGetMatDestiny

## Description
Returns the density of the specified construction material.

```pascal
FUNCTION OLDGetMatDestiny(materialName : STRING) : REAL;
```

```python

def vs.OLDGetMatDestiny(materialName):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|materialName|STRING||

## Examples
```pascal
resultVal := OLDGetMatDestiny('Example');
```
```python
import vs

# Returns the density of the specified construction material.
materialName = 'Example'

value = vs.OLDGetMatDestiny(materialName)
vs.Message('OLDGetMatDestiny returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss Analysis.md)
