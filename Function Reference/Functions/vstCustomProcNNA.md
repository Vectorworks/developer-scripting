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

## Examples
```pascal
BEGIN
	VSTSetCustomProc('VSTCustomProcNNA');
	modeValue := 2;
	radius := 1;
	result := VSTCustomProcNNA (kParameterizeProc, unused, modeValue, radius, spacing);
{
message (' inMode1 = ',inMode1,'    inMode2 = ',inMode2,'    result = ',result);
}
```
```python
import vs

# For internal use only.
inEvent = 1
inMode = 0
inDiameter = 2.0
inSpacing = 1.0

ok, outEvtResult = vs.vstCustomProcNNA(inEvent, inMode, inDiameter, inSpacing)
vs.Message('vstCustomProcNNA returned: ' + str((ok, outEvtResult)))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
