# SetDLComponentPenColors

## Description
Sets the fore and back colors of the left and right side pens of the component at index in the Double Line Preferences.

```pascal
FUNCTION SetDLComponentPenColors(
				index             : INTEGER;
				leftPenForeColor  : INTEGER;
				leftPenBackColor  : INTEGER;
				rightPenForeColor : INTEGER;
				rightPenBackColor : INTEGER): BOOLEAN;
```

```python
def vs.SetDLComponentPenColors(index, leftPenForeColor, leftPenBackColor, rightPenForeColor, rightPenBackColor):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|leftPenForeColor|INTEGER|The fore color of the left pen.|
|leftPenBackColor|INTEGER|The back color of the left pen.|
|rightPenForeColor|INTEGER|The fore color of the right pen.|
|rightPenBackColor|INTEGER|The back color of the right pen.|

## Remarks
CJG 3-23-07

## Examples
```pascal
resultOK := SetDLComponentPenColors(1, 2, 3, 10, 5);
```
```python
import vs

# Sets the fore and back colors of the left and right side pens of the
# component at index in the Double Line Preferences.
index = 1
leftPenForeColor = 5
leftPenBackColor = 5
rightPenForeColor = 5
rightPenBackColor = 5

ok = vs.SetDLComponentPenColors(index, leftPenForeColor, leftPenBackColor, rightPenForeColor, rightPenBackColor)
if ok:
    vs.Message('SetDLComponentPenColors succeeded')
else:
    vs.Message('SetDLComponentPenColors failed')
```

## See Also
VS Functions:
[GetDLComponentPenColors](GetDLComponentPenColors.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
