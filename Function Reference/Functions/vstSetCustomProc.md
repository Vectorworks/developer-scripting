# vstSetCustomProc

```pascal
PROCEDURE vstSetCustomProc(inRoutineName : STRING);
```

```python
def vs.vstSetCustomProc(inRoutineName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inRoutineName|STRING|   |

## Examples
```pascal
BEGIN
	VSTSetCustomProc('VSTCustomProcNNA');
	modeValue := 2;
	radius := 1;
	result := VSTCustomProcNNA (kParameterizeProc, unused, modeValue, radius, spacing);
{
```
```python
import vs

inRoutineName = 'Example'

vs.vstSetCustomProc(inRoutineName)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
