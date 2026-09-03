# SetVPLayerVisibility

## Description
Sets the visibility for the specified layer in the specified viewport.

```pascal
FUNCTION SetVPLayerVisibility(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				visibilityType : INTEGER): BOOLEAN;
```

```python
def vs.SetVPLayerVisibility(viewportHandle, layerHandle, visibilityType):
    return BOOLEAN
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
	FOR j := 1 TO gViewPortInfo [sheetNum].NumLayers DO
		OK := SetVPLayerVisibility (viewportH, GetLayerByName (gViewPortInfo [sheetNum].LayerName [j]), gViewPortInfo [sheetNum].LayerVisibility [j]);

{//// create an empty temp layer and make it visible in the viewport }
tempLayName := CreateUUID;
tempLayHand := CreateLayer( tempLayName, 1 );
boo := SetVPLayerVisibility( testVPHand, tempLayHand, 0 );

BEGIN
	OK := SetVPLayerVisibility (viewportH, layerH, GetObjectVariableInt (layerH, 153));
	IF frontH <> NIL THEN
		OK := SetVPLayerVisibility (frontH, layerH, GetObjectVariableInt (layerH, 153));
	IF rightH <> NIL THEN
		OK := SetVPLayerVisibility (rightH, layerH, GetObjectVariableInt (layerH, 153));
```
```python
import vs

# Sets the visibility for the specified layer in the specified viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer
visibilityType = 0

ok = vs.SetVPLayerVisibility(viewportHandle, layerHandle, visibilityType)
if ok:
    vs.Message('SetVPLayerVisibility succeeded')
else:
    vs.Message('SetVPLayerVisibility failed')
```

## Version
Availability: from VectorWorks 11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
