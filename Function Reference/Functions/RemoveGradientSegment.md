# RemoveGradientSegment

## Description
Removes the specified segment from the specified gradient.

```pascal
PROCEDURE RemoveGradientSegment(
				gradient     : HANDLE;
				segmentIndex : INTEGER);
```

```python
def vs.RemoveGradientSegment(gradient, segmentIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient from which to remove a segment.|
|segmentIndex|INTEGER|Index of segment to be removed.|(segment indexes begin with 1)|

## Examples
==== VectorScript ====
```pascal
RemoveGradientSegment (gradientHandle, 4);
{ removes the segment with index 4 }
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
