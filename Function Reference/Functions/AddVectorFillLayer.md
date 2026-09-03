# AddVectorFillLayer

## Description
Procedure AddVectorFillLayer is used to add layers to a vector fill definition. This procedure call should follow a call to BeginVectorFillN. 

The input parameters for a vector fill layer match the inputs from the right side of the VectorWorks hatch editor dialog.

A color table listing with associated index values can be found in the [Script Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#color-palette).

```pascal
PROCEDURE AddVectorFillLayer(
				xStart     : REAL;
				yStart     : REAL;
				xRepeat    : REAL;
				yRepeat    : REAL;
				xOffset    : REAL;
				yOffset    : REAL;
				dashFactor : REAL;
				lineWeight : INTEGER;
				colorIndex : INTEGER);
```

```python
def vs.AddVectorFillLayer(xStart, yStart, xRepeat, yRepeat, xOffset, yOffset, dashFactor, lineWeight, colorIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|xStart|REAL|X coordinate of fill origin.|
|yStart|REAL|Y coordinate of fill origin.|
|xRepeat|REAL|X coordinate of fill repeat origin.|
|yRepeat|REAL|Y coordinate of fill repeat origin.|
|xOffset|REAL|X coordinate of fill offset origin.|
|yOffset|REAL|Y coordinate of fill offset origin.|
|dashFactor|REAL|Dash factor of layer(percentage of fill line that is solid).|
|lineWeight|INTEGER|Line weight of layer, in mils.|
|colorIndex|INTEGER|Pen color of layer.|

## Remarks
Follows a call to BeginVectorFill. The input for the layer match the input from the right side of the hatch editor dialog.

## Examples
[AddHatchToResource](examples/AddHatchToResource.md)

```pascal
AddVectorFillLayer(0, 0,1, 1, 0.2, -0.2, 1, 1, 257);

BEGIN
	RGBTocolorIndex (kHtch1aR, kHtch1aG, kHtch1aB, colorIndexA);
	RGBTocolorIndex (kHtch1bR,kHtch1bG,kHtch1bB, colorIndexB);
	BEGINVectorFillN(LocalName,FALSE,FALSE,256);
		AddVectorFillLayer(2,0,7.5,12.990381057,7.5,-12.990381057,0.4,1,colorIndexA);
		AddVectorFillLayer(2,0,-7.5,12.990381057,-7.5,-12.990381057,0.4,1,colorIndexA);
		AddVectorFillLayer(2,0,2.22045e-016,25.980762114,7.5,-12.990381057,0.25,1,colorIndexB);
	EndVectorFill;
	objectHANDLE := GetObject(LocalName);
```
```python
import vs

# Procedure AddVectorFillLayer is used to add layers to a vector fill definition.
xStart = 1.0
yStart = 2.0
xRepeat = 0.5
yRepeat = 3.0
xOffset = 0.0
yOffset = 0.0
dashFactor = 1.0
lineWeight = 1
colorIndex = 1

vs.AddVectorFillLayer(xStart, yStart, xRepeat, yRepeat, xOffset, yOffset, dashFactor, lineWeight, colorIndex)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from MiniCAD7.0.1

## Category
* [Hatches @ Vector Fills](../Categories/Hatches%20-%20Vector%20Fills.md)
