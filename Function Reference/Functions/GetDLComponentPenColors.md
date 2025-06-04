# GetDLComponentPenColors

## Description
Gets the fore and back colors of the left and right side pens of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLComponentPenColors(
				index                 : INTEGER;
				VAR leftPenForeColor  : INTEGER;
				VAR leftPenBackColor  : INTEGER;
				VAR rightPenForeColor : INTEGER;
				VAR rightPenBackColor : INTEGER): BOOLEAN;
```

```python
def vs.GetDLComponentPenColors(index):
    return (BOOLEAN, leftPenForeColor, leftPenBackColor, rightPenForeColor, rightPenBackColor)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|leftPenForeColor|INTEGER|Returns the fore color of the left pen.|
|leftPenBackColor|INTEGER|Returns the back color of the left pen.|
|rightPenForeColor|INTEGER|Returns the fore color of the right pen.|
|rightPenBackColor|INTEGER|Resturns the back color of the right pen.|

## Remarks
CJG 3-23-07

## See Also
VS Functions:
[SetDLComponentPenColors](SetDLComponentPenColors.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
