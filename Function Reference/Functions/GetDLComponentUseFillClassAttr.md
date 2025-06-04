# GetDLComponentUseFillClassAttr

## Description
Gets the use fill class attributes flag of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLComponentUseFillClassAttr(
				index            : INTEGER;
				VAR useClassAttr : BOOLEAN): BOOLEAN;
```

```python
def vs.GetDLComponentUseFillClassAttr(index):
    return (BOOLEAN, useClassAttr)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|useClassAttr|BOOLEAN|Returns whether or not the component is using class attributes for its fill.|

## Remarks
CJG 3-23-07

## See Also
VS Functions:
[SetDLComponentUseFillClassAttr](SetDLComponentUseFillClassAttr.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
