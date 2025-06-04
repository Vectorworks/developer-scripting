# InsertNewComponentN

## Description
Inserts a new component in an object.

```pascal
FUNCTION InsertNewComponentN(
				object               : HANDLE;
				beforeComponentIndex : INTEGER;
				width                : REAL (Coordinate);
				fill                 : LONGINT;
				leftPenWeight        : INTEGER;
				rightPenWeight       : INTEGER;
				leftPenStyle         : LONGINT;
				rightPenStyle        : LONGINT): BOOLEAN;
```

```python
def vs.InsertNewComponentN(object, beforeComponentIndex, width, fill, leftPenWeight, rightPenWeight, leftPenStyle, rightPenStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|beforeComponentIndex|INTEGER|The index before which to insert the new component.|
|width|REAL (Coordinate)|The width of the component.|
|fill|LONGINT|The fill of the component.  Positive values for patterns, negative ref numbers for hatches.|
|leftPenWeight|INTEGER|The pen weight of the component's left line.|
|rightPenWeight|INTEGER|The pen weight of the component's right line.|
|leftPenStyle|LONGINT|The pen style of the component's left line.  Positive values for patterns, negative values for line types.|
|rightPenStyle|LONGINT|The pen style of the component's right line.  Positive values for patterns, negative values for line types.|

## See Also
VS Functions:
[DeleteComponent](DeleteComponent.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
