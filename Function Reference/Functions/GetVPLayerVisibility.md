# GetVPLayerVisibility

## Description
Gets the visibility for the specified layer in the specified viewport.

```pascal
FUNCTION GetVPLayerVisibility(
				viewportHandle     : HANDLE;
				layerHandle        : HANDLE;
				VAR visibilityType : INTEGER): BOOLEAN;
```

```python
def vs.GetVPLayerVisibility(viewportHandle, layerHandle):
    return (BOOLEAN, visibilityType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |
|layerHandle|HANDLE|   |
|visibilityType|INTEGER|   |

## Remarks
visibilityType values: 
* -1 invisible, 
* 0 visible, 
* 2 gray

## Examples
```pascal
BEGIN
	OK := GetVPLayerVisibility (viewportH, layerH, tempVis);
	tempVis := Abs (tempVis);
	CASE tempVis OF
		0: SetObjectVariableInt (layerH, 153, 0);
		1: SetObjectVariableInt (layerH, 153, -1);

BEGIN
IF ((GetObjectVariableInt(layerH,154) = 1) & (GetVPLayerVisibility(viewportH, layerH ,tempint))) THEN
	BEGIN
	Layer(GetLName(layerH));
	CASE tempint OF
		1,-1: HideLayer;
		2,-2: GrayLayer;
		OTHERWISE ShowLayer;

BEGIN
	OK := GetVPLayerVisibility (h, layerH, tempInt);
	tempInt := Abs (tempInt);
	IF (tempInt = 0) | (tempInt = 2) THEN
	BEGIN
		gViewPortInfo [gNumSheets2].NumLayers := gViewPortInfo [gNumSheets2].NumLayers + 1;
```
```python
import vs

# Gets the visibility for the specified layer in the specified viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer

ok, visibilityType = vs.GetVPLayerVisibility(viewportHandle, layerHandle)
vs.Message('GetVPLayerVisibility returned: ' + str((ok, visibilityType)))
```

## Version
Availability: from VectorWorks 11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
