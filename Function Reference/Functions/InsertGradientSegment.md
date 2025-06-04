# InsertGradientSegment

## Description
Inserts a new segment into the gradient and initializes its data to the specified values.

A segment consists of a single color spot and the single midpoint immediately to the right of the color spot.

```pascal
FUNCTION InsertGradientSegment(
				gradient         : HANDLE;
				spotPosition     : REAL;
				midpointPosition : REAL;
				red              : LONGINT;
				green            : LONGINT;
				blue             : LONGINT): INTEGER;
```

```python
def vs.InsertGradientSegment(gradient, spotPosition, midpointPosition, red, green, blue):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient into which a segment is to be inserted.|
|spotPosition|REAL|Position of the segment's color spot relative to left-most point of the gradient.|(position &gt;= 0.0 and position &lt;= 1.0)|
|midpointPosition|REAL|Position of the segment's midpoint relative to color spot immediately to left.|(position &gt;= 0.0 and position &lt;= 1.0)|
|red|LONGINT|Red component of the color spot's color.|(red &gt;= 0 and red &lt;= 255)|
|green|LONGINT|Green component of the color spot's color.|(green &gt;= 0 and green &lt;= 255)|
|blue|LONGINT|Blue component of the color spot's color.|(blue &gt;= 0 and blue &lt;= 255)|

## Examples
==== VectorScript ====
```pascal
index := InsertGradientSegment(gradientHandle, 0.35, 0.4, 255, 255, 255);
{ inserts a white color spot at position, 0.35, with a midpoint position of 0.4 }
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
