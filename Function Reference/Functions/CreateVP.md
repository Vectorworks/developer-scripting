# CreateVP

## Description
Creates a viewport object. The specified parent handle may only be a layer or a group contained within a layer, nested or otherwise.

```pascal
FUNCTION CreateVP(parentHandle : HANDLE): HANDLE;
```

```python
def vs.CreateVP(parentHandle):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|parentHandle|HANDLE|   |

## Remarks
(*\_c\_*, 2015.02.25):  This invariably creates a VP with scale 1:1, view top-plan and all layers and classes set to invisible.

## Examples
```pascal
IF viewPortH = NIL THEN viewportH := CreateVP (sheetLayerH)
ELSE OK := SetParent (viewPortH, sheetLayerH);

{ create the viewport }
viewportH := CreateVP (onSheetLayer);

BEGIN
	gActLayerH := ActLayer;
	viewportH := CreateVP(LayerHand);
	layerH := FLayer;
	WHILE layerH <> NIL DO
	BEGIN
		{ check to be sure this is a not a sheet layer }
```
```python
import vs

# Creates a viewport object.
parentHandle = vs.ActLayer()  # parent container (the active layer)

objHandle = vs.CreateVP(parentHandle)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks 11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
