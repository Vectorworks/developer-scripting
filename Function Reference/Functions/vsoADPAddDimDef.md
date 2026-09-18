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

## Examples
```pascal
vsoADPAddDimDef(1, 1.0, 2.0, 2);
```
```python
import vs

# Add a dimension definition data to the result for the Auto Dimension
# GetDimensionDefinitions (78) message sent to a Script object.
message = 'Hello Vectorworks'
startPt3 = 1.0
endPt3 = 2.0
dimOffset = 1

vs.vsoADPAddDimDef(message, startPt3, endPt3, dimOffset)
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Events](../Categories/Object%20Events.md)
