# vstCustomProcNNA

## Description
For internal use only.

```pascal
FUNCTION vstCustomProcNNA(
				inEvent          : LONGINT;
				VAR outEvtResult : LONGINT;
				inMode           : LONGINT;
				inDiameter       : REAL;
				inSpacing        : REAL):BOOLEAN;
```

```python
def vs.vstCustomProcNNA(inEvent, inMode, inDiameter, inSpacing):
    return (BOOLEAN, outEvtResult)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inEvent|LONGINT|   |
|outEvtResult|LONGINT|Output parameter.|
|inMode|LONGINT|   |
|inDiameter|REAL|   |
|inSpacing|REAL|   |

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
