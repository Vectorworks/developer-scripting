# TextOrigin

## Description
Procedure TextOrigin is used to specify the origin point (location) of a newly created text object.

The position of the actual text with respect to the origin is determined by the current vertical and horizontal text justification modes.

![Text Locus](files/Textlocus.gif)

```pascal
PROCEDURE TextOrigin(pX,pY : REAL);
```

```python
def vs.TextOrigin(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinates of text origin.|

## See Also
VS Functions:
[MoveTo](MoveTo.md)

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
