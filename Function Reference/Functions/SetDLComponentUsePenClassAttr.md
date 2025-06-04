# SetDLComponentUsePenClassAttr

## Description
Sets the useclass attributes flags of the left and right side pens of the component at index in the Double Line Preferences.

```pascal
FUNCTION SetDLComponentUsePenClassAttr(
				index                : INTEGER;
				leftPenUseClassAttr  : BOOLEAN;
				rightPenUseClassAttr : BOOLEAN): BOOLEAN;
```

```python
def vs.SetDLComponentUsePenClassAttr(index, leftPenUseClassAttr, rightPenUseClassAttr):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|leftPenUseClassAttr|BOOLEAN|Whether or not the component will use class attributes for its left pen.|
|rightPenUseClassAttr|BOOLEAN|Whether or not the component will use class attributes for its right pen.|

## Remarks
CJG 3-23-07

## See Also
VS Functions:
[GetDLComponentUsePenClassAttr](GetDLComponentUsePenClassAttr.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
