# Symbol

## Description
Procedure Symbol places a symbol in the document at the specified coordinate location.

```pascal
PROCEDURE Symbol(
				symbolName    : STRING;
				pX,pY         : REAL;
				rotationAngle : REAL);
```

```python
def vs.Symbol(symbolName, p, rotationAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symbolName|STRING|Name of symbol.|
|p|REAL|Coordinates of symbol insertion point.|
|rotationAngle|REAL|Rotation angle of symbol, in degrees.|

## Remarks
This doesn't work if [AngleVar](AngleVar.md) is turned on.

Seems to set the documents active symbol definition [CMP]

## Examples
```pascal
BEGIN
  Symbol(KnobName,X1+DoorWidth/2,Y1-DoorHeight/2,90);
  GetSymLoc3D(lNewObj,xctr,yctr,zctr);
  SET3DRot(lNewObj, 0, 90, 0, xctr,yctr,zctr);
END;

BEGIN
	VSave ('__SeatingLayoutTempView');
	SetView (0, 0, 0, 0, 0, 0);
	Symbol(symName, 0, 0, 0);
	h := LNewObj;
	GetBBox(h, p1x, p1y, p2x, p2y);
	gRowSpacing := Str2Num(GetRField(objHand, kSeatingObjectName, 'RowSpacing'));
	gSeatSpacing := Str2Num(GetRField(objHand, kSeatingObjectName, 'SeatSpacing'));

		IF SelectSymbolDialog('', '','FlowChartSym', 0, '', '', symName) = 1 THEN SetRField(objHand, objName, 'Symbol Name', symName);
	END;
	IF symName = ''
		THEN Rect(-.5 * Scale, .375 * Scale, .5 * Scale, -.375 * Scale)
		ELSE Symbol(symName, 0, 0, 0);
	textCenterY := 0;
END ELSE IF pConfig = 'Terminator' THEN BEGIN
	BeginPoly;
		ArcTo(-.5 * Scale, .1875 * Scale, 0 * Scale);
```
```python
import vs

# Procedure Symbol places a symbol in the document at the specified
# coordinate location.
symbolName = 'MySymbol'
p = (0, 0)
rotationAngle = 45.0

vs.Symbol(symbolName, p, rotationAngle)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
