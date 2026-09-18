# GetZatXY

## Description
Returns the Z elevation of a point X,Y on the specified object. If hObject = NIL then searches all visible objects; hObject = layer - all objects on the layer

```pascal
FUNCTION GetZatXY(
				hObject  : HANDLE;
				X        : REAL;
				Y        : REAL;
				VAR outZ : REAL): BOOLEAN;
```

```python
def vs.GetZatXY(hObject, X, Y):
    return (BOOLEAN, outZ)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|X|REAL|   |
|Y|REAL|   |
|outZ|REAL|   |

## Examples
```pascal
 		p1x:=p1x-p2x+1";
 		p1y:=p1y-p2y+1";
 		GetSymLoc(LecHand,x,y);
 		HMove(LecHand,p1x,p1y);
 		BSB := GetZatXY(ActLayer,x,y,TotalHeight);
 		HMove(LecHand,-p1x,-p1y);
IF (BSB = TRUE) THEN
BEGIN
	GetLayerElevation(ActLayer, baseElev, thickness);

p1x:=p1x-p2x+1";
p1y:=p1y-p2y+1";
GetSymLoc(ScreenHand,x,y);
HMove(ScreenHand,p1x,p1y);
BSB := GetZatXY(ActLayer,x,y,TotalHeight);
{AlrtDialog(Concat(TotalHeight));}
HMove(ScreenHand,-p1x,-p1y);
{AlrtDialog(Concat(baseElev));}
{AlrtDialog(Concat(TotalHeight));}
```
```python
import vs

# Returns the Z elevation of a point X,Y on the specified object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
X = 0.0
Y = 0.0

ok, outZ = vs.GetZatXY(hObject, X, Y)
vs.Message('GetZatXY returned: ' + str((ok, outZ)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
