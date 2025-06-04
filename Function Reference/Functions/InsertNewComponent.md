# InsertNewComponent

## Description
Inserts a new component in an object.

```pascal
FUNCTION InsertNewComponent(
				obj                  : HANDLE;
				beforeComponentIndex : INTEGER;
				width                : REAL;
				fill                 : LONGINT;
				leftPenWeight        : INTEGER;
				rightPenWeight       : INTEGER;
				leftPenStyle         : INTEGER;
				rightPenStyle        : INTEGER): BOOLEAN;
```

```python
def vs.InsertNewComponent(obj, beforeComponentIndex, width, fill, leftPenWeight, rightPenWeight, leftPenStyle, rightPenStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|beforeComponentIndex|INTEGER|The index before which to insert the new component.|
|width|REAL|The width of the component.|
|fill|LONGINT|The fill of the component.  Positive values for patterns, negative ref numbers for hatches.|
|leftPenWeight|INTEGER|The pen weight of the component's left line.|
|rightPenWeight|INTEGER|The pen weight of the component's right line.|
|leftPenStyle|INTEGER|The pen style of the component's left line.  Positive values for patterns, negative values for dash styles.|
|rightPenStyle|INTEGER|The pen style of the component's right line.  Positive values for patterns, negative values for dash styles.|

## See Also
VS Functions:
[DeleteComponent](DeleteComponent.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
