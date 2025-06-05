# GetLVis

## Description
Function GetLVis returns the visibility of the referenced layer.

**Table - Layer Visibility**

| Visibility | Index Value |
|------------|-------------|
| Normal     | 0           |
| Grayed     | 2           |
| Invisible  | -1          |

```pascal
FUNCTION GetLVis(h : HANDLE): INTEGER;
```

```python
def vs.GetLVis(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Remarks
Note that this returns the state of the layer, as determined in the Layers... dialog, not whether or not the layer is actually visible on the screen. If Layer Options is set to Active Only, a "visible" layer will not be "visible" on the screen unless it is the active layer. This is the same behavior as GetObjectVariableInt(layerHandle, 153), which only returns the layer's visibility setting, not whether or not it's actually visible.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
FUNCTION GetLayerVisibility(layerHandle :handle) :INTEGER;
{Returns the effective visibility of a layer.}
BEGIN
    GetLayerVisibility := -1;
    IF layerHandle = ActLayer THEN GetLayerVisibility := 0 ELSE {Active layers are always visible.}
    IF (GetObjectVariableInt(ActLayer, 154) = 1) & (GetObjectVariableInt(layerHandle, 154) = 1) THEN BEGIN
        {If it's not the active layer, then the only way that it can be visible is if
the active layer is a design layer, and so is layerHandle, and the combination
of layer options and the layer's visibility will result in a visible layer.}
        IF (GetLayerOptions = 2) & (GetLVis(layerHandle) = 2) THEN GetLayerVisibility := 2 ELSE
        IF (GetLayerOptions = 2) & (GetLVis(layerHandle) = 0) THEN GetLayerVisibility := 2 ELSE
        IF (GetLayerOptions > 2) & (GetLVis(layerHandle) = 2) THEN GetLayerVisibility := 2 ELSE
        IF (GetLayerOptions > 2) & (GetLVis(layerHandle) = 0) THEN GetLayerVisibility := 0;
    END;
END;
BEGIN
    Message(GetLVis(GetLayerByName('Layer-1')));
END;
RUN(Example);
```
#### Python ####
```python
def GetLayerVisibility(layerHandle):
	#{Returns the effective visibility of a layer.}
	GetLayerVisibility = -1
	if layerHandle == vs.ActLayer(): 
		GetLayerVisibility = 0 #{Active layers are always visible.}
	if (vs.GetObjectVariableInt(vs.ActLayer(), 154) == 1) and (vs.GetObjectVariableInt(layerHandle, 154) == 1):
	#{If it's not the active layer, then the only way that it can be visible is if
	#the active layer is a design layer, and so is layerHandle, and the combination
	#of layer options and the layer's visibility will result in a visible layer.}
		if (vs.GetLayerOptions() == 2) and (vs.GetLVis(layerHandle) == 2):
			GetLayerVisibility = 2 
		elif (vs.GetLayerOptions() == 2) and (vs.GetLVis(layerHandle) == 0):
			GetLayerVisibility = 2
		elif (vs.GetLayerOptions() > 2) and (vs.GetLVis(layerHandle) == 2):
			GetLayerVisibility = 2
		elif (vs.GetLayerOptions() > 2) and (vs.GetLVis(layerHandle) == 0):
			GetLayerVisibility = 0

def Example():
	GetLayerVisibility(vs.ActLayer())
	vs.Message(vs.GetLVis(vs.GetLayerByName('Layer-1')))

Example()
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
