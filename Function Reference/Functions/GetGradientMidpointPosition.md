# GetGradientMidpointPosition

## Description
Gets the midpoint position of the specified gradient segment.

```pascal
PROCEDURE GetGradientMidpointPosition(
				gradient     : HANDLE;
				segmentIndex : INTEGER;
				VAR position : REAL);
```

```python
def vs.GetGradientMidpointPosition(gradient, segmentIndex):
    return position
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment from which to get the data.|(segment indexes begin with 1)|
|position|REAL|Position of the segment's midpoint relatvie to color spot immediately to left.|(position &gt;= 0.0 and position &lt;= 1.0)|

## Examples
#### VectorScript ####
```pascal
GetGradientMidpointPosition(gradientHandle, 4, midpointPosition);
```
#### Python ####
```python
midpointPosition = vs.GetGradientMidpointPosition(gradientHandle, 4)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
