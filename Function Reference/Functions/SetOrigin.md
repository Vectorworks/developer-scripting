# SetOrigin

## Description
Shifts the position of the document origin. The function does not modify the relative 
positions of objects in the document; the coordinate locations of objects, however, 
will change when the origin location is modified.

```pascal
PROCEDURE SetOrigin(
				x : REAL;
				y : REAL);
```

```python
def vs.SetOrigin(x, y):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x|REAL|X-offset from current origin.|
|y|REAL|Y-offset from current origin.|

## Remarks
The difference between this and [SetOriginAbsolute](SetOriginAbsolute.md) is that this call *shifts* the origin the specified amount, where [SetOriginAbsolute](SetOriginAbsolute.md) sets the origin to the specified values.

## Examples
#### VectorScript ####
```pascal
Rect(0,0,1,1);
SetOrigin(1,1);

{ Creates a rectangle with the bottom left point at coordinates (0,0), then moves the origin so that the top right point of the rectangle has coordinates (0,0). }
```
#### Python ####
```python

```

```pascal
IF ((GetObject(concat(SDName, kDash, num2str(0, Scalefactor))) = NIL)&(gettype(GetObject(SDName)) = 16)) THEN BEGIN
	GetOrigin(xO, yO);
	SetOrigin(-xO, -yO);
	numSymDefs := 0;
	H := GetObject(SDName);
	factor := ScaleFactor;
	IF ((H <> NIL) & (gettype(H)=16)) THEN BEGIN

GetOrigin(userOriginX, userOriginY);
SetOrigin(-userOriginX, -userOriginY);

BEGIN
PushAttrs;
GetOrigin(xOrig,yOrig);
SetOrigin(-xOrig,-yOrig);
lowestPoint := kBiggestReal;
higestPoint := -kBiggestReal;
MaxRight := -kBiggestReal;
MinLeft := kBiggestReal;
```
```python
vs.SetOrigin(0, 0)
```

## See Also
VS Functions:
[SetOriginAbsolute](SetOriginAbsolute.md)

## Version
Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
