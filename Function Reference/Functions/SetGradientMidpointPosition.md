# SetGradientMidpointPosition

## Description
Sets the midpoint position of the specified gradient segment.

```pascal
PROCEDURE SetGradientMidpointPosition(
				gradient     : HANDLE;
				segmentIndex : INTEGER;
				position     : REAL);
```

```python
def vs.SetGradientMidpointPosition(gradient, segmentIndex, position):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment for which to set the data.|(segment indexes begin with 1)|
|position|REAL|Position of the segment's midpoint relatvie to color spot immediately to left.|(position &gt;= 0.0 and position &lt;= 1.0)|

## Examples
#### VectorScript ####
```pascal
SetGradientMidpointPosition(gradientHandle, 4, 0.6);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
