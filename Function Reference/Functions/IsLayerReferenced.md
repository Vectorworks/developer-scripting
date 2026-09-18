# IsLayerReferenced

## Description
Returns whether a layer is workgroup referenced, and if so, the path to the source document is returned.

```pascal
FUNCTION IsLayerReferenced(
				layer        : HANDLE;
				VAR pathname : STRING): BOOLEAN;
```

```python
def vs.IsLayerReferenced(layer):
    return (BOOLEAN, pathname)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|Handle to the layer|
|pathname|STRING|On return, a string containing the path to the source document|

## Remarks
This returns FALSE on broken references to layers belonging to files residing on external disks. 
It is not correct, even if the reference is broken, the layer is nevertheless referenced, so the routine should return TRUE. (VW 13-83388).

Use the pref object boo 700, instead, it is more secure:
```pascal
IsReferenced := GetObjectVariableBoolean(handleToResourceDefinition, 700); { locked/referenced status }
```

## Examples
```pascal
BEGIN
	IF (NOT IsLayerReferenced(layerHdl, LayerRefPath)) & (GetObjectVariableInt(layerHdl,154) = 1) THEN
		BEGIN
		layerNm := GetLName(layerHdl);
		AddChoice(LayerDlgID, 12, layerNm, index);
		index := index +1;
		END;
```
```python
import vs

# Returns whether a layer is workgroup referenced, and if so, the path to the
# source document is returned.
layer = vs.ActLayer()  # handle to the active design layer

ok, pathname = vs.IsLayerReferenced(layer)
vs.Message('IsLayerReferenced returned: ' + str((ok, pathname)))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Layers](../Categories/Layers.md)
