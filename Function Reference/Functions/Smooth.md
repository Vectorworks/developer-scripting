# Smooth

## Description
Procedure Smooth sets the smoothing type of newly created polyline or polygon objects.

{| class="wikitable_c"
|+ Table - Smoothing Types
! Smooth Type !! Constant
|-
| None
| 0
|-
| Bezier
| 1
|-
| Cubic
| 2
|-
| Arc
| 3
|}

```pascal
PROCEDURE Smooth(smoothType : INTEGER);
```

```python
def vs.Smooth(smoothType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|smoothType|INTEGER|Smoothing style.|

## Examples
#### VectorScript ####
```pascal
Smooth(2);
Poly(0, 0, -0.5, 1, 0.5, 2);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
