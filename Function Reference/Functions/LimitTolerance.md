# LimitTolerance

## Description
Procedure LimitTolerance is used with dimensioning procedures to define a tolerance for the most recently created dimension object.

```pascal
PROCEDURE LimitTolerance(
				showVal     : BOOLEAN;
				boxText     : BOOLEAN;
				leader      : STRING;
				trailer     : STRING;
				lowDistance : REAL;
				hiDistance  : REAL);
```

```python
def vs.LimitTolerance(showVal, boxText, leader, trailer, lowDistance, hiDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|showVal|BOOLEAN|Dimension text display flag.|
|boxText|BOOLEAN|Boxed text display flag.|
|leader|STRING|Dimension leader text string.|
|trailer|STRING|Dimension trailer text string.|
|lowDistance|REAL|Tolerance value text string.|
|hiDistance|REAL|Tolerance value text string.|

## Examples
==== VectorScript ====
```pascal
LinearDim(-2&quot;,2&quot;,1&quot;,2&quot;,-3&quot;,0,771,771,0.75);
LimitTolerance(TRUE,FALSE,'','',-1&quot;,1&quot;);
```
==== Python ====
```python

```

## Version
Availability: from MiniCAD4.0

## Category
* [Dimensions](../Categories/Dimensions.md)
