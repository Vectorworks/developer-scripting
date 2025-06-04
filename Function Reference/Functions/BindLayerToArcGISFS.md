# BindLayerToArcGISFS

## Description
Associate the active design layer with the ArcGIS feature service and bring in georeferenced shapes and data. The parameter inRequestAll specifies the extent of the requested features. If inRequestAll = FALSE it will request features overlapping the view region otherwise it will request all features on the feature layer.

```pascal
PROCEDURE BindLayerToArcGISFS(
				inURL        : STRING;
				inFeatureId  : STRING;
				inRequestAll : BOOLEAN);
```

```python
def vs.BindLayerToArcGISFS(inURL, inFeatureId, inRequestAll):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inURL|STRING|   |
|inFeatureId|STRING|   |
|inRequestAll|BOOLEAN|   |

## Version
Availability: from Vectorworks 2023

## Category
* [GIS](../Categories/GIS.md)
