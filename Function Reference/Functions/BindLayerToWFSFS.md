# BindLayerToWFSFS

## Description
Associate the active design layer with the WFS feature service and bring in georeferenced shapes and data. The parameter inRequestAll specifies the extent of the requested features. If inRequestAll = FALSE it will request features overlapping the view region otherwise it will request all features on the feature layer.

```pascal
PROCEDURE BindLayerToWFSFS(
				inURL         : STRING;
				inFeatureName : STRING;
				inRequestAll  : BOOLEAN);
```

```python
def vs.BindLayerToWFSFS(inURL, inFeatureName, inRequestAll):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inURL|STRING|   |
|inFeatureName|STRING|   |
|inRequestAll|BOOLEAN|   |

## Version
Availability: from Vectorworks 2023

## Category
* [GIS](../Categories/GIS.md)
