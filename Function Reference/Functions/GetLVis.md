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

```pascal
IF SupportedL <> GetPluginString(3003){All} THEN BEGIN
	IF SupportedL = GetPluginString(3000){Active} THEN
		if GetLayer( H ) <> ActLayer then ok := FALSE;
	IF SupportedL = GetPluginString(3001){Editable} THEN
		if GetLVis( GetLayer( H ) ) = 2{grayed, i.e. non-editable} then ok := FALSE;
END;

BEGIN
IF (GetObjectVariableInt(currLayer, 154) = 1) & (GetLVis(currLayer) = 0) & (GetLScale(currLayer) = actScale)
	& ((GetPref(94) = TRUE) | (GetProjection(currLayer) = 6)) THEN
	BEGIN
	pluginH := FSObject(currLayer);
	while (pluginH <> NIL) Do
		BEGIN
		IF (pluginH <> origObj) THEN
			ApplyMarkerStyleToSEM;

	WHILE (hlyr <> NIL) DO BEGIN
		{** NEW - Check for viewport sheet layers and exclude them from the list [TEU - 1/23/04]}
		{IF (GetLVis(hlyr) <> -1) THEN BEGIN}
{*** NEW 6/8 ***}
		IF (GetLVis(hlyr) <> -1)&(GetObjectVariableInt(hlyr,154)=1) THEN BEGIN

		{* NEW: The instance is not being stripped from the layer name. This change is being implemented 	*}
		{* because custom layer names (particularly AIA) may not have a dash separating the instance and	*}
		{* indiv2type will strip off part of the layer name [TEU-7/17/2003] 						*}

			AddChoice(dialogID,  itemID, GetLName(hlyr), k);
			{AddChoice(dialogID,  itemID, indiv2type(GetLName(hlyr)), k);}
```
```python
import vs

# Function GetLVis returns the visibility of the referenced layer.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetLVis(h)
vs.Message('GetLVis returned: ' + str(resultN))
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
