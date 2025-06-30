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
|spotPosition|REAL|Position of the segment's color spot relative to left-most point of the gradient.|(position >= 0.0 and position <= 1.0)|
|midpointPosition|REAL|Position of the segment's midpoint relative to color spot immediately to left.|(position >= 0.0 and position <= 1.0)|
|red|LONGINT|Red component of the color spot's color.|(red >= 0 and red <= 255)|
|green|LONGINT|Green component of the color spot's color.|(green >= 0 and green <= 255)|
|blue|LONGINT|Blue component of the color spot's color.|(blue >= 0 and blue <= 255)|

## Examples
#### VectorScript ####
```pascal
index := InsertGradientSegment(gradientHandle, 0.35, 0.4, 255, 255, 255);
{ inserts a white color spot at position, 0.35, with a midpoint position of 0.4 }
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
