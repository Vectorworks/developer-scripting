# DoubleTolerance

## Description
Procedure DoubleTolerance is used with dimensioning procedures to define a tolerance for the most recently created dimension.

```pascal
PROCEDURE DoubleTolerance(
				showVal     : BOOLEAN;
				boxText     : BOOLEAN;
				leader      : STRING;
				trailer     : STRING;
				topDistance : REAL;
				botDistance : REAL);
```

```python
def vs.DoubleTolerance(showVal, boxText, leader, trailer, topDistance, botDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|showVal|BOOLEAN|Dimension text display flag.|
|boxText|BOOLEAN|Boxed text display flag.|
|leader|STRING|Dimension leader text string.|
|trailer|STRING|Dimension trailer text string.|
|topDistance|REAL|Tolerance value text string.|
|botDistance|REAL|Tolerance value text string.|

## Examples
==== VectorScript ====
```pascal
LinearDim(-2",2",1",2",-3",0,771,771,0.75);
DoubleTolerance(True,False,'est. ','',1/16",1/16");
{defines a dimension with a double tolerance}
```
==== Python ====
```python
vs.LinearDim(-2,2,1,2,-3,0,771,771,0.75)
vs.DoubleTolerance(True,False,'est. ','',1/16,1/16)
```

## Version
Availability: from MiniCAD4.0

## Category
* [Dimensions](../Categories/Dimensions.md)
