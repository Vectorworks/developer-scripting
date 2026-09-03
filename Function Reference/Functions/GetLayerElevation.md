# GetLayerElevation

## Description
Gets the elevation and thickness of the specified layer.

```pascal
PROCEDURE GetLayerElevation(
				h             : HANDLE;
				VAR baseElev  : REAL;
				VAR thickness : REAL);
```

```python
def vs.GetLayerElevation(h):
    return (baseElev, thickness)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the layer|
|baseElev|REAL|Base elevation of the layer|
|thickness|REAL|Thickness of the layer|

## Remarks
[[User:Orso.b.schmid| orso]] 2006.11.25: Please note that this routines always returns millimeters.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    h :HANDLE; 
    baseElev, thickness :REAL;
BEGIN
    h := FLayer;
    WHILE h <> NIL DO BEGIN
        GetLayerElevation(h, baseElev, thickness);
        thickness := thickness / (25.4 / GetPrefReal(152)); { convert from mm to current units }
        AlrtDialog(Concat('layer name: ', GetLName(h), ', baseElev: ', baseElev, ', thickness: ', thickness));
        h := NextLayer(h);
    END;
END;
RUN(Example);
```
#### Python ####
```python
def Example():
    h = vs.FLayer()
    while h != None:
        baseElev, thickness = vs.GetLayerElevation(h)
        thickness = thickness / (25.4 / vs.GetPrefReal(152)) #{ convert from mm to current units }
        vs.AlrtDialog(vs.Concat('layer name: ', vs.GetLName(h), ', baseElev: ', baseElev, ', thickness: ', thickness))
        h = vs.NextLayer(h)
Example()
```

```pascal
{ convert found wall bottom Z from global to layer coordinates. }
GetLayerElevation( GetLayer( gWallHand ), layerElev, layerThick );
layerElev   := layerElev * ( GetPrefReal( 152 ) / 25.4 );	{ convert to doc units. }
wallBottomZ := ( wallBottomZ - layerElev );					{ to layer coordinates. }

{Remove layer elevation for certain objects due to their specific workflow}
IF gObjectTypeName = GetMyPluginString(5032) THEN BEGIN		{ Slab	}
	GetLayerElevation(GetLayer(gPluginObjH), layerElevation, dummy);
	layerElevation := layerElevation * ( GetPrefReal( 152 ) / 25.4 );	{ convert to doc units. }
	matZ1 := matZ1 - layerElevation;
END;

BEGIN
	result := GetEntityMatrix(objectHand, matX1,matY1,matZ1,matAngleX,matAngleY,matAngleZ);
	layerH := GetLayer( objectHand );
	GetLayerElevation( layerH, layerElevation, layerThickness );
```
```python
import vs

# Gets the elevation and thickness of the specified layer.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

baseElev, thickness = vs.GetLayerElevation(h)
vs.Message('GetLayerElevation returned: ' + str((baseElev, thickness)))
```

## See Also
VS Functions:
[SetLayerElevation](SetLayerElevation.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Layers](../Categories/Layers.md)
