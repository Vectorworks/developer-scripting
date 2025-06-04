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

## See Also
VS Functions:
[GetDLComponentPenColors](GetDLComponentPenColors.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
