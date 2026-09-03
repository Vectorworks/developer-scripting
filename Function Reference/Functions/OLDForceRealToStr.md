# OLDForceRealToStr

## Description
Converts force real value to string and returns TRUE on success.

```pascal
FUNCTION OLDForceRealToStr(forceValue : REAL): STRING;
```

```python
def vs.OLDForceRealToStr(forceValue):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|forceValue|REAL|   |

## Examples
```pascal
	ReactionForceVal := Str2Num( GetRField( HoistHdl, PIOName, 'ReactionForce' ) );
	ReactionForceStr := OLDForceRealToStr( ReactionForceVal );
	SetRField( HoistHdl, PIOName, 'ReactionForceStr', ReactionForceStr );
END;
```
```python
import vs

# Converts force real value to string and returns TRUE on success.
forceValue = 1.0

text = vs.OLDForceRealToStr(forceValue)
vs.Message('OLDForceRealToStr returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
