# SetDLComponentFillColors

## Description
Sets the fore and back fill colors of the component at index in the Double Line Preferences.

```pascal
FUNCTION SetDLComponentFillColors(
				index         : INTEGER;
				fillForeColor : INTEGER;
				fillBackColor : INTEGER): BOOLEAN;
```

```python
def vs.SetDLComponentFillColors(index, fillForeColor, fillBackColor):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|fillForeColor|INTEGER|The fore color of the fill.|
|fillBackColor|INTEGER|The back color of the fill.|

## Remarks
CJG 3-23-07

## Examples
```pascal
resultOK := SetDLComponentFillColors(1, 2, 3);
```
```python
import vs

# Sets the fore and back fill colors of the component at index in the Double
# Line Preferences.
index = 1
fillForeColor = 5
fillBackColor = 5

ok = vs.SetDLComponentFillColors(index, fillForeColor, fillBackColor)
if ok:
    vs.Message('SetDLComponentFillColors succeeded')
else:
    vs.Message('SetDLComponentFillColors failed')
```

## See Also
VS Functions:
[GetDLComponentFillColors](GetDLComponentFillColors.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
