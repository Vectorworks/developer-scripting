# SetInvisLayersOFF

## Description
Sets the invisible exported DXF layers to OFF

```pascal
PROCEDURE SetInvisLayersOFF(invisLayerOFF : BOOLEAN);
```

```python

def vs.SetInvisLayersOFF(invisLayerOFF):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|invisLayerOFF|BOOLEAN||

## Examples
```pascal
SetInvisLayersOFF(TRUE);
```
```python
import vs

# Sets the invisible exported DXF layers to OFF.
invisLayerOFF = False

vs.SetInvisLayersOFF(invisLayerOFF)
```

## Version
Availability: from Vectorworks 2024.6

## Category
* [ImportExport](../Categories/ImportExport.md)
