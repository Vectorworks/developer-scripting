# SetDLComponentFill

## Description
Sets the fill of the component at index in the Double Line Preferences.

```pascal
FUNCTION SetDLComponentFill(
				index : INTEGER;
				fill  : LONGINT): BOOLEAN;
```

```python
def vs.SetDLComponentFill(index, fill):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|fill|LONGINT|The fill of the component.  Positive values for patterns, negative object indexes for hatches.|

## Remarks
CJG 6-27-06

## See Also
VS Functions:
[GetDLComponentFill](GetDLComponentFill.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
