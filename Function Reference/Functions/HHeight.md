# HHeight

## Description
Function HHeight returns the height of the referenced object.

```pascal
FUNCTION HHeight(h : HANDLE): REAL;
```

```python
def vs.HHeight(h):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Observed in 2021: Despite the OIP Width and Height fields flipping values when an object such as a rectangle is rotated 90/-90 degrees, vs.HWidth and vs.HHeight will always return the initial width and height values of the unrotated object, which can lead to unexpected values being returned in some instances. Unsure if this would be considered a bug or a feature...? -AMH (2021.06.26)

## Version
Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
