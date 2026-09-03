# HPerim

## Description
Function HPerim returns the perimeter of the referenced object.

```pascal
FUNCTION HPerim(h : HANDLE): REAL;
```

```python
def vs.HPerim(h):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
([[User:Orso.b.schmid|Orso]], 2011 Jan. 27): HPerim is affected by the application preference "2D Conversion Resolution" (PrefInt 55): the function will output faulty values on polylines with curved vertexes, if this preference is set to anything but "Very high" (512). It is advisable to set this preferences to 512 before using HPerim and restore the user value at end of script. (tested VW 2010 and 2011).

## Examples
```pascal
BEGIN
	GetArc(arcHandle, theAngle, theta);
  	HCenter(arcHandle, centerPt[1], centerPt[2]);
	theRadius := HPerim(arcHandle) / Deg2Rad(theta);
	theArcLength := (PI * theRadius * theta) / 180;
	chord := Sin(Deg2Rad(Abs(theta/2))) * theRadius * 2;
	T := theRadius * Tan(Deg2Rad(theta/2));
END;

r := HPerim (ObjH) / Deg2Rad (theta2);
x := x0 + r * Cos (Deg2Rad (theta1));
y := y0 + r * Sin (Deg2Rad (theta1));

		x1 := x2;
		y1 := y2;
	END;
	Perim := Perim + Distance (x1, y1, x0, y0);
	ClosedPoly := Num2Str (6, Perim) = Num2Str (6, HPerim (hPoly));
END;
```
```python
import vs

# Function HPerim returns the perimeter of the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.HPerim(h)
vs.Message('HPerim returned: ' + str(value))
```

## Version
Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
