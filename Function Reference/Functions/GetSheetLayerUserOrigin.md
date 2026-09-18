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

SetOriginAbsolute(0, 0);
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

# Gets the user origin of the specified sheet layer.
layerHandle = vs.ActLayer()  # handle to the active design layer

ok, xOrigin, yOrigin = vs.GetSheetLayerUserOrigin(layerHandle)
vs.Message('GetSheetLayerUserOrigin returned: ' + str((ok, xOrigin, yOrigin)))
```

## Version
Availability: from VectorWorks10.5

## Category
* [Layers](../Categories/Layers.md)
