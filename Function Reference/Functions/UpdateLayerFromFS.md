# UpdateLayerFromFS

## Description
Update a feature service bound to a layer to get the latest location information or other data. The parameter inRequestAll specifies the extent of the requested features. If inRequestAll = FALSE it will request features overlapping the view region otherwise it will request all features on the feature layer.

```pascal
PROCEDURE UpdateLayerFromFS(inRequestAll : BOOLEAN);
```

```python
def vs.UpdateLayerFromFS(inRequestAll):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inRequestAll|BOOLEAN|   |

## Version
Availability: from Vectorworks 2023

## Category
* [GIS](../Categories/GIS.md)
