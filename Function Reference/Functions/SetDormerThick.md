# SetDormerThick

## Description
Procedure SetDormerThick sets dormer roof and wall thicknesses for the referenced roof.

```pascal
PROCEDURE SetDormerThick(
				roofObject        : HANDLE;
				wallThickDistance : REAL;
				roofThickDistance : REAL);
```

```python
def vs.SetDormerThick(roofObject, wallThickDistance, roofThickDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|wallThickDistance|REAL|Wall thickness of dormer.|
|roofThickDistance|REAL|Roof thickness of dormer.|

## Examples
[CreateRoofOb](examples/CreateRoofObj.md)

```pascal
SetDormerThick(roofObject, 1.0, 2.0);
```
```python
import vs

# Procedure SetDormerThick sets dormer roof and wall thicknesses for the
# referenced roof.
roofObject = vs.FSActLayer()  # handle to the first selected object on the active layer
wallThickDistance = 0.1
roofThickDistance = 0.1

vs.SetDormerThick(roofObject, wallThickDistance, roofThickDistance)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
