# GetLayerByName

## Description
Returns a handle to the specified layer.

```pascal
FUNCTION GetLayerByName(layerName : STRING): HANDLE;
```

```python
def vs.GetLayerByName(layerName):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layerName|STRING|Name of layer.|

## Examples
```pascal
{ 3D or plan rotation }
IF (( NOT ( ( GetProjection( GetLayerByName( pluginLayer ) ) ) = 6 ) ) |  GetPref(92)) &  (GetObjectVariableInt(GetLayer(gPluginH), 154) = 1 ) THEN
BEGIN
	Move3DObj( gPluginH, (CenterX - CurX), (CenterY - CurY), -Zval );
END

{Delete temp working layer}
hTempLayer := FLayer;
hResLayer := GetLayerByName(kStrErrorLayer);
IF hResLayer <> NIL THEN
	BEGIN
	If  (hTempLayer = hResLayer) AND (NextLayer(hTempLayer) = hResLayer) THEN
		Message('Error')

		END;
	hTempLayer := NextLayer(hTempLayer);
	END;
GetSelectedChoiceInfo(dialog1,  5,0,popup5Int,popup5Str);
gDstLayerScale := GetLScale(GetLayerByName(popup5Str));
gDispScale := gDstLayerScale;
checkBox6 := gDrawGrid;
SetBooleanItem(dialog1,  6,gDrawGrid);	{Draw Background Grid}
checkBox8 := gDrawExisting;
```
```python
import vs

# Returns a handle to the specified layer.
layerName = 'Design Layer-1'

objHandle = vs.GetLayerByName(layerName)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks8.5

## Category
* [Layers](../Categories/Layers.md)
