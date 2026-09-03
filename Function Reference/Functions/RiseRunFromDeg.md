# RiseRunFromDeg

## Description
Converts slope from degrees to rise-over-run string.

```pascal
FUNCTION RiseRunFromDeg(fSlopeDeg : REAL): STRING;
```

```python
def vs.RiseRunFromDeg(fSlopeDeg):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fSlopeDeg|REAL|   |

## Examples
```pascal
BEGIN
gValAng := tmpReal;
SetItemText(dialogID, kSwapRiseOverRun, RiseRunFromDeg( gValAng ));
SetItemText(dialogID, kSwapPercent, PercStrFromDeg( gValAng ));
END
```
```python
import vs

# Converts slope from degrees to rise-over-run string.
fSlopeDeg = 1.0

text = vs.RiseRunFromDeg(fSlopeDeg)
vs.Message('RiseRunFromDeg returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2016

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
