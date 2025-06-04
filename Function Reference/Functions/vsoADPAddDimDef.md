# vsoADPAddDimDef

## Description
Add a dimension definition data to the result for the Auto Dimension GetDimensionDefinitions (78) message sent to a Script object.

```pascal
PROCEDURE vsoADPAddDimDef(
				message   : LONGINT;
				startPt3  : REAL;
				endPt3    : REAL;
				dimOffset : INTEGER);
```

```python
def vs.vsoADPAddDimDef(message, startPt3, endPt3, dimOffset):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|startPt3|REAL|   |
|endPt3|REAL|   |
|dimOffset|INTEGER|   |

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
