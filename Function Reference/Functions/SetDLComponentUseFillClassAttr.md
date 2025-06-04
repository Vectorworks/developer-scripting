# SetDLComponentUseFillClassAttr

## Description
Sets the use fill class attributes flag of the component at index in the Double Line Preferences.

```pascal
FUNCTION SetDLComponentUseFillClassAttr(
				index        : INTEGER;
				useClassAttr : BOOLEAN): BOOLEAN;
```

```python
def vs.SetDLComponentUseFillClassAttr(index, useClassAttr):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|useClassAttr|BOOLEAN|Whether or not the component will use class attributes for its fill.|

## Remarks
CJG 3-23-07

## See Also
VS Functions:
[GetDLComponentUseFillClassAttr](GetDLComponentUseFillClassAttr.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
