# HAreaN

## Description
Compute the area of a given object, it has the same function as HArea(), but the result in case of polyline is more accurate.

```pascal
FUNCTION HAreaN(ObjectHandle : HANDLE): REAL;
```

```python
def vs.HAreaN(ObjectHandle):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ObjectHandle|HANDLE|It is the object we want to calculate its area.|

## Examples
```pascal
HAreaN(object);
```

```pascal
perim := HPerimN (objH);
area  := HAreaN  (objH);
```
```python
import vs

# Compute the area of a given object, it has the same function as HArea(),
# but the result in case of polyline is more accurate.
ObjectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

area = vs.HAreaN(ObjectHandle)
vs.Message('HAreaN returned: ' + str(area))
```
See also in tutorials: [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [25. Geometric Property Extraction Table](ai%20examples/25_WorksheetPolyGeometry.md), [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md), [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## Version
Availability: from Vectorworks 2012
Deprecated: [Vectorworks 2012 Deprecated Functions](../../Common/Versions/Vectorworks%202012.md)

## Category
* [Object Info](../Categories/Object%20Info.md)
