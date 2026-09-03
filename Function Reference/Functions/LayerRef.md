# LayerRef

## Description
Procedure LayerRef places a layer reference (layer link) into the active layer at location (0,0).

```pascal
PROCEDURE LayerRef(layerName : STRING);
```

```python
def vs.LayerRef(layerName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layerName|STRING|Name of referenced layer.|

## Examples
#### VectorScript ####
```pascal
LayerRef('Layer-2');
{creates a layer link of 'Layer-2' on the active layer}
```
#### Python ####
```python

```

```pascal
IF getpref(21) THEN setpref(21,FALSE); {eliminate later!!?}
FOR temp_i := 1 TO listCount DO IF layerStatusList[temp_i] THEN BEGIN
	temp_h := getobject(LayerNameList[temp_i]);
	GetLayerElevation(temp_h,temp_z,temp_dz);
	layerRef(LayerNameList[temp_i]);
	tempLL_h := lactlayer;
	setobjectvariableboolean(tempLL_h,700,FALSE);{unlock LL}
	IF NOT(layerhas3D(temp_h)) THEN SetObjectVariableBoolean(tempLL_h,161,TRUE);{new RFA 12/16/02}
	temp_z := gUPI * temp_z / 25.4;
```
```python
vs.LayerRef('Design Layer-1')
```

## Version
Availability: from MiniCAD4.0

## Category
* [Layers](../Categories/Layers.md)
