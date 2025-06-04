# GetDLComponentFill

## Description
Gets the fill of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLComponentFill(
				index    : INTEGER;
				VAR fill : LONGINT): BOOLEAN;
```

```python
def vs.GetDLComponentFill(index):
    return (BOOLEAN, fill)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|fill|LONGINT|Returns the fill of the component.  Positive values for patterns, negative ref numbers for hatches.|

## Remarks
CJG 6-27-06

## See Also
VS Functions:
[SetDLComponentFill](SetDLComponentFill.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
