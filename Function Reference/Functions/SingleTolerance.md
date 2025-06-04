# SingleTolerance

## Description
Procedure SingleTolerance is used with dimensioning procedures to define a tolerance for the most recently created dimension.

```pascal
PROCEDURE SingleTolerance(
				showVal     : BOOLEAN;
				boxText     : BOOLEAN;
				leader      : STRING;
				trailer     : STRING;
				limDistance : REAL);
```

```python
def vs.SingleTolerance(showVal, boxText, leader, trailer, limDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|showVal|BOOLEAN|Dimension text display flag.|
|boxText|BOOLEAN|Boxed text display flag.|
|leader|STRING|Dimension leader text string.|
|trailer|STRING|Dimension trailer text string.|
|limDistance|REAL|Limit tolerance string.|

## Examples
==== VectorScript ====
```pascal
LinearDim(-2&quot;,2&quot;,1&quot;,2&quot;,-3&quot;,0,771,770,0.75);
SingleTolerance(True,False,'approx. ','',1/16&quot;);
```
==== Python ====
```python

```

## Version
Availability: from MiniCAD4.0

## Category
* [Dimensions](../Categories/Dimensions.md)
