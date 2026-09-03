# vsoSetClosureGap

## Description
Provide a Gap for Left, Right, Top, Bottom edge of Wall Closure

```pascal
PROCEDURE vsoSetClosureGap(
				leftGapValue   : REAL;
				rightGapValue  : REAL;
				topGapValue    : REAL;
				bottomGapValue : REAL);
```

```python
def vs.vsoSetClosureGap(leftGapValue, rightGapValue, topGapValue, bottomGapValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|leftGapValue|REAL|   |
|rightGapValue|REAL|   |
|topGapValue|REAL|   |
|bottomGapValue|REAL|   |

## Examples
```pascal
vsoSetClosureGap(1.0, 2.0, 0.5, 1.5);
```
```python
import vs

# Provide a Gap for Left, Right, Top, Bottom edge of Wall Closure.
leftGapValue = 1.0
rightGapValue = 2.0
topGapValue = 0.5
bottomGapValue = 3.0

vs.vsoSetClosureGap(leftGapValue, rightGapValue, topGapValue, bottomGapValue)
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
