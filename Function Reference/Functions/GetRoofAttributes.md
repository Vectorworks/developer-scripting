# GetRoofAttributes

## Description
Function GetRoofAttributes returns the attributes of the referenced roof object.

**Table - Roof Miter Styles**

| Miter Style | Constant |
|-------------|----------|
| Vertical    | 1        |
| Horizontal  | 2        |
| Double      | 3        |
| Square      | 4        |

```pascal
FUNCTION GetRoofAttributes(
				theRoof          : HANDLE;
				VAR genGableWall : BOOLEAN;
				VAR bearingInset : REAL;
				VAR roofThick    : REAL;
				VAR miterType    : INTEGER;
				VAR vertMiter    : REAL): BOOLEAN;
```

```python
def vs.GetRoofAttributes(theRoof):
    return (BOOLEAN, genGableWall, bearingInset, roofThick, miterType, vertMiter)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theRoof|HANDLE|Handle to roof object.|
|genGableWall|BOOLEAN|Returns gable wall generation state.|
|bearingInset|REAL|Returns bearing inset dimension.|
|roofThick|REAL|Returns roof thickness.|
|miterType|INTEGER|Returns miter style.|
|vertMiter|REAL|Returns vertical miter dimension.|

## Remarks
genGableWall: Set to true to have a wall created at gable ends of the roof.  Otherwise no object will be inserted.
bearingInset  is where the weight of the roof rests on the wall.  This is an inset from the defining edge of the roof plan.
miterType: Specify 1 for a vertical miter, 2 for horizontal miter, 3 for a double miter cut, and 4 for a square end miter cut.
vertMiter: This is used only with the double miter type; it specifies the vertical length of the miter cut.



slabKind := GetObjectVariableInt(h, 172); {1 = roof, 2 = floor, 3 = column}

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
var
theRoof :HANDLE;
genGableWall :BOOLEAN; 
bearingInset, roofThick :REAL; 
miterType :INTEGER; 
vertMiter :REAL;
begin
theRoof := FSActLayer;
IF GetRoofAttributes(theRoof, genGableWall, bearingInset, roofThick, miterType, vertMiter)
THEN Message(genGableWall, ' ', bearingInset, ' ', roofThick, ' ', miterType, ' ', vertMiter);
end;
RUN(Example);
```
#### Python ####
```python
def Example():
	theRoof = vs.FSActLayer()
	hasAttr, genGableWall, bearingInset, roofThick, miterType, vertMiter = vs.GetRoofAttributes(theRoof)
	if hasAttr:
		vs.Message(genGableWall, ' ', bearingInset, ' ', roofThick, ' ', miterType, ' ', vertMiter)
Example()
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
