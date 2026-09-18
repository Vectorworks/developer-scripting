# Get3DInfo

## Description
Procedure Get3DInfo returns the height, width and depth values of the referenced 3D object.

```pascal
PROCEDURE Get3DInfo(
				h          : HANDLE;
				VAR height : REAL;
				VAR width  : REAL;
				VAR depth  : REAL);
```

```python
def vs.Get3DInfo(h):
    return (height, width, depth)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to 3D object.|
|height|REAL|Height of object.|
|width|REAL|Width of object.|
|depth|REAL|Depth of object.|

## Remarks
The "height, width, depth" order of the parameters in this call is misleading. The call returns delta-Y, delta-X and delta-Z IN THAT ORDER. Screwy, I know. The example is not a good one because it makes no use of the X and Y data.

## Examples
[Manipulate3DObjects](examples/Manipulate3DObjects.md)

```pascal
Get3DInfo(ObjH, x_span, y_span, z_span);
Get3DCntr(ObjH, garb_r, garb_r, z_center);
{base_elev is used only when the symbol is in wall}
theHeight := z_center - (z_span / 2);

	AppendRoofEdge(gRoofH,gXtemp,gYtemp,pRoofPitch,pOverhang,pHeight-gAdjust);
	END;
ResetObject(gRoofH);
Add_Holes_TO_Roof(gRoofH);
Get3DInfo(gRoofH,temp_r,temp_r,temp_r);
IF (pDrawPitchedRoof & (temp_r < pRoofThk))THEN {sloped roof has failed}
	BEGIN
		SetRField(gMyHand,gMyName,'DrawPitchedRoof','FALSE');
		gFlatRoof := TRUE;

Get3DInfo( h, garb_r, garb_r, z_span );
Get3DCntr( h, garb_r, garb_r, z_center );
z_center := z_center + ( z_span / 2 );
GetZVals(actLayerElev, actLayerThick);
z_center := z_center  - actLayerElev;
```
```python
import vs

# Procedure Get3DInfo returns the height, width and depth values of the
# referenced 3D object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

height, width, depth = vs.Get3DInfo(h)
vs.Message('Get3DInfo returned: ' + str((height, width, depth)))
```

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
