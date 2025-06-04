# GetGradientSpotPosition

## Description
Gets the spot position of the specified gradient segment.

```pascal
PROCEDURE GetGradientSpotPosition(
				gradient     : HANDLE;
				segmentIndex : INTEGER;
				VAR position : REAL);
```

```python
def vs.GetGradientSpotPosition(gradient, segmentIndex):
    return position
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment from which to get the data.|(segment indexes begin with 1)|
|position|REAL|Position of the segment's color spot relative to left-most point of the gradient.|(position &gt;= 0.0 and position &lt;= 1.0)|

## Examples
#### VectorScript ####
```pascal
GetGradientSpotPosition(gradientHandle, 4, spotPosition);
```
#### Python ####
```python
spotPosition = vs.GetGradientSpotPosition(gradientHandle, 4)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
