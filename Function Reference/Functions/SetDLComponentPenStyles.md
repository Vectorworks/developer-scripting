# SetDLComponentPenStyles

## Description
Sets the left and right pen styles for the component at index in the Double Line Preferences.

```pascal
FUNCTION SetDLComponentPenStyles(
				index         : INTEGER;
				penStyleLeft  : INTEGER;
				penStyleRight : INTEGER): BOOLEAN;
```

```python
def vs.SetDLComponentPenStyles(index, penStyleLeft, penStyleRight):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|penStyleLeft|INTEGER|The pen style of the component's left line.  Positive values for patterns, negative values for dash styles.|
|penStyleRight|INTEGER|The pen style of the component's right line.  Positive values for patterns, negative values for dash styles.|

## Remarks
CJG 6-27-06

## Examples
```pascal
resultOK := SetDLComponentPenStyles(1, 2, 3);
```
```python
import vs

# Sets the left and right pen styles for the component at index in the Double
# Line Preferences.
index = 1
penStyleLeft = 0
penStyleRight = 0

ok = vs.SetDLComponentPenStyles(index, penStyleLeft, penStyleRight)
if ok:
    vs.Message('SetDLComponentPenStyles succeeded')
else:
    vs.Message('SetDLComponentPenStyles failed')
```

## See Also
VS Functions:
[GetDLComponentPenStyles](GetDLComponentPenStyles.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
