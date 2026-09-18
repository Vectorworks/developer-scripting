# SetDLComponentWidth

## Description
Sets the width of the nth component of the Double Line Preferences, where n is equal to index.

```pascal
FUNCTION SetDLComponentWidth(
				index         : INTEGER;
				widthDistance : REAL): BOOLEAN;
```

```python
def vs.SetDLComponentWidth(index, widthDistance):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|The index of the component.|
|widthDistance|REAL|The width of the component.|

## Remarks
CJG 6-27-06

## Examples
```pascal
resultOK := SetDLComponentWidth(1, 1.0);
```
```python
import vs

# Sets the width of the nth component of the Double Line Preferences, where n
# is equal to index.
index = 1
widthDistance = 2.0

ok = vs.SetDLComponentWidth(index, widthDistance)
if ok:
    vs.Message('SetDLComponentWidth succeeded')
else:
    vs.Message('SetDLComponentWidth failed')
```

## See Also
VS Functions:
[GetDLComponentWidth](GetDLComponentWidth.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
