# GetDLComponentUsePenClassAttr

## Description
Gets the useclass attributes flags of the left and right side pens of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLComponentUsePenClassAttr(
				index                    : INTEGER;
				VAR leftPenUseClassAttr  : BOOLEAN;
				VAR rightPenUseClassAttr : BOOLEAN): BOOLEAN;
```

```python
def vs.GetDLComponentUsePenClassAttr(index):
    return (BOOLEAN, leftPenUseClassAttr, rightPenUseClassAttr)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|leftPenUseClassAttr|BOOLEAN|Returns whether or not the component is using class attributes for its left pen.|
|rightPenUseClassAttr|BOOLEAN|Returns whether or not the component is using class attributes for right pen.|

## Remarks
CJG 3-23-07

## See Also
VS Functions:
[SetDLComponentUsePenClassAttr](SetDLComponentUsePenClassAttr.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
