# SetRoofAttributes

## Description
Function SetRoofAttributes sets the definition attributes of a roof object in a VectorWorks document. 

**Table - Roof Miter Styles**

| Miter Style | Constant |
|-------------|----------|
| Vertical    | 1        |
| Horizontal  | 2        |
| Double      | 3        |
| Square      | 4        |

```pascal
PROCEDURE SetRoofAttributes(
				roofObject           : HANDLE;
				genGableWall         : BOOLEAN;
				bearingInsetDistance : REAL;
				roofThickDistance    : REAL;
				miterType            : INTEGER;
				vertMiterDistance    : REAL);
```

```python
def vs.SetRoofAttributes(roofObject, genGableWall, bearingInsetDistance, roofThickDistance, miterType, vertMiterDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof .|
|genGableWall|BOOLEAN|Sets gable roof generation mode.|
|bearingInsetDistance|REAL|Sets bearing inset distance.|
|roofThickDistance|REAL|Sets roof thickness.|
|miterType|INTEGER|Sets miter style.|
|vertMiterDistance|REAL|Specifies vertical miter dimension.|

## Remarks
genGableWall: Set to true to have a wall created at gable ends of the roof.  Otherwise no object will be inserted.
bearingInset  is where the weight of the roof rests on the wall.  This is an inset from the defining edge of the roof plan.
miterType:  Specify 1 for a vertical miter, 2 for horizontal miter, 3 for a double miter cut, and 4 for a square end miter cut.  vertMiter: This is used only with the double miter type; it specifies the vertical length of the miter cut.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
thickness :REAL;
str	:STRING;

PROCEDURE SetIt(h :HANDLE);
BEGIN
IF GetObjectVariableInt(h, 172) = 1 THEN 
SetObjectVariableReal(h, 170, thickness * 25.4);
END;

PROCEDURE FindRoofFaces(h :HANDLE);
VAR
temp_h :HANDLE;
roofObject :HANDLE; 
genGableWall :BOOLEAN; 
bearingInsetDistance, roofThickDistance :REAL; 
miterType :INTEGER; 
vertMiterDistance :REAL;
BEGIN
IF GetType(h) = 71 THEN SetIt(h) ELSE
IF GetRoofAttributes(h, genGableWall, bearingInsetDistance, roofThickDistance, miterType, vertMiterDistance) THEN
SetRoofAttributes(h, genGableWall, bearingInsetDistance, thickness, miterType, vertMiterDistance);
END;

BEGIN
thickness := RealDialog('Enter desired thickness', '10');
str := Concat('((T=71) | (T=83)) &amp; (L=''', GetLName(ActLayer), ''')');
ForEachObject(FindRoofFaces, str);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
