# GetSheetLayerUserOrigin

## Description
Gets the user origin of the specified sheet layer.

```pascal
FUNCTION GetSheetLayerUserOrigin(
				layerHandle : HANDLE;
				VAR xOrigin : REAL;
				VAR yOrigin : REAL): BOOLEAN;
```

```python
def vs.GetSheetLayerUserOrigin(layerHandle):
    return (BOOLEAN, xOrigin, yOrigin)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layerHandle|HANDLE|Handle of the layer.|
|xOrigin|REAL|X component of the sheet layer user origin.|
|yOrigin|REAL|Y component of the sheet layer user origin.|

## Version
Availability: from VectorWorks10.5

## Category
* [Layers](../Categories/Layers.md)
