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
==== VectorScript ====
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
==== Python ====
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

## See Also
VS Functions:
[SetLayerElevation](SetLayerElevation.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Layers](../Categories/Layers.md)
