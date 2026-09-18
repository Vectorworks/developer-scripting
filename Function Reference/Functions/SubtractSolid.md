# SubtractSolid

## Description
Function SubtractSolid creates a new solid subtraction object from the referenced source objects.

**Table - Solids Operation Result Codes**

| Operation Result     | Result Code |
|----------------------|-------------|
| Success              | 0           |
| Null geometry error  | 1           |
| Geometry error       | 2           |
| Out of memory error  | 4           |
| Bad group error      | 5           |
| Invalid object type  | 6           |
| Bad input            | 20          |

```pascal
FUNCTION SubtractSolid(
				obj1         : HANDLE;
				obj2         : HANDLE;
				VAR newSolid : HANDLE): INTEGER;
```

```python
def vs.SubtractSolid(obj1, obj2):
    return (INTEGER, newSolid)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj1|HANDLE|Handle to source object for subtract operation.|
|obj2|HANDLE|Handle to source object for subtract operation.|
|newSolid|HANDLE|Handle to resultant object from subtract operation.|

## Remarks
\_c\_ (2018.02.11):  obj1 = clipped, obj2 = clipper

Everything cuts the backmost object, which will be the 1st retrived using [FIn3D](FIn3D.md).

A solid subtraction has object type 84 and subtype 516. Mind, also other objects have type 84, such as Generic Solids (eventually generated using [ExtrudeAlongPath](ExtrudeAlongPath.md))

## Examples
```pascal
	ClosePoly;
	Poly(X-Length, Y-depth+Inset,X-depth+Inset+LeftLength, Y-RightLength-Length,2*(X+Length-depth+Inset+LeftLength)-Length, -2*(Y-RightLength)-Length,2*X-Length,- 2*(Y+Length-depth+Inset)-Length);
EndXtrd;
Cut := LNewObj;
Result := SubtractSolid(Circle,Cut,Temp);
BeginXtrd(pKick_Height+(HmTDH-pKick_Height)*kBottomDrawerPct, QD3DDelta +pKick_Height+(HmTDH-pKick_Height)*kBottomDrawerPct);
	Arc(X+inset-Length,Y+inset-Length,X-inset,Y-inset,0,360);
EndXtrd;
Circle := LNewObj;

		ELSE {Other cabinets}
			Rect(X1-kSlatSpace+I*SlatWidth,Y1,X1+kSlatSpace+I*SlatWidth,Y1-SHeight);
	END;
EndXtrd;
I := SubtractSolid(SlabHand,LNewObj,Grooved);
AttrReconfig(Grooved,parmHand);

resultcode:=AddSolid(hVault1,hVault2,hVaultComb);
resultcode:=SubtractSolid(hTower,hVaultComb,hCampi);
SetTextureRef(hCampi,-1,3);
```
```python
import vs

# Function SubtractSolid creates a new solid subtraction object from the
# referenced source objects.
obj1 = vs.FSActLayer()  # handle to the first selected object on the active layer
obj2 = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

resultN, newSolid = vs.SubtractSolid(obj1, obj2)
vs.Message('SubtractSolid returned: ' + str((resultN, newSolid)))
```
See also in tutorials: [06. Boolean Solids: Drill a Hole Through a Block](ai%20examples/06_BooleanSolids.md)

## Version
Availability: from MiniCAD 7.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
