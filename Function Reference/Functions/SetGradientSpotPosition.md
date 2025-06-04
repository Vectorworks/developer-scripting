# SetGradientSpotPosition

## Description
Sets the spot position of the specified gradient segment.

Note: you must use a variable, initialized to the segment index, to pass as a parameter. After the data has been set, this variable will contain the index of the segment, which may have changed because of the spot position specified.

```pascal
PROCEDURE SetGradientSpotPosition(
				gradient         : HANDLE;
				VAR segmentIndex : INTEGER;
				position         : REAL);
```

```python
def vs.SetGradientSpotPosition(gradient, segmentIndex, position):
    return segmentIndex
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment for which to set the data.|(segment indexes begin with 1)|
|position|REAL|Position of the segment's color spot relative to left-most point of the gradient.|(position &gt;= 0.0 and position &lt;= 1.0)|

## Examples
==== VectorScript ====
```pascal
SetGradientSpotPosition(gradientHandle, segmentIndex, 0.9);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
