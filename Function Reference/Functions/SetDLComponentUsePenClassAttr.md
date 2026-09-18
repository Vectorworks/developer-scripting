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

## Examples
```pascal
resultOK := SetDLComponentUsePenClassAttr(1, TRUE, FALSE);
```
```python
import vs

# Sets the useclass attributes flags of the left and right side pens of the
# component at index in the Double Line Preferences.
index = 1
leftPenUseClassAttr = True
rightPenUseClassAttr = True

ok = vs.SetDLComponentUsePenClassAttr(index, leftPenUseClassAttr, rightPenUseClassAttr)
if ok:
    vs.Message('SetDLComponentUsePenClassAttr succeeded')
else:
    vs.Message('SetDLComponentUsePenClassAttr failed')
```

## See Also
VS Functions:
[GetDLComponentUsePenClassAttr](GetDLComponentUsePenClassAttr.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
