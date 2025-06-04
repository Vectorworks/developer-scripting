# GetDLComponentWidth

## Description
Gets the width of the component at index in the Double Line Preferences.

```pascal
FUNCTION GetDLComponentWidth(
				index     : INTEGER;
				VAR width : REAL): BOOLEAN;
```

```python
def vs.GetDLComponentWidth(index):
    return (BOOLEAN, width)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|width|REAL|Returns the width of the component.|

## Remarks
CJG 6-27-06

## See Also
VS Functions:
[SetDLComponentWidth](SetDLComponentWidth.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
