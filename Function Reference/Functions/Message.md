# Message

## Description
Procedure Message displays a floating message palette onscreen. Parameters z1 thru zN specify the values to be displayed in the palette. Parameters can be any supported data type or variables.

If Message is called and the palette is already displayed, the value in the palette will be replaced by the new information.

```pascal
PROCEDURE Message(z : ANY);
```

```python
def vs.Message(z):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|z|ANY|   |

## Examples
#### VectorScript ####
```pascal
Message('Hello, world');

Message('The Number of objects was :',theNumber);
{displays a string using the variable value}
```
#### Python ####
```python

```

```pascal
		SetTextVerticalAlign(ObjectHand,3);
		ResetObject(ObjectHand);
		CreateSeatLayoutObj := ObjectHand;
	END
	ELSE Message(GetPluginString(3015), ' [', Poly_H, ']');
END;

	9: MonthStartDay:=  243;
	10: MonthStartDay:=  273;
	11: MonthStartDay:=  304;
	12: MonthStartDay:=  334;
	OTHERWISE Message(kBadValue);
END;

Message(GetPlugInString(3013));
SetCursor(lgCrossC);
GetPt(x, y);
SetCursor(arrowC);
ClrMessage;
```
```python
vs.Message( msg )

if vs.GetTypeN(h) == 94:
	vs.NameClass(className)
else:
	vs.Message( vs.GetResourceString(11000, 10), className, vs.GetResourceString(11000, 11) )
	#Cannot create class; an object of that name already exists.}
```
See also in tutorials: [01. Draw a Room with Walls](ai%20examples/01_DrawRoomWithWalls.md), [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md), [03. Build a Curved Path with Mixed Vertex Types](ai%20examples/03_CurvedPolylinePath.md), [04. Extrude 2D Shapes into 3D Solids](ai%20examples/04_ExtrudeShapesTo3D.md)

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
