# GetDLComponentPenStyles

## Description
Gets the left and right side pen styles of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLComponentPenStyles(
				index             : INTEGER;
				VAR penStyleLeft  : INTEGER;
				VAR penStyleRight : INTEGER): BOOLEAN;
```

```python
def vs.GetDLComponentPenStyles(index):
    return (BOOLEAN, penStyleLeft, penStyleRight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|penStyleLeft|INTEGER|Returns the pen style of the component's left line.  Positive values for patters, negative values for dash styles.|
|penStyleRight|INTEGER|Returns the pen style of the component's right line.  Positive values for patterns, negative values for dash styles.|

## Remarks
CJG 6-27-06

## See Also
VS Functions:
[SetDLComponentPenStyles](SetDLComponentPenStyles.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
