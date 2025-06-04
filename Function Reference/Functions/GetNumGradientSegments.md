# GetNumGradientSegments

## Description
Gets the number of segments in the gradient.

```pascal
FUNCTION GetNumGradientSegments(gradient : HANDLE): INTEGER;
```

```python
def vs.GetNumGradientSegments(gradient):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|The gradient from which to get the number of segments.|

## Remarks
Note: a gradient must always have at least 2 segments.

This also returns the number of levels in a hatch definition, like [{VS:GetObjectVariableInt]](HatchDefH, 660).

## Examples
==== VectorScript ====
```pascal
numSegments := GetNumGradientSegments(gradientHandle);
```
==== Python ====
```python
numSegments = vs.GetNumGradientSegments(gradientHandle)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
