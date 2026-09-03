# DegFromStr

## Description
Converts slope from string format to degrees.

```pascal
FUNCTION DegFromStr(
				fSlopeDef   : STRING;
				fSlopeValue : STRING;
				VAR fAngle  : REAL): BOOLEAN;
```

```python
def vs.DegFromStr(fSlopeDef, fSlopeValue):
    return (BOOLEAN, fAngle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fSlopeDef|STRING|   |
|fSlopeValue|STRING|   |
|fAngle|REAL|   |

## Examples
```pascal
BEGIN
GetItemText(dialogID, kSwapRiseOverRun, tmpStr);
IF NOT DegFromStr('RiseRun', tmpStr, tmpReal) THEN
	BEGIN
	InvalidValue(dialogID, kSwapRiseOverRun, item, getpluginstring(5013));
	exitProc := TRUE;
	END
```
```python
import vs

# Converts slope from string format to degrees.
fSlopeDef = 'Example'
fSlopeValue = 'Example'

ok, fAngle = vs.DegFromStr(fSlopeDef, fSlopeValue)
vs.Message('DegFromStr returned: ' + str((ok, fAngle)))
```

## Version
Availability: from Vectorworks 2016

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
