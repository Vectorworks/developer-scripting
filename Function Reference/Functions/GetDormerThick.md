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

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
