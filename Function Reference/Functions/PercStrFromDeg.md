# PercStrFromDeg

## Description
Converts slope from degrees to percent string.

```pascal
FUNCTION PercStrFromDeg(fSlopeDeg : REAL): STRING;
```

```python
def vs.PercStrFromDeg(fSlopeDeg):
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

# Converts slope from degrees to percent string.
fSlopeDeg = 1.0

text = vs.PercStrFromDeg(fSlopeDeg)
vs.Message('PercStrFromDeg returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2016

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
