# LineTo

## Description
Procedure LineTo creates a line object in the document. LineTo draws from the current graphics pen position to the specified coordinate location. The line object is drawn with the current default attributes unless otherwise specified in the VectorScript routine.

```pascal
PROCEDURE LineTo(pX,pY : REAL);
```

```python
def vs.LineTo(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Line endpoint.|

## Remarks
(Joel Sciamma, 2006.08.14): After the line is drawn, the graphics pen is set to the end of the line ready to draw another object. Use [ MoveTo](MoveTo.md) to reset the graphics pen position.

## Examples
#### VectorScript ####
```pascal
LineTo(3,4);
{draws a line from the current pen position to (3, 4)}
```
#### Python ####
```python

```

## See Also
VS Functions: [Absolute](Absolute.md) | [Relative](Relative.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
