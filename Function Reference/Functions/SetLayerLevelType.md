# SetLayerLevelType

## Description
Sets the Layer Level Type of a Layer. If the type passed in does not exist or if it already used by another Layer on the same Story, then the operation will fail.

```pascal
FUNCTION SetLayerLevelType(
				layer          : HANDLE;
				layerLevelType : STRING): BOOLEAN;
```

```python
def vs.SetLayerLevelType(layer, layerLevelType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|The Layer for which the Layer Level Type is being set.|
|layerLevelType|STRING|The Layer Level Type.|

## Examples
```pascal
SetLayerLevelType(ActLayer, 'LT_SLAB');
```

```pascal
layerH := GetLayerByName(UserLayerName);
if ( (storyDL = TRUE ) AND (gSheetInfo [sheetNum].SheetType = 3) ) THEN BEGIN
	if hStory <> NIL THEN BEGIN
		IF foundLevelType THEN BEGIN
			OK := SetLayerLevelType( layerH, storyLevel );
		END;
```
```python
import vs

# Sets the Layer Level Type of a Layer.
layer = vs.ActLayer()  # handle to the active design layer
layerLevelType = 'Design Layer-1'

ok = vs.SetLayerLevelType(layer, layerLevelType)
if ok:
    vs.Message('SetLayerLevelType succeeded')
else:
    vs.Message('SetLayerLevelType failed')
```

## See Also
VS Functions:
[GetLayerLevelType](GetLayerLevelType.md) 
| [CreateLayerLevelType](CreateLayerLevelType.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
