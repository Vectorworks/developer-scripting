# GetDormerThick

## Description
Procedure GetDormerThick returns dormer roof and wall thicknesses for the referenced roof.

```pascal
PROCEDURE GetDormerThick(
				roofObject    : HANDLE;
				VAR wallThick : REAL;
				VAR roofThick : REAL);
```

```python
def vs.GetDormerThick(roofObject):
    return (wallThick, roofThick)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to dormer.|
|wallThick|REAL|Returns dormer wall thickness.|
|roofThick|REAL|Returns dormer roof thickness.|

## Examples
```pascal
GetDormerThick(roofObject, 1.0, 2.0);
```
```python
import vs

# Procedure GetDormerThick returns dormer roof and wall thicknesses for the
# referenced roof.
roofObject = vs.FSActLayer()  # handle to the first selected object on the active layer

wallThick, roofThick = vs.GetDormerThick(roofObject)
vs.Message('GetDormerThick returned: ' + str((wallThick, roofThick)))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
