# DoubleFixedTolerance

## Description
Procedure DoubleFixedTolerance is used with dimensioning procedures to define a tolerance for the most recently created dimension object.

```pascal
PROCEDURE DoubleFixedTolerance(
				showVal : BOOLEAN;
				boxText : BOOLEAN;
				leader  : STRING;
				trailer : STRING;
				topStr  : STRING;
				botStr  : STRING);
```

```python
def vs.DoubleFixedTolerance(showVal, boxText, leader, trailer, topStr, botStr):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|showVal|BOOLEAN|Dimension text display flag.|
|boxText|BOOLEAN|Boxed text display flag.|
|leader|STRING|Dimension leader text string.|
|trailer|STRING|Dimension trailer text string.|
|topStr|STRING|Tolerance value text string.|
|botStr|STRING|Tolerance value text string.|

## Examples
==== VectorScript ====
```pascal
LinearDim(-2",2",1",2",-3",0,771,771,0.75);
DoubleFixedTolerance(TRUE,FALSE,'','','yes','no');
{defines a dimension with a double fixed tolerance}
```
==== Python ====
```python
vs.LinearDim(-2,2,1,2,-3,0,771,771,0.75)
vs.DoubleFixedTolerance(True,False,'','','yes','no')
#{defines a dimension with a double fixed tolerance}
```

## Version
Availability: from MiniCAD4.0

## Category
* [Dimensions](../Categories/Dimensions.md)
