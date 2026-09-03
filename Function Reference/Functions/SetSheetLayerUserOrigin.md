# SetSheetLayerUserOrigin

## Description
Sets the user origin of the specified sheet layer.

```pascal
FUNCTION SetSheetLayerUserOrigin(
				layerHandle : HANDLE;
				xOrigin     : REAL;
				yOrigin     : REAL): BOOLEAN;
```

```python
def vs.SetSheetLayerUserOrigin(layerHandle, xOrigin, yOrigin):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layerHandle|HANDLE|   |
|xOrigin|REAL|   |
|yOrigin|REAL|   |

## Examples
```pascal
sheetLayerH := ActLayer;
bSheetLayer := FALSE;
IF (sheetLayerH <> nil) & (GetObjectVariableInt(sheetLayerH, 154) = 2) THEN BEGIN
	boo := GetSheetLayerUserOrigin(sheetLayerH,  sheetOriginX, sheetOriginY);
	boo := SetSheetLayerUserOrigin(sheetLayerH, 0, 0);
	bSheetLayer := TRUE;
END;

sheetLayerH := ActLayer;
bSheetLayer := FALSE;
IF (sheetLayerH <> nil) & (GetObjectVariableInt(sheetLayerH, 154) = 2) THEN BEGIN
	result := GetSheetLayerUserOrigin(sheetLayerH,  sheetOriginX, sheetOriginY);
	result := SetSheetLayerUserOrigin(sheetLayerH, 0, 0);
	bSheetLayer := TRUE;
END;

sheetLayerH := ActLayer;
bSheetLayer := FALSE;
IF (sheetLayerH <> nil) & (GetObjectVariableInt(sheetLayerH, 154) = 2) THEN BEGIN
	boo := GetSheetLayerUserOrigin(sheetLayerH, sheetOrigin.x, sheetOrigin.y);
	boo := SetSheetLayerUserOrigin(sheetLayerH, 0, 0);
	bSheetLayer := TRUE;
END;
```
```python
import vs

# Sets the user origin of the specified sheet layer.
layerHandle = vs.ActLayer()  # handle to the active design layer
xOrigin = 1.0
yOrigin = 2.0

ok = vs.SetSheetLayerUserOrigin(layerHandle, xOrigin, yOrigin)
if ok:
    vs.Message('SetSheetLayerUserOrigin succeeded')
else:
    vs.Message('SetSheetLayerUserOrigin failed')
```

## Version
Availability: from VectorWorks10.5

## Category
* [Layers](../Categories/Layers.md)
